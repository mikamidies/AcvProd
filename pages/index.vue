<template>
  <div class="master">
    <DesktopHeader />

    <main>
      <HomeHero />
      <HomePortfolio />
      <HomeForm />
    </main>

    <DesktopFooter />
  </div>
</template>

<script>
import DesktopHeader from "~/components/DesktopHeader.vue";
import HomeHero from "@/components/HomePage/HomeHero.vue";
import HomePortfolio from "~/components/HomePage/HomePortfolio.vue";
import DesktopFooter from "~/components/DesktopFooter.vue";

export default {
  components: {
    DesktopHeader,
    HomeHero,
    HomePortfolio,
    DesktopFooter,
  },
};
</script>

<style></style>
