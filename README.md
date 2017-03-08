[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/koada-os/paper-input-username)

# <paper-input-username>

Material design: Text fields with username check system

`<paper-input-username>` is a single-line text field with Material Design styling alowing you to make server-side check to verify if the username is valid.

Example:

<!--

```
<custom-element-demo>
  <template>
    <link rel="import" href="paper-input-username.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```

-->

```html
<paper-input-username id="validInput" minlength="3" min-error-message="Your username must be longer." label="Valid Username" allowed-pattern="[a-zA-Z0-9]"></paper-input-username>
<paper-input-username id="failInput" label="Conflict Username" allowed-pattern="[a-zA-Z]" style="height:10px;"></paper-input-username>
<script>
var validInput = document.getElementById('validInput');
var failInput = document.getElementById('failInput')
var customFailInput = document.getElementById('customFailInput')
validInput.addEventListener('username-changed', function(e,w) {
  console.log(e,w);
    validInput.usernameValid();
});
failInput.addEventListener('username-changed', function() {
    failInput.usernameInvalid('The username already exists');
});
</script>
```
