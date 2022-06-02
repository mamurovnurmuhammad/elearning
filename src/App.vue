<template>
  <div class="container border">
    <div class="left border">
      <div class="column">
        <div class="box ">
          <img src="@/assets/logo.png" alt="">
        </div>
        <div class="buttons border">
          <button class="first-btn" @click="first_click()" :class="{ secondclick: first_clicked }">
            <div class="flex border">
              <div class="img border asosiy" :class="{generalgrey: !first_clicked}"></div>
              <p>Asosiy</p>
            </div>
          </button>
          <button class="second-btn" @click="second_click()" :class="{ secondclick: second_clicked }">
            <div class="flex border">
              <div class="img border dars" :class="{darsgrey: second_clicked}"></div>
              <p>Dars jadvali</p>
            </div>
          </button>
          <button class="third-btn" @click="third_click()" :class="{ secondclick: thirtd_clicked }">
            <div class="flex border">
              <div class="img border homework"></div>
              <p>Homework</p>
            </div>
          </button>
          <button class="fourth-btn" @click="fourth_click()" :class="{ secondclick: fourth_clicked }">
            <div class="flex border">
              <div class="img border message"></div>
              <p>Message</p>
            </div>
          </button>
          <button class="fifth-btn" @click="fifth_click()" :class="{ secondclick: fifth_clicked }">
            <div class="flex border">
              <div class="img border group"></div>
              <p>Group</p>
            </div>
          </button>
          <button class="sixth-btn" @click="sixth_click()" :class="{ secondclick: sixth_clicked }">
            <div class="flex border">
              <div class="img border settings"></div>
              <p>Settings</p>
            </div>
          </button>
        </div>
        <div class="flex logout border">
          <button>
            <div class="img border log"></div>
            <p>Log out</p>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  data() {
    return {
      first_clicked: true,
      second_clicked: false,
      thirtd_clicked: false,
      fourth_clicked: false,
      fifth_clicked: false,
      sixth_clicked: false
    }
  },
  methods: {
    first_click() {
      this.first_clicked = true,
        this.second_clicked = false,
        this.thirtd_clicked = false,
        this.fourth_clicked = false
      this.fifth_clicked = false,
        this.sixth_clicked = false
    },
    second_click() {
      this.first_clicked = false,
        this.second_clicked = true,
        this.thirtd_clicked = false,
        this.fourth_clicked = false
      this.fifth_clicked = false,
        this.sixth_clicked = false
    },
    third_click() {
      this.first_clicked = false,
        this.second_clicked = false,
        this.thirtd_clicked = true,
        this.fourth_clicked = false
      this.fifth_clicked = false
      this.sixth_clicked = false
    },
    fourth_click() {
      this.first_clicked = false,
        this.second_clicked = false,
        this.thirtd_clicked = false,
        this.fourth_clicked = true
      this.fifth_clicked = false,
        this.sixth_clicked = false
    },
    fifth_click() {
      this.first_clicked = false,
        this.second_clicked = false,
        this.thirtd_clicked = false,
        this.fourth_clicked = false
      this.fifth_clicked = true,
        this.sixth_clicked = false
    },
    sixth_click() {
      this.first_clicked = false,
        this.second_clicked = false,
        this.thirtd_clicked = false,
        this.fourth_clicked = false
      this.fifth_clicked = false,
        this.sixth_clicked = true
    },
  },
}
</script>

<style>
.border {
  /* border: 1px solid red; */
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.container {
  height: 100vh;
  width: 100vw;
}

.left {
  height: 100%;
  width: 20%
}

.column {
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 100%;
}

.box {
  height: 66px;
  width: 122px;
  margin-top: 8%;
  margin-bottom: 8%;
}

.box img {
  height: 100%;
  width: 100%;
}

.buttons {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-around;
  width: 80%;
  height: 50%;

}

.buttons button {
  width: 100%;
  height: 15%;
  border-radius: 10px;
  border: none;
  background-color: #2C7FE0;
  color: #fff;
  display: flex;
  align-items: center;
  cursor: pointer;
}

.buttons button:hover {
  border: 2px solid #2C7FE0;
}

.buttons button .flex {
  height: 60%;
  display: flex;
  align-items: center;
  margin-left: 10%;
  justify-content: flex-start;
  width: 80%;
}

.flex p {
  font-size: 150%;
  margin-left: 10%;
}

.img {
  background-repeat: no-repeat;
  background-size: cover;
  height: 80%;
  width: 15%;
  background-position: center;
  font-family: sans-serif;
}

.asosiy {
  background-image: url('@/assets/appsico.png');
}

.dars {
  background-image: url('@/assets/calendarico.png');
}

.homework {
  background-image: url('@/assets/schoolbagico.png');
}

.message {
  background-image: url('@/assets/massageico.png');
}

.group {
  background-image: url('@/assets/groupico.png');
}

.settings {
  background-image: url('@/assets/settingsico.png');
}



.generalgrey{
  background-image: url('@/assets/silverappico.png');
}

.darsgrey{
  background-image: url('@/assets/calendar.png');
}

.logout {
  width: 80%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 7%;
  margin-top: 50%;
  cursor: pointer;
}

.logout button {
  height: 100%;
  width: 80%;
  border-radius: 10px;
  border: none;
  background: none;
  color: #C5CBD3;
  display: flex;
  align-items: center;
  cursor: pointer;

}

.logout:hover {
  border: 2px solid #2C7FE0;
  border-radius: 10px;
}

.logout:active {
  background-color: #2C7FE0;
  color: #fff;
}

button .log {
  height: 55%;
  width: 14%;
  background: url('@/assets/logoutico.png');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}


.buttons .first-btn {
  background-color: #fff;
  color: #C5CBD3;
}

.buttons .second-btn {
  background-color: #fff;
  color: #C5CBD3;
}

.buttons .third-btn {
  background-color: #fff;
  color: #C5CBD3;
}

.buttons .fourth-btn {
  background-color: #fff;
  color: #C5CBD3;
}

.buttons .fifth-btn {
  background-color: #fff;
  color: #C5CBD3;
}

.buttons .sixth-btn {
  background-color: #fff;
  color: #C5CBD3;
}




.buttons .secondclick {
  background-color: #2C7FE0;
  color: #fff;
}
</style>

