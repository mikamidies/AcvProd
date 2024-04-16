<template>
  <div class="wrap">
    <div class="container">
      <h4 class="title">Biz bilan bog'lanish</h4>
      <form method="POST" @submit.prevent="sendTelegram">
        <input v-model="name" type="text" placeholder="Ismingiz" />
        <input
          v-model="number"
          type="number"
          placeholder="Telefon raqamingiz"
        />
        <textarea v-model="message" placeholder="Qo'shimcha izoh"></textarea>
        <button type="submit">Yuborish</button>
      </form>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      number: "",
      name: "",
      message: "",

      token: "6921466328:AAGvVVrLd10Uv-yoUmOvkYiamQXezXkw8pg",
      chatId: "-1002002693188",
    };
  },

  methods: {
    sendTelegram() {
      const message = `Name: ${this.name}%0APhone number: ${this.number}%0AMessage: ${this.message}`;

      this.$axios
        .post(
          `https://api.telegram.org/bot${this.token}/sendMessage?chat_id=${this.chatId}&text=${message}`
        )
        .then((response) => {
          console.log("Successfully", response);
          this.number = "";
          this.name = "";
          this.message = "";
          alert("Successfully sent");
        }),
        (error) => {
          console.log(error);
        };
    },
  },
};
</script>

<style scoped>
.wrap {
  padding: 40px 0 80px 0;
}
.title {
  font-weight: 600;
  text-align: center !important;
  margin-bottom: 24px;
}
form {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  gap: 24px;
  max-width: 900px;
  margin: 0 auto;
}
input,
textarea {
  padding: 12px;
  border: 1px solid #ebebeb;
  width: 100%;
}
textarea {
  min-height: 220px;
  resize: none;
}
textarea:focus {
  outline: none;
}
button {
  background: var(--blue);
  color: white;
  padding: 12px 56px;
  max-width: 30%;
}
</style>
