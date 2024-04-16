<template>
  <div class="wrap">
    <div class="container">
      <div class="left">
        <a href="tel:+998950082299" class="val">+998 95 008 22 99</a>
        <a href="mailto:info@avcprod.com" class="val">info@avcprod.com</a>
        <p class="val">
          Tashkent, Shaykhontohur dst. <br />
          Jangakh 37
        </p>
      </div>
      <div class="right">
        <div class="brand">
          <img src="@/assets/img/white.png" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.wrap {
  background: var(--black);
  color: white;
  padding: 40px 24px;
}
.val {
  font-size: 56px;
  font-weight: 400;
  line-height: 72px;
  color: white;
  display: flex;
}
.container {
  display: grid;
  align-items: flex-end;
  grid-template-columns: 7fr 3fr;
}
.brand {
  display: flex;
  justify-content: flex-end;
}
.brand img {
  width: 320px;
}
</style>
