<script>
  import Panel from "./Panel.svelte";
  import { iOS } from "$scripts/platform-check";
</script>

<Panel panelTitle={"info"} openIcon={"./icons/heart.svg"} closeIconOffset={8}>
  <header>
    <h2>DMZ Key Locations</h2>
    <p>
      Thanks for using my map! Please contact me through the Discord server
      (link below) if you find a key location that isn't on the map, found a
      typo, bugs, suggestions, etc. I will also be using this Discord for future
      update notes.
    </p>
    <p style:margin-bottom={"2rem"}>
      If you enjoy using this map please consider donating!
    </p>
    <p style:opacity={0.5}>
      Huge thanks to <a
        href="https://www.youtube.com/@TroubleChuteBasics"
        target="_blank"
        rel="noreferrer"
      >
        TroubleChute
      </a>
      for allowing his videos to be used for the project!
    </p>
    <p style:opacity={0.5}>
      Inspired by <a
        href="https://dmzintel.com/"
        target="_blank"
        rel="noreferrer"
      >
        dmzintel
      </a>
      and
      <a href="https://www.dmzmap.com/" target="_blank" rel="noreferrer">
        dmzmap
      </a>
    </p>
    <p style:opacity={0.5}>
      Map by <a
        href="https://www.activision.com/"
        target="_blank"
        rel="noreferrer"
      >
        Activision Publishing, Inc.
      </a>
    </p>
    <p style:opacity={0.5} />
  </header>
  <footer class:scrollbar={!iOS()}>
    <a href="https://discord.gg/vqCwgh8buH" target="_blank" rel="noreferrer">
      <img src="./icons/discord.svg" alt="Discord" />
    </a>
    <a
      href="https://github.com/SjorsWijsman/dmz-key-locations"
      target="_blank"
      rel="noreferrer"
    >
      <img src="./icons/github.svg" alt="Github" />
    </a>
    <a
      href="https://www.paypal.com/donate/?hosted_button_id=L599J6499CT5W"
      target="_blank"
      rel="noreferrer"
    >
      <img src="./icons/heart.svg" alt="Github" />
      <span>Donate</span>
    </a>
  </footer>
</Panel>

<style>
  header {
    padding: 1rem;
  }

  footer {
    position: absolute;
    width: 22rem;
    background-color: var(--color-black);
    display: flex;
    align-items: center;
    padding: 0.5rem 1rem;
    margin-top: 1rem;
    box-shadow: 0 0 1rem var(--color-black-dark);
    bottom: 0;
    border-radius: 0 0 0.5rem 0.5rem;
  }

  @media only screen and (max-width: 30rem) {
    footer {
      width: calc(100% - 10px - 1rem);
      border-radius: 0;
      border-bottom-left-radius: 0.5rem;
    }

    footer:not(.scrollbar) {
      width: calc(100% - 10px);
    }
  }

  h2 {
    margin: 0.5rem 0;
  }

  p {
    opacity: 0.9;
    line-height: 1.3rem;
  }

  footer > a {
    display: block;
    display: flex;
    align-items: center;
    height: 3rem;
    width: 3rem;
    margin-right: 1rem;
    background-color: var(--color-black-dark);
    border-radius: 0.5rem;
    padding: 0.3rem;
    text-decoration: none;
    font-weight: bold;
    transition: all 0.1s ease-out;
  }

  footer > a:hover {
    background-color: var(--color-main);
    transform: scale(1.2);
  }

  footer > a img {
    max-height: 2.5rem;
    max-width: 2.5rem;
  }

  footer > a:last-of-type {
    margin-right: 0;
    margin-left: auto;
    width: 9rem;
    padding: 0.3rem 1rem;
    background-color: var(--color-contrast);
    font-weight: bold;
    font-size: 1.2rem;
  }

  footer > a:last-of-type:hover {
    background-color: var(--color-contrast-light);
  }

  footer > a:last-of-type img {
    max-height: 2rem;
    max-width: 2rem;
    margin: 0;
    margin-right: 0.7rem;
  }
</style>
