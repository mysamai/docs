# Writing plugins

In the `<script>` section above add

```js
// Add a new plugin to the list of learnable actions
sam.learn('myplugin', {
  description: 'Say hello from my plugin'
});

// Register the action to perform when a classificationc comes in
sam.action('myplugin', (el, classification = {}) => {
  // `el` is the main HTML element to render in
  // classification has information about what was said
  el.innerHTML = 'Hello from myplugin! You said: '
    + classification.text;
});
```
