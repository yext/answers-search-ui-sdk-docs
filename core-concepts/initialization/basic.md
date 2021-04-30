---
title: Basic Initialization
order: 1
---

## Basic Initialization

The first step is to initalize the library. This is done using the **`ANSWERS.init`** command.
This function accepts a set of configuration options.

At a minimum `apiKey`, `experienceKey`, `businessId` and `experienceVersion` must be specified.
Here is an example.

```js
ANSWERS.init({
  apiKey: "3517add824e992916861b76e456724d9",
  experienceKey: "answers-js-docs",
  businessId: "3215760",
  experienceVersion: "PRODUCTION",
  onReady: function() {
    // ADD COMPONENTS HERE
  },
});
```

The `onReady` property is used to add components. You can learn more about adding components in the [Components](/components) section.

## Additional Initialization Options

Learn more about additional initialization configuration in the [Initialization Options](/initialization-options) section.
