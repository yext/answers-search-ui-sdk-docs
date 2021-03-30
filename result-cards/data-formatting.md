---
title: Data Formatting
order: 4
---

## Rich Text Formatting

The Yext knowledge graph comes with Rich text fields; these are fields that allow for bolding, italics, hyperlinks, and more! The Answers Search UI includes a `formatRichText` function translates CommonMark to HTML, therefore allowing for rich text to be displayed on a card.


### Definition

```js
ANSWERS.formatRichText(rtfFieldValue, eventOptionsFieldName = null, targetConfig = '')
```

- `rtfFieldValue` is the field reference, for example `item.c_myRichTextField`)
- `eventOptionsFieldName`. When clicking any link in the resulting HTML, an AnalyticsEvent will be fired. If the `eventOptionsFieldName` has been specified, the `eventOption`s will include a fieldName attribute with the given value.
- `targetConfig` dictates where the link is opened: the current window, a new tab, etc. It can have either be a string or an object
    - `targetConfig = '_blank'` - all RTF types will recieve a `_blank` target
    - `targetConfig = { url: '_blank', phone: '_self', email: '_parent' }` - each type of RTF receives a different `target`

> Note that when using this function, you must ensure that the relevant template correctly unescapes the output HTML.

### Example

In this example, rich text formatting is used on the details field for the FAQ.

```js
ANSWERS.addComponent('VerticalResults', {
  /* ...other vertical results config... */
    card: {
        cardType: 'Accordion',
        dataMappings: {
            title: (item) => item.name,
            link: (item) => item.landingPageUrl,
            details: (item) => ANSWERS.formatRichText(item.answer, 'answer', '_self'),               
            url: (item) => item.landingPageUrl,
            target: "_self"
        },
    }
}
```


## Text Highlighting

You can optionally display highlighted fields in your card data mappings. A field becomes highlighted when it's has either either a text search match or a document search match. The `_highlighted`  object, will return the field highlighted with strong tags. You can accesss it in a custom item template. 

```js
this.addComponent("VerticalResults", {
    container: ".vertical-container",
    verticalKey: "locations",
    itemTemplate: `<div>
        {{#if result._highlighted.description}}
            {{{ result._highlighted.description }}}
        {{else}}
            {{result._raw.description}}
        {{/if}}
    </div>`
    });
```

This will display the text highlighting for the `description` field only when it returns, otherwise it will display the raw value. 