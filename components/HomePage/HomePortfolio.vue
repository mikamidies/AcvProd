<template>
  <div class="wrap">
    <h1 class="title">Portfolio</h1>
    <div class="items">
      <div class="item">
        <div class="iframe">
          <iframe
            src="https://www.youtube.com/embed/T_lC2O1oIew?&controls=0&loop=1&rel=0&playlist=T_lC2O1oIew"
            title="YouTube video player"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            referrerpolicy="strict-origin-when-cross-origin"
            allowfullscreen
          ></iframe>
        </div>
      </div>
      <div class="item">
        <div class="iframe">
          <iframe
            src="https://www.youtube.com/embed/T_lC2O1oIew?&controls=0&loop=1&rel=0&playlist=T_lC2O1oIew"
            title="YouTube video player"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            referrerpolicy="strict-origin-when-cross-origin"
            allowfullscreen
          ></iframe>
        </div>
      </div>
      <div class="item">
        <div class="iframe">
          <iframe
            src="https://www.youtube.com/embed/T_lC2O1oIew?&controls=0&loop=1&rel=0&playlist=T_lC2O1oIew"
            title="YouTube video player"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            referrerpolicy="strict-origin-when-cross-origin"
            allowfullscreen
          ></iframe>
        </div>
      </div>
      <div class="item">
        <div class="iframe">
          <iframe
            src="https://www.youtube.com/embed/T_lC2O1oIew?&controls=0&loop=1&rel=0&playlist=T_lC2O1oIew"
            title="YouTube video player"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            referrerpolicy="strict-origin-when-cross-origin"
            allowfullscreen
          ></iframe>
        </div>
      </div>
      <div class="item">
        <div class="iframe">
          <iframe
            src="https://www.youtube.com/embed/T_lC2O1oIew?&controls=0&loop=1&rel=0&playlist=T_lC2O1oIew"
            title="YouTube video player"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            referrerpolicy="strict-origin-when-cross-origin"
            allowfullscreen
          ></iframe>
        </div>
      </div>
      <div class="item">
        <div class="iframe">
          <iframe
            src="https://www.youtube.com/embed/T_lC2O1oIew?&controls=0&loop=1&rel=0&playlist=T_lC2O1oIew"
            title="YouTube video player"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            referrerpolicy="strict-origin-when-cross-origin"
            allowfullscreen
          ></iframe>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.title {
  text-align: center;
  font-weight: 600 !important;
}
.wrap {
  padding: 40px 0;
}
.items {
  padding: 40px 24px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
.item {
  padding: 12px;
  height: 440px;
  cursor: pointer;
  transition: 0.4s;
}
.item:hover {
  background: #ebebeb;
}
.item:nth-child(2) {
  margin-top: 40px;
}
.item:nth-child(4),
.item:nth-child(6) {
  margin-top: -40px;
}

.iframe {
  width: 100%;
  height: 100%;
  overflow: hidden;
}
.iframe iframe {
  transform: scale(1.4);
  width: 100%;
  height: 100%;
  pointer-events: none;
}
</style>
