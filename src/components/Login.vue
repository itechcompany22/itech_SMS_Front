<template>
  <div class="login">
      <div class="login__section">
          <div class="login__section__items">
              <input type="text" placeholder="ID">
              <input type="password" placeholder="PW">
              <button>로그인</button>
              <button>ID/PW 찾기</button>
              <button>회원가입</button>
          </div>
      </div>
  </div>
</template>

<script>
export default {
  name: 'Login'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.login {
    display: flex;
    justify-content: center;
    width: 100%;
}
.login__section {
    display: flex;
    align-items: center;
    width: 65%;
    height: 60px;
}
.login__section__items > input {
    margin-right: 10px;
    height: 20px;
    box-sizing: border-box;
    padding: 0 5px;
}
.login__section__items > button {
    margin-right: 5px;
}
</style>
