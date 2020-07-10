<script>
  import classNames from "classnames";
  import { clickOutside } from "../lib/clickOutside.js";

  // images
  let pandaoLogo = "./images/pandao_logo.png";

  let showProducts = false;
  let dropdownClass =
    "absolute left-0 w-56 mt-2 p-0 m-0 bg-white border shadow-xl invisible";

  const toggleProductsDropdown = () => {
    showProducts = !showProducts;

    dropdownClass = classNames({
      "z-20 absolute right-0 w-64 mt-2 p-0 m-0 bg-white border shadow-xl invisible": !showProducts,
      "z-20 absolute right-0 w-64 mt-2 p-0 m-0 bg-white border shadow-xl visible": showProducts
    });
  };

  const hideProductsDropdown = () => {
    showProducts = false;

    dropdownClass = classNames({
      "z-20 absolute right-0 w-64 mt-2 p-0 m-0 bg-white border shadow-xl invisible": !showProducts,
      "z-20 absolute right-0 w-64 mt-2 p-0 m-0 bg-white border shadow-xl visible": showProducts
    });
  };
</script>

<nav class="navigation bg-gray-800">
  <ul class="flex justify-between text-xl px-8 md:px-48">

    <li
      class="cursor-pointer flex justify-between items-center"
      onclick="location.href='.'">
      <img
        class="w-16 mr-5 cursor-pointer"
        src={pandaoLogo}
        alt="PanDAO Logo" />
      <span class="text-white text-3xl font-semibold">Pan</span>
      <span class="brand-green text-3xl font-bold">DAO</span>
    </li>

    <li class="brand-white flex items-center justify-between">
      <div class="flex justify-center p-12">
        <!-- Dropdown -->
        <div
          class="relative dropdown"
          on:click={toggleProductsDropdown}
          use:clickOutside
          on:click_outside={showProducts ? hideProductsDropdown : null}>
          <button class="block focus:outline-none">Products</button>
          <!-- Dropdown Body -->
          <div class={dropdownClass}>
            <a
              href="."
              class="transition-colors duration-200 block px-4 py-2
              text-gray-900 hover:bg-gray-800 hover:text-white">
              Insure Digital Assets
            </a>
            <div class="py-2" />
            <a
              href="."
              class="transition-colors duration-200 block px-4 py-2 text-normal
              text-gray-900 hover:bg-gray-800 hover:text-white">
              Liquidity Provider
            </a>
          </div>
          <!-- // Dropdown Body -->
        </div>
        <!-- // Dropdown -->
      </div>
      <span>
        <a href=".">DAO</a>
      </span>
    </li>
  </ul>
</nav>
