<template>
  <div v-show="loginForm" class="hello">
    <h1>{{ msg }}</h1>
    <img src="../assets/logo.png" />
    <br>
    <input type="text"  placeholder="아이디를 입력하세요."/>
    <br>
    <input type="password" placeholder="비밀번호를 입력하세요." />
    <br><br>
    <div class="btn-area"><span>로그인</span> | <span v-on:click="join()">회원가입</span></div>
  </div>
  <JoinForm v-show="joinForm" />
  <router-view />
</template>

<script>
import JoinForm from '@/components/JoinForm.vue'

export default {
  name: 'LoginForm',
  props: {
      msg: String
  },
  data() {
      return {
          loginForm: true,
          joinForm: false
      }
  },
  methods: {
      join() {
          this.loginForm = false;
          this.joinForm = true;
      }
  },
  components: {
      JoinForm
  }
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    input {
        height: 20px;
        margin-bottom: 5px;
    }

    .btn-area span{
        background-color: #d8ffd5;
        padding: 5px;
        border-radius: 5px;
        font-weight: bold;
        cursor: pointer;
    }
</style>
