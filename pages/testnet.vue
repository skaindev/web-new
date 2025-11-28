<template>
  <div class="page">
    <TestnetHeader />
    <main>
      <TestnetHeroSection />
      <TestnetOverviewSection />
      <TestnetBuildSection />
      <TestnetBugBountySection />
    </main>
    <TestnetFooter />
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'Testnet - Skaina',
    }
  },
}
</script>

<style lang="postcss" scoped>
@import url('../components/lib/media-query-helper.css');

.page {
  background: #000 no-repeat;
  background-size: contain;
  background-position: top;

  @media (--viewport-small) {
    background: #000 no-repeat;
    background-size: 100%;
  }
}

main {
  overflow-x: hidden;
}

main > * + *,
footer {
  margin-top: 6rem;

  @media (--viewport-medium) {
    margin-top: 4rem;
  }

  @media (--viewport-small) {
    margin-top: 2rem;
  }
}
</style>
