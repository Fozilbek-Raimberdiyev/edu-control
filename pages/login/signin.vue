<template>
  <div class="wrapper">
    <form @submit.prevent="signIn()">
        <label for="login">Login</label>
        <input type="text" id="login" placeholder="Loginni kiriting">
        <label for="password">Parol</label>
        <input type="password" id="password" placeholder="Parolni kiriting">
        <button type="submit">Kirish</button>
        <p class="register">Akkauntingiz yo'qmi? <nuxt-link to="/login/signup">Ro'yhatdan o'tish</nuxt-link></p>
    </form>
  </div>
</template>

<script>
export default {
methods : {
    signIn() {
        alert("Hali ish jarayonida emas!")
    }
}
}
</script>

<style scoped>
    .wrapper {
        width: 500px;
        margin: 20% auto;
    }
    form {
        width: 90%;
        margin: 0 auto;
    }
    form label {
        display: block;
        margin: 5px 0;
        font-size: 14px;
    }
    form input {
        display: block;
        width: 90%;
        border: 1px solid #C1C7CD;
        border-radius: 5px;
        padding: 5px 10px;
        outline: none;
    }
    form button {
        display: block;
        width: 90%;
        background: #1D2D5B;
        color: #fff;
        margin: 1rem 0;
        padding: 5px 0;
        border-radius: 5px;
    }
    .register a {
        color: #1D2D5B;
        font-weight: 600;
    }
</style>