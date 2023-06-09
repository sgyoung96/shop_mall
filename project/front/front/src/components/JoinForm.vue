<template>
  <div class="hello">
    <h1>Join to Vue Shop</h1>
    <img src="../assets/logo.png" />
    <br>
    계정 정보 <br>
    <input type="text" placeholder="이름을 입력하세요." />
    <br>
    <input type="text" placeholder="아이디를 입력하세요." />
    <br>
    <input type="text" placeholder="비밀번호를 입력하세요." />
    <br>
    <input type="text" placeholder="비밀번호를 확인해주세요." />
    <br>
    <input type="radio"  v-model="types" value="판매자"><label>판매자</label>
    <input type="radio"  v-model="types" value="구매자"><label>구매자</label>
    <br><br>
    <div class="btn-area"><span>가입하기</span></div>
  </div>
</template>

<script>
export default {
  name: 'JoinForm',
  data() {
      return {
          types: ''
      }
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
        padding-left: 20px;
        padding-right: 20px;
        border-radius: 5px;
        font-weight: bold;
        cursor: pointer;
    }

</style>
