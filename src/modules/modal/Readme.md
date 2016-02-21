# Modal

Modal popup.


## Markup

	<t-modal class="modal is-hidden">
		<header class="modal__header">
			<h3 class="modal__title">Hello world</h3>
			<button class="close js-modal-dismiss"></button>
		</header>
		<div class="modal__body">
			...
		</div>
		<footer class="modal__footer">
			<div class="button js-modal-dismiss">Cancel</div>
			<div class="button js-modal-commit">Save</div>
		</footer>
	</t-modal>

To disable modal closing by click on a shade use `data-modal-close-on-shade="no"` attribute:

	<t-modal class="modal is-hidden" data-modal-close-on-shade="no">

## How to open

Auto open:

	<t-modal class="modal is-hidden" data-component="modal" data-modal-open="yes">...</t-modal>

Open via JavaScript:

	<t-modal class="modal pony is-hidden">...</t-modal>
	triggerEvent($$('.pony'), 'tamia.modal.open');

Open via link:

	<a href="#" class="" data-fire="tamia.modal.open" data-target=".js-popup">Open</a>


## Events

### tamia.modal.open

Fire this event on `t-modal` DOM element to open popup.

### tamia.modal.close

Fire this event on `t-modal` DOM element to close popup.

### tamia.modal.commit

Fires when user clicks Save button.

You can prevent popup from closing:

	onEvent($$('.js-popup', 'tamia.modal.commit', () => {
		return false;
	});

### tamia.modal.dismiss

Fires when user click Cancel button.


## Skin

Set `modal_default_skin` or `modules_default_skin` to `true` to enable default skin.


## Configuration

### modal_shade_color

Type: CSS color value.

Color of popup shade layer.