<script>
  import { loadScript } from "@paypal/paypal-js";
  
  export let cartTotal = 0.01;
  const CLIENT_ID = "test"; // change this to your own client id

  loadScript({ "client-id": CLIENT_ID }).then((paypal) => {
    paypal
      .Buttons({
        style: {
          color: "blue",
          shape: "pill",
        },
        createOrder: function (data, actions) {
          // Set up the transaction
          return actions.order.create({
            purchase_units: [
              {
                amount: {
                  value: cartTotal,
                },
              },
            ],
          });
        },
        onApprove: function (data, actions) {
          // Capture order after payment approved
          return actions.order.capture().then(function (details) {
            alert("Payment successful!");
          });
        },
        onError: function (err) {
          // Log error if something goes wrong during approval
          alert("Something went wrong");
          console.log("Something went wrong", err);
        },
      })
      .render("#paypal-button-container");
  });
</script>

<div id="paypal-button-container" />

<style>
  #paypal-button-container {
    margin: 30px 0;
  }
</style>
