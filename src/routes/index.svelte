<script>
  import { onMount, onDestroy } from "svelte";
  import LandingPage from "../components/LandingPage.svelte";
  import ActionButton from "../components/ActionButton.svelte";

  let bamboo = "./images/bamboo.svg";
  let buttonListener;

  onMount(() => {
    for (let i = 0; i < 100; i++) {
      let star =
        '<div class="star m-0" style="animation: twinkle ' +
        (Math.random() * 5 + 5) +
        "s linear " +
        (Math.random() * 1 + 1) +
        "s infinite; top: " +
        Math.random() * (window.innerHeight - 100) +
        "px; left: " +
        Math.random() * (window.innerWidth - 100) +
        'px;"></div>';
      let header = document.getElementById("header");
      header.innerHTML += star;

      const button = document.getElementById("action-button");

      if (!buttonListener) {
        buttonListener = button.addEventListener("click", () => {
          window.open("https://pandao-handbook.on.fleek.co", "_blank");
        });
      }
    }
  });

  onDestroy(() => {
    buttonListener && buttonListener.removeEventListener();
  });
</script>

<svelte:head>
  <title>
    Digital Asset Insurance and Decentralized Management of Insurance Liquidity
    Pools | PanDAO
  </title>
</svelte:head>

<section
  id="header"
  class="header m-0 flex flex-col w-screen justify-center bg-gray-800 h-screen
  text-gray-100 ">
  <div class="moon">
    <ul>
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
      <li />
    </ul>
  </div>

  <h1
    class="text-base sm:text-xl md:text-2xl lg:text-3xl my-auto mx-auto md:mx-48
    ">
    Sleep better at night knowing your assets are covered
    <br />
    <span class="brand-green-dark text-base sm:text-lg md:text-xl lg:text-2xl">
      Decentralized Management of Insurance Liquidity Pools
    </span>
    <br />

    <ActionButton
      icon={bamboo}
      message="Learn about the DAO"
      url="https://pandao-handbook.on.fleek.co"
      newWindow={true} />
  </h1>
</section>

<LandingPage />
