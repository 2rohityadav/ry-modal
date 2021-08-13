# custom-modal

A simple modal dialog reusable component, using only Vanilla JavaScript. No frameworks or external libraries. The modal returns a promise which will give the option that the user chose. ***True*** if the user accepted, ***false*** if the user clicked cancel and ***null*** if the user closed the modal window.

The modal constructor accepts four parameters: the modal window title text, the modal window main text and the text for the accept and cancel buttons. Default values are used if the parameters are not provided.

***Since this component uses modern JavaScript, it should be compiled using Babel before deploying for older browsers.***

## Usage

Import ***modal.css*** and ***modal.js***

```javascript
<link rel="stylesheet" href="modal.css">
<script src="modal.js"></script>
```

Declare a function that will be called by the button, to handle the promise.

```javascript
<script>
  async function openModal() {
    this.myModal = new RyModal();

    try {
      const modalResponse = await myModal.question();
      alert(`The response is ${modalResponse}`);
    } catch(err) {
      console.log(err);
    }
  }
</script>
```

The index.html file provides an usage example.

## License

[MIT](https://choosealicense.com/licenses/mit/)
