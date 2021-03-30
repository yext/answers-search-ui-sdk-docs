---
title: Icon
order: 16
component: true
appliesTo: Both
apiProperties:
  - property: iconName
    type: string
    description: Use one of the predefined icons in the Answers Search UI Library
  - property: iconUrl
    type: string
    description: Sets the icon to reference an image URL. Overrides icon name.
  - property: classNames
    type: string
    description: Adds class names to the icon. Multiple classnames should be space-delimited. 
---

## Background

The icon component is typically created by other components, but it can also be used as a standalone component. 


## Basic Configuration
```html
<div class='icon-container'></div>
```

```js
ANSWERS.addComponent('IconComponent', {
  container: '.icon-container',
  iconName: 'pantheon',
});
```

## Built-In Icons

The following is a list of names for the icons that are supported by default. You can reference these names when a component has an attribute to set the icon (this includes the search bar, universal results and no results).

| Icon Name        | Image | 
| ------------- | -------------|
| briefcase     | <svg xmlns="http://www.w3.org/2000/svg">
    <path d="M20 7h-4V5c0-1.11-.89-2-2-2h-4c-1.11 0-2 .89-2 2v2H4c-1.11 0-1.99.89-1.99 2L2 20c0 1.11.89 2 2 2h16c1.11 0 2-.89 2-2V9c0-1.11-.89-2-2-2zm-6 0h-4V5h4v2z"></path></svg> |

briefcase
calendar
callout
chevron
close
directions
document
elements
email
gear
info
kabob
light_bulb
link
magnifying_glass
mic
office
pantheon
person
phone
pin
receipt
star
support
tag
thumb
window
yext_animated_forward
yext_animated_reverse
yext
