<template>
  <div class="wrapper">
    <form class="form" v-if="!formCompleted" @submit.prevent="signUp()">
        <label for="firstName">Ism</label>
        <input type="text" id="firstName" placeholder="Ismingizni kiriting">
        <label for="lastName">Familiya</label>
        <input type="password" id="lastName" placeholder="Familiyangizni kiriting">
        <label for="number">Telefon raqami</label>
        <input type="text" id="number" placeholder="Telefon raqamigizni kiriting">
        <label for="login">Login</label>
        <input type="text" id="login" placeholder="Login kiriting">
        <label for="password">Parol</label>
        <input type="password" id="password" placeholder="Parolni kiriting">
        <button type="submit">Ro'yhatdan o'tish</button>
        <p class="register">Akkauntingiz bormi? <nuxt-link to="/login/signin">Kirish</nuxt-link></p>
    </form>
    <div  v-if="formCompleted" class="verify form">
        <label for="code">Kod</label>
        <input type="text" id="code" placeholder="Yuborilgan kodni kiriting">
        <button @click="sendCode()">Kiritish</button>
    </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            formCompleted: false
        }
    },
methods : {
    signUp() {
        this.formCompleted = true
    },
    sendCode() {

    }
}
}
</script>

<style scoped>
    .wrapper {
        width: 500px;
        margin: 8% auto;
    }
    .form {
        width: 90%;
        margin: 0 auto;
    }
    .form label {
        display: block;
        margin: 5px 0;
        font-size: 14px;
    }
    .form input {
        display: block;
        width: 90%;
        border: 1px solid #C1C7CD;
        border-radius: 5px;
        padding: 5px 10px;
        outline: none;
    }
    .form button {
        display: block;
        width: 90%;
        background: #1D2D5B;
        color: #fff;
        margin: 1rem 0;
        padding: 5px 0;
        border-radius: 5px;
    }
    .form button:hover {
        border-color: rgb(29,45,91,.8);
        background-color: rgb(29,45,91,.8);
    }
    .register a {
        color: #1D2D5B;
        font-weight: 600;
    }
</style>