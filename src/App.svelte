<script>
  import { onMount } from 'svelte';
  import QRCode from 'easyqrcodejs';

  let text = '';
  let logo = '';
  let logoWidth = 'auto';
  let logoHeight = 'auto';
  let colorDark = '#275F7A';
  let backgroundImage = '';
  let qrcode;
  $: url = `https://bigstate-safety.appspot.com/${text.replace(' ', '_')}`;

  $: options = {
    text: url,
    logo: logo,
    logoWidth: logoWidth,
    logoHeight: logoHeight,
    colorDark: colorDark,
    backgroundImage: backgroundImage,
  };

  $: console.log(options);

  function newText(text) {
    if (qrcode) {
      qrcode.makeCode(text);
    }
  }

  $: newText(text);

  onMount(() => {
    // text = 'hi';
    // logo =
    //   'http://www.bigstateelectric.com/wp-content/uploads/2015/05/big-state-electric1.png';
    // logoWidth = 80;
    // logoHeight = 80;
    colorDark = '#275F7A';
    backgroundImage =
      'http://www.bigstateelectric.com/wp-content/uploads/2015/05/big-state-electric1.png'; // Background Image
    //backgroundImageAlpha = 1; // Background image transparency, value between 0 and 1. default is 1.
    //autoColor = false;

    qrcode = new QRCode(document.getElementById('qrcode'), options);
  });
</script>

<div id="qrcode" />

<input bind:value={text} />
