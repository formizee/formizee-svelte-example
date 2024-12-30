<script lang="ts">
	import svelteLogo from '$lib/assets/svelte.svg';
	import windowIcon from '$lib/assets/window.svg';
	import globeIcon from '$lib/assets/globe.svg';
	import fileIcon from '$lib/assets/file.svg';

	let { children } = $props();
</script>

<header>
  <h1>Formizee.</h1>
  <span>+</span>
  <figure>
    <img src={svelteLogo}
      alt="Svelte logo"
      height="38"
      width="38"
    />
    <span>Svelte</span>
  </figure>
</header>
<main>
{@render children()}
</main>
<footer>
  <div>
    <a
      href="https://docs.formizee.com"
      target="_blank"
      rel="noopener noreferrer"
    >
      <img
        aria-hidden={true}
        src={fileIcon}
        alt="File icon"
        width="16"
        height="16"
      />
      Learn
    </a>
    <a
      href="https://docs.formizee.com/docs/quickstart"
      target="_blank"
      rel="noopener noreferrer"
    >
      <img
        aria-hidden={true}
        src={windowIcon}
        alt="Window icon"
        width="16"
        height="16"
      />
      Examples
    </a>
    <a
      href="https://formizee.com"
      target="_blank"
      rel="noopener noreferrer"
    >
      <img
        aria-hidden={true}
        src={globeIcon}
        alt="Globe icon"
        width="16"
        height="16"
      />
      formizee.com
    </a>
  </div>
</footer>

<style>
	:global(body) {
    margin: 0;
    padding: 0;
    display: flex;
    min-height: 100vh;
    align-items: center;
    flex-direction: column;
    justify-content: center;
    text-rendering: optimizeLegibility;
    -moz-osx-font-smoothing: grayscale;
    -webkit-font-smoothing: antialiased;
    font-family: "Inter", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol";
	}

  main {
    width: 100%;
    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: center;
  }

  header {
    gap: 1rem;
    display: flex;
    align-items: center;
    flex-direction: row;

    h1, span {
      font-weight: 700;
    }

    figure {
      flex-direction: row;
      align-items: center;
      display: flex;
      gap: 10px;

      margin: 0;
      font-size: 25px;
      font-weight: 500;
    }
  }

  footer {
    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: center;
    margin-top: 2rem;
    padding: 8px;

    div {
      display: flex;
      flex-direction: row;
      gap: 2rem;
    }

    a {
      gap: 1rem;
      color: black;
      display: flex;
      align-items: center;
      text-decoration: none;
      font-family: 'Space Grotesk'
    }
    a:hover {
      text-decoration: underline;
      text-underline-offset: 4px;
    }
  }


  @font-face {
    font-family: 'Inter';
    src: url('/fonts/inter.ttf') format('truetype');
    font-weight: normal;
    font-style: normal;
  }

  @font-face {
    font-family: 'Space Grotesk';
    src: url('/fonts/space-grotesk.ttf') format('truetype');
    font-weight: normal;
    font-style: normal;
  }
</style>
