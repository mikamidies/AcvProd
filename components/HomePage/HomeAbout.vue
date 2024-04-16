<template>
  <div class="wrap">
    <div class="anchor" id="about"></div>
    <div class="container">
      <div class="grid">
        <div class="left">
          <h4 class="heading">Biz haqimizda</h4>
          <div class="items">
            <div class="item">
              <p class="sup">Yillik tajriba</p>
              <p class="num">4+</p>
            </div>
            <div class="item">
              <p class="sup">Mijozlar va hamkorlar</p>
              <p class="num">30+</p>
            </div>
          </div>
        </div>
        <div class="right">
          <p class="par">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Delectus,
            accusantium?
          </p>
          <p class="txt">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Voluptatum
            perferendis maxime itaque voluptatem quas eius quam, veritatis ut
            eveniet quod velit accusantium libero accusamus iste fuga omnis illo
            eligendi repudiandae numquam? Magni? <br />
            Lorem ipsum dolor, sit amet consectetur adipisicing elit. Modi
            repellendus vel ipsum, aliquid explicabo velit aliquam.
          </p>
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
  padding: 80px 0 40px 0;
  position: relative;
}
.grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  max-width: 80%;
  margin: 0 auto;
}
.heading,
.num {
  font-size: 48px;
  font-weight: 600;
}
.items {
  margin-top: 16px;
  display: flex;
  align-items: center;
  gap: 32px;
}
.sup {
  padding-bottom: 16px;
  border-bottom: 2px solid;
  font-weight: 500;
  min-width: 200px;
}
.par {
  font-weight: 700;
  font-size: 20px;
  margin-bottom: 16px;
}
@media screen and (max-width: 1024px) {
  .grid {
    grid-template-columns: repeat(1, 1fr);
  }
  .sup {
    min-width: 0;
  }
}
</style>
