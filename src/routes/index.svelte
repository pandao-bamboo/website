<script>
  import { onMount } from "svelte";

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
    }
  });
</script>

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
    class="text-base sm:text-xl md:text-2xl lg:text-4xl my-auto mx-auto md:mx-48
    ">
    Sleep better at night knowing your assets are covered.
    <br />
    <span class="brand-green-dark text-base sm:text-lg md:text-xl lg:text-3xl">
      Decentralized Management of Insurance Liquidity Pools
    </span>
    <br />
    <button href="#about-dao" class="button-brand-grey mt-5 font-semibold">
      learn about the dao
    </button>
  </h1>

</section>
