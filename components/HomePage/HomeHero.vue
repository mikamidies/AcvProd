<template>
  <div class="wrap" id="hero">
    <iframe
      width="560"
      height="315"
      src="https://www.youtube.com/embed/T_lC2O1oIew?autoplay=1&mute=1&controls=0&loop=1&rel=0&playlist=T_lC2O1oIew"
      title="YouTube video player"
      frameborder="0"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      allowfullscreen
    ></iframe>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.wrap {
  position: relative;
  height: 100vh;
  overflow: hidden;
}
iframe {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  pointer-events: none;
  transform: scale(1.2);
}
.wrap::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 30%;
  background: beige;
  background: rgb(2, 0, 36);
  background: rgb(0, 0, 0);
  background: linear-gradient(
    180deg,
    rgba(0, 0, 0, 1) 0%,
    rgba(0, 0, 0, 0.4990371148459384) 40%,
    rgba(0, 0, 0, 0) 100%
  );
  z-index: 10;
}
.wrap::before {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 30%;
  background: beige;
  background: rgb(2, 0, 36);
  background: rgb(0, 0, 0);
  background: linear-gradient(
    0deg,
    rgba(0, 0, 0, 1) 0%,
    rgba(0, 0, 0, 0.4990371148459384) 40%,
    rgba(0, 0, 0, 0) 100%
  );
  z-index: 10;
}
</style>
