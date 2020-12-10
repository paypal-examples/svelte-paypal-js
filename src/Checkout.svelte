<script>
  import { loadScript } from '@paypal/paypal-js';

  loadScript({'client-id': 'sb'}).then(paypal => {
    paypal.Buttons().render('#paypal-button-container')
  });
</script>


<div id="paypal-button-container"></div>