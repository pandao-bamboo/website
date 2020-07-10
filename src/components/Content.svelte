<script>
  let githubLogo = "./images/github_logo.svg";
  let twitterLogo = "./images/twitter_logo.svg";
  let discordLogo = "./images/discord_logo.svg";
  let aragonLogo = "./images/aragon_logo.png";
  let ethereumLogo = "./images/ethereum_logo.png";

  function toggleFooterSection(e) {
    const list = e.target.parentElement.parentElement.querySelector("article");
    if (list.classList.contains("h-0")) {
      list.classList.remove("h-0");
    } else {
      list.classList.add("h-0");
    }
  }
</script>

<section class="bg-gray-700">
  <div class="max-w-screen-lg mx-auto md:px-4 md:pt-10 md:pb-5">
    <div class="flex items-center flex-col">
      <h1
        class="brand-green font-mono sm:text-lg md:text-xl lg:text-2xl my-auto
        mx-auto md:mx-48">
        PanDAO is a Insurance Co-op
      </h1>

      <p class="text-white text-lg mb-5 text-center">
        PanDAO is a decentralized autonomous organization summoned to manage
        pools of liquidity in order to provide every day users insurance for
        their digital assets.
      </p>
    </div>

    <div
      class="border-none px-4 flex flex-row my-5 justify-between items-center
      w-full">
      <div>
        <h1 class="text-white">Trustless</h1>
      </div>

      <div>
        <h1 class="text-white">Member Owned</h1>
      </div>

      <div>
        <h1 class="text-white">Opensource Organization</h1>
      </div>
    </div>
  </div>
  <div class="max-w-screen-lg mx-auto border-none px-4">
    <section
      class="flex flex-row justify-between border-t text-white font-light
      text-sm pt-4 pb-6 pt-5 pb-6 w-full">
      <div class="flex justify-between items-center items-center">

        <span class="mt-2">
          <img
            class="ethereum-logo mr-2"
            src={ethereumLogo}
            alt="ethereum logo" />
        </span>
        <span>
          <img class="mr-5 logo-icons" src={aragonLogo} alt="aragon link" />
        </span>
      </div>

      <div class="flex justify-between items-center">
        <span class="mr-2">
          <a href="https://github.com/pandao-bamboo" target="_blank">
            <img class="social-icons" src={githubLogo} alt="pandao github" />
          </a>
        </span>
        <span class="mr-2">
          <a href="https://twitter.com/PandaoBamboo" target="_blank">
            <img class="social-icons" src={twitterLogo} alt="pandao github" />
          </a>
        </span>
        <span class="mr-2">
          <a href="https://discord.gg/Wg92Ndk" target="_blank">
            <img class="social-icons" src={discordLogo} alt="pandao github" />
          </a>
        </span>
      </div>
    </section>
  </div>
</section>
