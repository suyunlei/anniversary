<template>
  <div class="index">
    <div class="index-left">
      <div class="left-top">
        <p>For Mia and Ray</p>
      </div>
      <div class="left1">
        <p>One Thousand Day</p>
        <p>anniversary</p>
        <p>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="64"
            height="64"
            fill="#000000"
            viewBox="0 0 256 256"
          >
            <rect width="256" height="256" fill="none"></rect>
            <path
              d="M128,216S28,160,28,92A52,52,0,0,1,128,72h0A52,52,0,0,1,228,92C228,160,128,216,128,216Z"
              fill="none"
              stroke="#000000"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="16"
            ></path>
          </svg>
          <span> happy </span>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="64"
            height="64"
            fill="#000000"
            viewBox="0 0 256 256"
          >
            <rect width="256" height="256" fill="none"></rect>
            <path
              d="M128,216S28,160,28,92A52,52,0,0,1,128,72h0A52,52,0,0,1,228,92C228,160,128,216,128,216Z"
              fill="none"
              stroke="#000000"
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="16"
            ></path>
          </svg>
        </p>
      </div>
      <div class="left2">
        <router-link to="./indexPage.vue">
          <a class="button" @click="change">
            Life on the road is bitter, only you are sweet.
          </a>
        </router-link>
      </div>
    </div>
    <div class="index-right">
      <img :src="imgUrl" class="love-rose" v-if="clicking" />
      <img src="../assets/dancing.jpg" class="dancing" v-if="!clicking" />
    </div>
  </div>
</template>

<script>
export default {
  name: "indexPage",
  data() {
    return {
      imgUrl: require("../assets/love-rose.jpg"),
      clicking: true,
    };
  },
  methods: {
    change() {
      this.clicking = !this.clicking;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.index {
  display: grid;
  grid-template-columns: 1fr 1fr;
  /* justify-content: center; */
  width: 100%;
  height: 100vh;
  overflow: hidden;
  background-color: #ced4da;
  color: #212529;
}
.love-rose {
  width: 100%;
  height: auto;
  opacity: 0.8;
}

.index-left {
  height: 100%;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 1fr 6fr 1fr;
  position: relative;
}
.index-right {
  height: 100%;
  overflow: hidden;
  position: relative;
}

.left-top {
  font-weight: 1000;
  font-size: 1.563rem;
  justify-self: center;
  align-self: flex-end;
}
.left1 {
  font-weight: 1000;
  font-size: 3.815rem;
  line-height: 1.2;
  grid-row: 2/3;
  justify-self: center;
  align-self: center;
  text-align: center;
}
.left2 {
  font-weight: 600;
  font-size: 1.563rem;
  grid-row: 3/4;
  justify-self: end;
  align-self: end;
  margin-bottom: 50px;
  margin-right: 50px;
}
.dancing {
  opacity: 0.7;
  width: 100%;
  height: auto;
  position: absolute;
  top: 0;
  bottom: 0;
  margin: auto;
  border-radius: 20px;
}
.button {
  cursor: pointer;
  padding: 5px;
  border-radius: 10px;
  border: 2px solid #adb5bd;
  box-shadow: 10px 10px 5px #adb5bd;
}
a:link {
  text-decoration: none;
  color: #212529;
}
a:visited {
  color: #212529;
  box-shadow: none;
}
a:hover {
  color: #212529;
}
a:active {
  color: #212529;
  box-shadow: none;
}
</style>
