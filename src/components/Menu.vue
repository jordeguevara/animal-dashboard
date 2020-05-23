<template>
  <!-- <b-button v-b-toggle.sidebar-menu class="mb-2 toggleMenu" size="sm">
      <b-icon icon="list-nested" color="#282828" aria-hidden="true"></b-icon>
  </b-button>-->
  <!-- <b-sidebar id="sidebar-menu" text-variant="light" title="Menu" visible> -->
  <nav id="sidebar-menu">
    <h3 class="header">Crossing Exchange</h3>
    <ul class="menu-list">
      <li class="menu-item">
        <div class="item">
          <div class="item__image">
            <img class="icon-home" src="../assets/home_unselected.png" />
          </div>
          <span class="item__title">
            <router-link tag="span" to="/">Home</router-link>
          </span>
        </div>
      </li>
      <li class="menu-item">
        <div class="item">
          <div class="item__image">
            <img class="icon" src="../assets/beets_unselected.png" />
          </div>
          <span class="item__title">
            <router-link tag="span" to="/prices">Turnip prices</router-link>
          </span>
        </div>
      </li>
      <li class="menu-item">
        <div class="item">
          <div class="item__image">
            <img class="icon-qr" src="../assets/qr_unselected.png" :style="{width:24, height:24}" />
          </div>
          <span class="item__title">
            <router-link tag="li" to="/design">Design codes</router-link>
          </span>
        </div>
      </li>
      <li class="menu-item">
        <div class="item">
          <div class="item__image">
            <img class="icon" src="../assets/setting.png" :style="{width:24, height:24}" />
          </div>
          <span class="item__title">
            <router-link tag="li" to="/settings">Settings</router-link>
          </span>
        </div>
      </li>
      <li class="menu-item">
        <div class="item">
          <div class="item__image">
            <img class="icon" src="../assets/signout.png" :style="{width:24, height:24}" />
          </div>
          <span class="item__title">
            <router-link tag="li" to="/logout">Logout</router-link>
          </span>
        </div>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  }
};
</script>

<style lang="scss">
@import "global.scss";
.item {
  display: flex;
  // background: green;
  justify-content: center;
  margin: 0 auto;
  width: 60%;
  // box-sizing: border-box;
  &__image {
    // background: red;
    width: 20%;
    padding: 10px 0;
    // display: flex;
  }
  &__title {
    // background: yellow;
    width: 80%;
    padding: 10px 15px;
    text-align: start;
  }
}
.icon {
  width: 30px;
  height: 30px;
  // padding: 5px;
  margin: 0 5px;
  &-qr {
    width: 20px;
    height: 20px;
    margin: 0 5px;
  }
  &-home {
    width: 25px;
    height: 25px;
    margin: 0 5px;
  }
}
#sidebar-menu {
  background: lighten(#f76a8c, 10%) !important;
  width: 20%;
  height: 100vh;
}
.header {
  color: #fff;
  text-align: center;
  padding: 25px;
  font-size: 32px;
  font-weight: 600;
  font-family: fantasy;
}
.menu-list {
  height: auto;
  margin-top: 50px;
  color: #fff;
  display: flex;
  flex-direction: column;
  justify-content: center;
  // background: red;
  padding: 0;
  color: #fff;
}
.menu-item {
  display: flex;
  text-decoration: none;
  list-style: none;
  width: 100%;
  margin: 10px 0;
  padding: 15px 0;
  &:hover {
    background: #f6acc8;
  }
}

.toggleMenu {
  position: fixed;
  left: 1.5%;
  top: 2%;
  background: transparent;
  border: 1px solid #282828;
  &:hover {
    background: #efe4e4;
  }
  &:active,
  &:focus {
    background: #efe4e4;
  }
}

@media (max-width: 1100px) {
  #sidebar-menu {
    display: none;
  }
}

@media (min-width: 1100px) and (max-width: 1300px) {
  .item {
    width: 80%;
    &__image {
      // background: blue;
      width: 30%;
      padding: 10px 0;
      // display: flex;
    }
    &__title {
      // background: purple;
      width: 70%;
      padding: 10px 15px;
      text-align: start;
    }
  }
}
</style>
