<template>
  <div class="head">
    <div class="header">
      <div class="header__left">
        <div class="header__left__logo">LOGO</div>
      </div>
      <div class="header__middle"></div>
        <nav class="header__middle__nav">
          <ul class="header__gnb__nav--list">
            <li>
              <a>문자발송</a>
            </li>
            <li @mouseover="listAddress = true" @mouseleave="listAddress = false">
              <a>주소록</a>
              <transition name="fade">
                <ul v-if="listAddress" @click="listAddress = false">
                  <li><a href="/#/">주소록 관리</a></li>
                  <li><a href="/#/">수신차단관리</a></li>
                </ul>
              </transition>
            </li>
            <li @mouseover="listSent = true" @mouseleave="listSent = false">
              <a>발송함</a>
              <transition name="fade">
                <ul v-if="listSent" @click="listSent = false">
                  <li><a href="/#/">발송내역</a></li>
                  <li><a href="/#/">예약내역</a></li>
                </ul>
             </transition>
            </li>
            <li>
              <a>충전소</a>
            </li>
            <li @mouseover="listCenter = true" @mouseleave="listCenter = false"> 
              <a>고객센터</a>
              <transition name="fade">
                <ul v-if="listCenter" @click="listCenter = false">
                  <li><a href="/#/">공지사항</a></li>
                  <li><a href="/#/">1:1문의</a></li>
                  <li><a href="/#/">자주묻는질문</a></li>
                  <li><a href="/#/">이용약관</a></li>
                </ul>
             </transition>
            </li>
          </ul>
        </nav>
      <div class="header__right">
        <div class="header__right__items">ITEM_BOX</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      listAddress: false,
      listSent: false,
      listCenter: false
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
a {
  cursor: pointer;
}
.head {
  width: 100%;
  display: flex;
  justify-content: center;
  margin-top: 10px;
}
.header {
  width: 65%;
  height: 50px;
  display: flex;
  justify-content: space-between;
}
.header__left__logo {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100px;
  height: 100%;
  border: 1px solid #ccc;
  text-align: center;
}
.header__middle__nav {
  width: 80%;
  display: flex;
  align-items: center;
}
.header__middle__nav > ul {
  width: 100%;
  display: flex;
  justify-content: space-around;
}
.header__middle__nav > ul > li {
  font-size: 18px;
  font-weight: 400;
}
.header__right__items {
  width: 100px;
  height: 100%;
  border: 1px solid #ccc;
  display: flex;
  justify-content: center;
  align-items: center;
}
.header__gnb__nav--list {
  display: flex;
  justify-content: space-evenly;
  list-style: none;
  height: 100%;
  align-items: center;
  font-size: 20px;
  font-weight: bold;
}
.header__gnb__nav--list > li {
  height: 100%;
  display: flex;
  align-items: center;
}
.header__gnb__nav--list > li > a {
  color: #000;
  position: relative;
  text-transform: uppercase;
  transition: 0.5s;
}
.header__gnb__nav--list > li > a::after {
  position: absolute;
  content: "";
  width: 100%;
  height: 3px;
  top: 100%;
  left: 0;
  background: #ccc;
  transition: transform 0.3s;
  transform: scaleX(0);
  transform-origin: right;
}
.header__gnb__nav--list > li > a:hover {
  color: #ccc;
}
.header__gnb__nav--list > li > a:hover::after {
  transform: scale(1);
  transform-origin: left;
}
.header__gnb__nav--list > img {
  width: 100px;
  cursor: pointer;
}
.header__gnb__nav--list > li {
  position: relative;
}
.header__gnb__nav--list > li > ul {
  position: absolute;
  width: 130px;
  left: 0;
  top: 100%;
  margin: 0;
  padding: 0;
  font-size: 16px;
  z-index: 2;
  color: #000;
}
.header__gnb__nav--list > li > ul > li {
  background: #c1c1c1;
  transition: background .2s;
  list-style: none;
  box-sizing: border-box;
  padding: 10px 5px;
}
.header__gnb__nav--list > li > ul > li:hover {
  background: #fff;
}
.fade-enter-active, .fade-leave-active {
  transition: opacity .2s;
}
.fade-enter, .fade-leave-active {
  opacity: 0;
}
</style>
