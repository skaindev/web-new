<template>
  <div class="banner">
    <v-text line-height="1.5" :weight="500" size="1rem">
      <a href="https://buy.skaina.com" target="_blank">Presale</a> is now live!
    </v-text>
  </div>
  
</template>

<style lang="css" scoped>
@import url('./lib/media-query-helper.css');

.banner {
  /* display: none; */
  background: linear-gradient(180deg, #31C1BF -4.5%, #000 100.1%); 
  padding: 0.25em 1.5em;
  color: #31C1BF;
  text-align: center;
  @media (--viewport-small) {
    padding: 0.25rem 2rem;
  }
}

a {
  color: var( --color-green);
  transition: opacity 0.4s ease-in;
  opacity: 1;
  text-underline-offset: 0.1em;
}

a:hover,
a:focus {
  opacity: 0.8;
  transition: opacity 0.4s ease-in;
}
</style>
