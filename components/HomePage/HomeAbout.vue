<template>
  <div class="wrap">
    <div class="anchor" id="about"></div>
    <div class="container">
      <div class="grid">
        <div class="left">
          <div>
            <h4 class="heading">Biz haqimizda</h4>
            <div class="items">
              <div class="item">
                <p class="sup">Yillik tajriba</p>
                <p class="num">2+</p>
              </div>
              <div class="item">
                <p class="sup">Mijozlar va hamkorlar</p>
                <p class="num">40+</p>
              </div>
            </div>
          </div>
          <img src="@/assets/img/blue.png" alt="" class="logo" />
        </div>
        <div class="right">
          <p class="par">
            Bizning ijodiy video operatorlar guruhimiz onlayn marketing uchun
            qiziqarli va esda qolarli video kontent yaratishga qaratilgan ijodiy
            jamoadir. Biz yaratgan har bir video nafaqat tomoshabinlar
            e'tiborini jalb qilishini, balki uzoq vaqt esda qolarli taassurot
            qoldirishini ta'minlashga intilamiz.
          </p>
          <p class="txt">
            Biz tomoshabinlarni suratga olish, tahrirlash va vizual dizaynga
            innovatsion yondashuvlar orqali jalb qila olamiz. Bizning jamoamiz
            Internet-marketing dunyosidagi tendentsiyalarni o'rganadi va sizga
            va sizning biznesingizga eng samarali va ijodiy echimlarni taklif
            qilish uchun doimiy ravishda takomillashib boradi. <br />
            Biz uchun har bir loyiha bizning shaxsiyatimiz va
            professionalligimizni namoyish etish imkoniyatidir. Biz videolarimiz
            nafaqat sizning noyob vazifangiz va qadriyatlaringizni aks
            ettirishini, balki tomoshabinlarni harakatga ilhomlantirishini
            ta'minlashga intilamiz. Jamoamizga ishoning va biz sizning
            xabaringizni maqsadli auditoriyaga eng jozibali va samarali tarzda
            etkazishda yordam beramiz.
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
  padding: 80px 0 80px 0;
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
.left {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.logo {
  width: 500px;
  opacity: 0.1;
}
@media screen and (max-width: 1024px) {
  .grid {
    grid-template-columns: repeat(1, 1fr);
    max-width: 100%;
    gap: 24px;
  }
  .sup {
    min-width: 0;
    padding-bottom: 8px;
    font-size: 15px;
  }
  .wrap {
    padding: 40px 0;
  }
  .heading {
    font-size: 24px;
  }
  .items {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 24px;
  }
  .logo {
    display: none;
  }
  .par {
    font-size: 16px;
  }
  .txt {
    font-size: 14px;
  }
}
</style>
