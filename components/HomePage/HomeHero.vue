<template>
  <div class="wrap" id="hero">
    <iframe
      width="560"
      height="315"
      src="https://www.youtube.com/embed/kqNG-uBFALo?autoplay=1&mute=1&controls=0&loop=1&rel=0&playlist=kqNG-uBFALo"
      title="YouTube video player"
      frameborder="0"
      allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
      allowfullscreen
    ></iframe>

    <div class="button">
      <a
        href="https://www.youtube.com/watch?v=kqNG-uBFALo&t=2s"
        target="_blank"
      >
        To'liq videoni ko'rish</a
      >
    </div>
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
.button {
  position: absolute;
  bottom: 24px;
  right: 32px;
  z-index: 99;
}
.button a {
  color: white;
  font-size: 24px;
}
@media screen and (max-width: 1024px) {
  .wrap {
    height: 200px;
  }
  iframe {
    transform: scale(1.01);
  }
  .button {
    position: absolute;
    bottom: 16px;
    right: 16px;
  }
  .button a {
    color: white;
    font-size: 18px;
  }
}
</style>
