<script>
  // export let segment;

  // images
  let pandaoLogo = "./images/pandao_logo.png";
  let githubLogo = "./images/github_logo.svg";
  let twitterLogo = "./images/twitter_logo.svg";
  let discordLogo = "./images/discord_logo.svg";
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
    <li class="flex justify-between items-center">
      <span class="mr-3">
        <a
          href="https://github.com/pandao-bamboo"
          target="_blank"
          rel="noopener noreferrer">
          <img class="w-8" src={githubLogo} alt="Github" />
        </a>
      </span>
      <span class="mr-3">
        <a
          href="https://twitter.com/PandaoBamboo"
          target="_blank"
          rel="noopener noreferrer">
          <img class="w-8" src={twitterLogo} alt="Twitter" />
        </a>
      </span>
      <span>
        <a
          href="https://discord.gg/Wg92Ndk"
          target="_blank"
          rel="noopener noreferrer">
          <img class="w-8" src={discordLogo} alt="Community" />
        </a>
      </span>
    </li>
  </ul>
</nav>
