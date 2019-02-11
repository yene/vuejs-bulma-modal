# modal-esc

## Closing a modal dialog by pressing ESC
> The modal is shown and hidden with `v-if` this triggers mounted on every open.

How did bootstrap do it? [_setEscapeEvent](https://github.com/twbs/bootstrap/blob/de0bb1e0522d14bcdef70746da277992f992f83c/js/src/modal.js#L301)

The modal `div` needs a `tabindex` or it cant be focused. After the modal is opened the div is focused, this allows us to filter the `event.target` in the keydown event.


> `tabindex` is required to make a div selectable. Use -1 if you don't want users to be able to tab to it.

## Finding leaked event listeners
After modal is closed there should be no more event listeners for keydown.
In chrome you can inspect the event listeners with `getEventListeners(document)`.

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```
