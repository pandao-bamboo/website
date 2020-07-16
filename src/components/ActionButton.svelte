<script>
  export let icon;
  export let url;
  export let message;
  export let newWindow;

  const openHandbook = url => {
    window.open(url, newWindow ? "_blank" : "");
  };
</script>

<button
  id="action-button"
  on:click={e => openHandbook(url)}
  class="flex flex-row justify-between button-brand-grey mt-5 font-semibold ">
  <img src={icon} alt={message} class="w-8 bamboo-icon" />
  {message}
</button>
