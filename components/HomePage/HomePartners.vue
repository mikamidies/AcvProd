<template>
  <div class="wrap">
    <div class="anchor" id="partners"></div>
    <div class="container">
      <h4 class="title">Bizning mijozlarimiz</h4>
      <div class="grid">
        <div class="item">
          <img src="@/assets/img/part-1.png" alt="" />
        </div>
        <div class="item">
          <img src="@/assets/img/part-2.png" alt="" />
        </div>
        <div class="item">
          <img src="@/assets/img/part-3.png" alt="" />
        </div>
        <div class="item">
          <img src="@/assets/img/part-4.png" alt="" />
        </div>
        <div class="item">
          <img src="@/assets/img/part-5.png" alt="" />
        </div>
        <div class="item">
          <img src="@/assets/img/part-6.png" alt="" />
        </div>
        <div class="item">
          <img src="@/assets/img/part-7.png" alt="" />
        </div>
        <div class="item">
          <img src="@/assets/img/part-8.png" alt="" />
        </div>
        <div class="item">
          <img src="@/assets/img/part-9.png" alt="" />
        </div>
        <div class="item">
          <img src="@/assets/img/part-10.png" alt="" />
        </div>
        <div class="item">
          <img src="@/assets/img/part-11.png" alt="" />
        </div>
        <div class="item">
          <img src="@/assets/img/part-12.png" alt="" />
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
  padding-bottom: 120px;
  position: relative;
}
.grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 4px;
  max-width: 80%;
  margin: 0 auto;
}
.title {
  text-align: center;
  margin-bottom: 24px;
}
.item img {
  width: 80%;
  height: 60%;
  object-fit: contain;
  transform: scale(0.9);
  transition: 0.3s;
}
.item:hover img {
  transform: scale(1);
}
.item {
  height: 120px;
  border: 1px solid #ebebeb;
  display: flex;
  align-items: center;
  justify-content: center;
}
@media screen and (max-width: 1024px) {
  .wrap {
    padding-bottom: 80px;
  }
  .grid {
    max-width: 100%;
    grid-template-columns: repeat(2, 1fr);
  }
  .item {
    height: 80px;
  }
}
</style>
