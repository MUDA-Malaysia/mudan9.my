<script context="module">
  import {
    addMessages,
    init,
    getLocaleFromNavigator /*, register */
  } from 'svelte-intl-precompile';
  // import en from '$locales/en.js'; // If using typescript you can also use the .ts extension.
  // import es from '$locales/es.js'; // load from $myprefix/es.js you configured a custom import path.
  // if you put your translations in js files, import then usin the relative path. E.g. `import en from '../../locales/en.js'`
  // @ts-ignore
  // addMessages('en', en);
  // addMessages('es', es);
  // register('es', () => import('$locales/es.js')); <-- use this approach if you want locales to be load lazily

  init({
    fallbackLocale: 'en',
    initialLocale: getLocaleFromNavigator() || 'en'
  });
</script>

<script lang="ts">
  // import { page } from '$app/stores';
  import { onMount } from 'svelte';
  import '../app.scss';

  onMount(() => {
    console.log(window.innerHeight, window.outerHeight);
    window.addEventListener('scroll', (e) => {
      console.log(e);
    });
  });
</script>

<svelte:head>
  <title>Parti MUDA | N9</title>
  <meta name="description" content="Parti MUDA Negeri Sembilan" />
  <meta property="og:title" content="MUDA" />
  <meta property="og:description" content="Parti MUDA Negeri Sembilan" />
  <meta property="og:image" content="/muda-n9.png" />
</svelte:head>

<svg
  style="position: fixed; left: -9999999px"
  version="2.0"
  xmlns="http://www.w3.org/2000/svg"
  xmlns:xlink="http://www.w3.org/1999/xlink"
>
  <defs>
    {@html `<linearGradient id="ig_paint0_linear" x1="1.27375" y1="131.698" x2="122.063" y2="10.9086" gradientUnits="userSpaceOnUse">
    <stop stop-color="#FFD521"/><stop offset="0.05" stop-color="#FFD521"/><stop offset="0.501119" stop-color="#F50000"/><stop offset="0.95" stop-color="#B900B4"/><stop offset="0.950079" stop-color="#B900B4"/><stop offset="1" stop-color="#B900B4"/>
      </linearGradient>
      <linearGradient id="ig_paint1_linear" x1="1.27382" y1="131.863" x2="122.163" y2="10.9746" gradientUnits="userSpaceOnUse">
        <stop stop-color="#FFD521"/><stop offset="0.05" stop-color="#FFD521"/><stop offset="0.501119" stop-color="#F50000"/><stop offset="0.95" stop-color="#B900B4"/><stop offset="0.950079" stop-color="#B900B4"/><stop offset="1" stop-color="#B900B4"/>
      </linearGradient>
      <linearGradient id="ig_paint2_linear" x1="1.30515" y1="131.867" x2="122.165" y2="11.0069" gradientUnits="userSpaceOnUse">
        <stop stop-color="#FFD521"/><stop offset="0.05" stop-color="#FFD521"/><stop offset="0.501119" stop-color="#F50000"/><stop offset="0.95" stop-color="#B900B4"/><stop offset="0.950079" stop-color="#B900B4"/><stop offset="1" stop-color="#B900B4"/>
      </linearGradient>`}
    {@html `<symbol id="tiktok" viewBox="0 0 48 48"><path d="M34.353 17.3269C37.4397 19.5413 41.2211 20.8442 45.3051 20.8442V12.9572C44.5322 12.9574 43.7613 12.8765 43.0051 12.7157V18.9239C38.9214 18.9239 35.1405 17.621 32.053 15.4068V31.5017C32.053 39.5533 25.5492 46.0798 17.5268 46.0798C14.5334 46.0798 11.7512 45.1716 9.44006 43.6141C12.0779 46.3208 15.7565 48 19.8263 48C27.8492 48 34.3534 41.4734 34.3534 33.4215V17.3269H34.353ZM37.1904 9.36999C35.6129 7.64045 34.5772 5.40535 34.353 2.93435V1.91992H32.1735C32.7221 5.06056 34.5934 7.74374 37.1904 9.36999ZM14.5142 37.4356C13.6329 36.2759 13.1566 34.8572 13.1587 33.3985C13.1587 29.716 16.1336 26.7302 19.8037 26.7302C20.4877 26.7301 21.1675 26.8352 21.8194 27.0427V18.9795C21.0576 18.8748 20.2888 18.8303 19.5203 18.8466V25.1226C18.868 24.915 18.1878 24.8096 17.5037 24.8103C13.8335 24.8103 10.8589 27.7957 10.8589 31.4787C10.8589 34.0828 12.3458 36.3373 14.5142 37.4356Z" fill="#FF004F"/><path d="M32.0529 15.4066C35.1404 17.6208 38.9213 18.9237 43.005 18.9237V12.7156C40.7255 12.2283 38.7075 11.0328 37.1903 9.36999C34.5931 7.74358 32.722 5.0604 32.1733 1.91992H26.4482V33.4212C26.4352 37.0936 23.4655 40.0672 19.8032 40.0672C17.6451 40.0672 15.7279 39.0348 14.5136 37.4356C12.3454 36.3373 10.8585 34.0826 10.8585 31.4788C10.8585 27.7962 13.8331 24.8104 17.5032 24.8104C18.2064 24.8104 18.8842 24.9203 19.5199 25.1228V18.8468C11.6384 19.0102 5.2998 25.473 5.2998 33.4214C5.2998 37.3892 6.87827 40.9861 9.44013 43.6143C11.7513 45.1716 14.5335 46.08 17.5268 46.08C25.5494 46.08 32.0531 39.5531 32.0531 31.5017V15.4066H32.0529Z" fill="black"/><path d="M43.0051 12.7156V11.037C40.9495 11.0401 38.9343 10.4624 37.1903 9.36987C38.7342 11.0661 40.7671 12.2357 43.0051 12.7156ZM32.1734 1.91997C32.1211 1.61982 32.0809 1.3177 32.053 1.01443V0H24.148V31.5016C24.1354 35.1735 21.1658 38.1471 17.5033 38.1471C16.428 38.1471 15.4128 37.891 14.5137 37.4358C15.7279 39.0349 17.6452 40.0671 19.8033 40.0671C23.4652 40.0671 26.4354 37.0938 26.4482 33.4214V1.91997H32.1734ZM19.5203 18.8468V17.0598C18.8598 16.9692 18.1938 16.9237 17.5271 16.924C9.50383 16.9239 3 23.4508 3 31.5016C3 36.5491 5.55612 40.9974 9.44034 43.614C6.87848 40.986 5.30002 37.3889 5.30002 33.4213C5.30002 25.473 11.6385 19.0102 19.5203 18.8468Z" fill="#00F2EA"/></symbol>`}
    {@html `<symbol id="facebook" viewBox="0 0 48 48"><g clip-path="url(#clip0_17_24)"><path d="M48 24C48 10.7452 37.2548 0 24 0C10.7452 0 0 10.7452 0 24C0 35.9789 8.77641 45.908 20.25 47.7084V30.9375H14.1562V24H20.25V18.7125C20.25 12.6975 23.8331 9.375 29.3152 9.375C31.9402 9.375 34.6875 9.84375 34.6875 9.84375V15.75H31.6613C28.68 15.75 27.75 17.6002 27.75 19.5V24H34.4062L33.3422 30.9375H27.75V47.7084C39.2236 45.908 48 35.9789 48 24Z" fill="#1877F2"/><path d="M33.3422 30.9375L34.4062 24H27.75V19.5C27.75 17.602 28.68 15.75 31.6613 15.75H34.6875V9.84375C34.6875 9.84375 31.9411 9.375 29.3152 9.375C23.8331 9.375 20.25 12.6975 20.25 18.7125V24H14.1562V30.9375H20.25V47.7084C22.7349 48.0972 25.2651 48.0972 27.75 47.7084V30.9375H33.3422Z" fill="white"/></g><defs><clipPath id="clip0_17_24"><rect width="48" height="48" fill="white"/></clipPath></defs></symbol>`}
    {@html `<symbol id="twitter" viewBox="0 0 24 20"><path d="M7.54752 19.7507C16.6042 19.7507 21.5578 12.2473 21.5578 5.74046C21.5578 5.52734 21.5578 5.31518 21.5434 5.10398C22.507 4.40693 23.3389 3.54386 24 2.55518C23.1014 2.95358 22.148 3.21473 21.1718 3.3299C22.1998 2.71459 22.9692 1.74668 23.3366 0.606379C22.3701 1.17999 21.3126 1.58421 20.2099 1.80158C19.4675 1.01216 18.4856 0.48942 17.4162 0.314263C16.3468 0.139107 15.2494 0.321294 14.294 0.832632C13.3385 1.34397 12.5782 2.15595 12.1307 3.14293C11.6833 4.1299 11.5735 5.23684 11.8186 6.29246C9.8609 6.19426 7.94576 5.68549 6.19745 4.79918C4.44915 3.91288 2.90676 2.66884 1.6704 1.14782C1.04073 2.23181 0.847872 3.51505 1.1311 4.73624C1.41433 5.95744 2.15234 7.02477 3.19488 7.72094C2.41123 7.69798 1.64465 7.48657 0.96 7.10462V7.16702C0.960311 8.30387 1.35385 9.40561 2.07387 10.2854C2.79389 11.1652 3.79606 11.7688 4.9104 11.9939C4.18548 12.1916 3.42487 12.2205 2.68704 12.0784C3.00181 13.0567 3.61443 13.9122 4.43924 14.5253C5.26405 15.1384 6.25983 15.4785 7.28736 15.4979C6.26644 16.3004 5.09731 16.8937 3.84687 17.2439C2.59643 17.5941 1.28921 17.6943 0 17.5389C2.25183 18.9839 4.87192 19.7504 7.54752 19.7469" fill="#1DA1F2"/></symbol>`}
    {@html `<symbol id="instagram" viewBox="0 0 134 134"><path d="M110.116 31.0217C110.116 26.599 106.531 23.028 102.125 23.028C97.7189 23.028 94.1313 26.599 94.1313 31.0217C94.1313 35.4281 97.7189 38.9991 102.125 38.9991C106.531 38.9991 110.116 35.4281 110.116 31.0217Z" fill="url(#ig_paint0_linear)"/><path d="M120.763 93.42C120.467 99.9079 119.382 103.433 118.481 105.774C117.271 108.878 115.828 111.098 113.486 113.426C111.171 115.754 108.952 117.194 105.848 118.391C103.506 119.305 99.9681 120.394 93.4805 120.703C86.4666 121.012 84.3883 121.078 66.602 121.078C48.8322 121.078 46.7374 121.012 39.7235 120.703C33.2359 120.394 29.7142 119.305 27.3727 118.391C24.2522 117.194 22.0492 115.754 19.7211 113.426C17.3764 111.098 15.933 108.878 14.7393 105.774C13.8382 103.433 12.7368 99.9079 12.4571 93.42C12.1153 86.4061 12.0526 84.2951 12.0526 66.545C12.0526 48.7587 12.1153 46.6639 12.4571 39.65C12.7368 33.1624 13.8382 29.6406 14.7393 27.2795C15.933 24.1787 17.3764 21.9722 19.7211 19.6441C22.0492 17.3194 24.2522 15.8757 27.3727 14.6658C29.7142 13.7484 33.2359 12.6763 39.7235 12.3673C46.7374 12.058 48.8322 11.9791 66.602 11.9791C84.3883 11.9791 86.4666 12.058 93.4805 12.3673C99.9681 12.6763 103.506 13.7484 105.848 14.6658C108.952 15.8757 111.171 17.3194 113.486 19.6441C115.828 21.9722 117.271 24.1787 118.481 27.2795C119.382 29.6406 120.467 33.1624 120.763 39.65C121.089 46.6639 121.168 48.7587 121.168 66.545C121.168 84.2951 121.089 86.4061 120.763 93.42ZM132.743 39.1042C132.417 32.0146 131.299 27.171 129.638 22.9523C127.948 18.5755 125.683 14.8663 121.973 11.1571C118.281 7.46446 114.572 5.19875 110.195 3.48894C105.96 1.84471 101.132 0.713455 94.0393 0.404434C86.9465 0.0623779 84.681 -3.05176e-05 66.602 -3.05176e-05C48.5395 -3.05176e-05 46.2575 0.0623779 39.1647 0.404434C32.0881 0.713455 27.2642 1.84471 23.0093 3.48894C18.649 5.19875 14.9398 7.46446 11.2472 11.1571C7.538 14.8663 5.27229 18.5755 3.56567 22.9523C1.92145 27.171 0.803515 32.0146 0.461452 39.1042C0.152436 46.197 0.0735168 48.466 0.0735168 66.545C0.0735168 84.6075 0.152436 86.873 0.461452 93.9658C0.803515 101.042 1.92145 105.883 3.56567 110.121C5.27229 114.481 7.538 118.207 11.2472 121.9C14.9398 125.592 18.649 127.875 23.0093 129.581C27.2642 131.225 32.0881 132.343 39.1647 132.669C46.2575 132.995 48.5395 133.073 66.602 133.073C84.681 133.073 86.9465 132.995 94.0393 132.669C101.132 132.343 105.96 131.225 110.195 129.581C114.572 127.875 118.281 125.592 121.973 121.9C125.683 118.207 127.948 114.481 129.638 110.121C131.299 105.883 132.417 101.042 132.743 93.9658C133.068 86.873 133.147 84.6075 133.147 66.545C133.147 48.466 133.068 46.197 132.743 39.1042Z" fill="url(#ig_paint1_linear)"/><path d="M66.602 88.7046C54.3597 88.7046 44.4258 78.787 44.4258 66.5447C44.4258 54.2827 54.3597 44.3523 66.602 44.3523C78.8477 44.3523 88.7947 54.2827 88.7947 66.5447C88.7947 78.787 78.8477 88.7046 66.602 88.7046ZM66.602 32.3566C47.7305 32.3566 32.4467 47.6733 32.4467 66.5447C32.4467 85.3999 47.7305 100.7 66.602 100.7C85.4734 100.7 100.774 85.3999 100.774 66.5447C100.774 47.6733 85.4734 32.3566 66.602 32.3566Z" fill="url(#ig_paint2_linear)"/></symbol>`}
  </defs>
</svg>

<nav>
  <div class="logo">
    <a href="/">MUDA N9</a>
  </div>
  <ul>
    <li><a href="/ge15">GE15 (2022)</a></li>
    <!-- <li><a href="/about-us">ABOUT US</a></li>
    <li><a href="/states">STATE</a></li>
    <li><a href="">About Us</a></li>
    <li><a href="">About Us</a></li> -->
  </ul>
</nav>

<main>
  <slot />
</main>

<footer>
  <ul class="social-media-list">
    <li>
      <a href="https://www.tiktok.com/@mudan9" target="_blank"
        >{@html `<svg width="100%" height="100%"><use href="#tiktok" /></svg>`}</a
      >
    </li>
    <li>
      <a href="https://www.instagram.com/partimudan9" target="_blank">
        {@html `<svg width="100%" height="100%"><use href="#instagram" /></svg>`}
      </a>
    </li>
    <li>
      <a href="https://twitter.com/partimudan9" target="_blank">
        {@html `<svg width="100%" height="100%"><use href="#twitter" /></svg>`}
      </a>
    </li>
    <li>
      <a href="https://www.facebook.com/partimudaN9" target="_blank"
        >{@html `<svg width="100%" height="100%"><use href="#facebook" /></svg>`}</a
      >
    </li>
  </ul>
  <!-- <ul class="locale-list">
    <li><a href="{$page.url}?lang=ms">Bahasa Melayu</a></li>
    <li><a href="{$page.url}?lang=zh">中文(简体)</a></li>
    <li><a href="{$page.url}?lang=en">English</a></li>
  </ul> -->
  <div style="text-align: center">Copyright Reserved © 2022. MUDA N9.</div>
  <div>
    Designed & Made by <a href="https://www.linkedin.com/in/sian-loong-7b4a3037" target="_blank"
      >SianLoong</a
    >.
  </div>
  <div>#MUDAN9 #INIRASAHKITA</div>
</footer>

<style lang="scss">
  nav {
    display: flex;
    max-width: 1024px;
    width: 100%;
    align-items: center;
    justify-content: space-between;
    margin: 0 auto;

    .logo {
      visibility: hidden;
      padding: 1.5rem;
      padding-right: 0;
      font-size: 26px;
      font-weight: bold;
    }

    ul {
      display: flex;
      justify-content: flex-end;
      padding: 1.5rem;

      li {
        display: block;
        margin: 0 0.5rem;
      }
    }

    @media screen and (min-width: 480px) {
      .logo {
        visibility: visible;
      }
    }
  }

  main {
    // flex: 1;
    // display: flex;
    // flex-direction: column;
    // padding: 1rem;
    // width: 100%;
    // box-sizing: border-box;
    max-width: 1024px;
    flex-grow: 1;
    margin: 0 auto;
  }

  footer {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 2rem 1.5rem 3rem;

    .social-media-list,
    .locale-list {
      list-style: none;
      list-style-position: inside;
      display: flex;

      li {
        margin: 6px;
      }
    }

    .social-media-list {
      li {
        a {
          display: inline-flex;
          width: 32px;
          height: 32px;
        }
      }
    }

    .locale-list {
      padding: 10px 0;
    }
  }

  footer a {
    font-weight: bold;
  }

  @media (min-width: 480px) {
    footer {
      padding: 1.5rem 0;
    }
  }
</style>
