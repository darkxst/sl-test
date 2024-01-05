# Proof of concept SL Web Tools site

Visit https://darkxst.github.io/silabs-firmware-builder/

Implementation is as simple as adding the following html to your page.

```html
    <script 
      type="module" 
      src="https://unpkg.com/@nabucasa/sl-web-tools@0.10.0/dist/web/nabucasa-zigbee-flasher.js?module">
    </script>
    
    <nabucasa-zigbee-flasher manifest="./assets/manifests/zbdongle-e.json">
        <span slot="button">Connect</span>
    </nabucasa-zigbee-flasher>
```

Sample [manifest](https://github.com/darkxst/sl-test/blob/gh-pages/assets/manifests/zbdongle-e.json) file

Powered by [SL Web Tools](https://github.com/NabuCasa/sl-web-tools)
