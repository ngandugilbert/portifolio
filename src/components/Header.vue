<template>
  <div class="container-header container-fluid">
    <div class="avatar">
      <img src="@/assets/images/profile-2.jpg" alt="" />
      Gilbert Ng'andu
    </div>
    <div class="menu">
      <button id="menu-btn" @click="showMenu(), (isMenu = !isMenu)">
        <div class="menu-line" id="line-one"></div>
        <div class="menu-line" id="line-two"></div>
        <div class="menu-line" id="line-three"></div>
      </button>
      <div class="menu-content-large">
        <ul>
          <li>About Me</li>
          <li>Education</li>
          <li>Technical Skills</li>
          <li>Contact Me</li>
        </ul>
      </div>
    </div>
    <div class="menu-content" id="mobile-menu">
      <ul id="list">
        <li>About Me</li>
        <li>
          <a href="#education"> Education</a>
        </li>
        <li>Technical Skills</li>
        <li>Contact Me</li>
        <li>Hire Me</li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  name: "HeaderVue",
  data() {
    return {
      isMenu: true,
    };
  },
  methods: {
    message() {
      alert("Hello");
    },
    showMenu() {
      const menu = document.getElementById("mobile-menu");
      const lineOne = document.getElementById("line-one");
      const lineTwo = document.getElementById("line-two");
      const lineThree = document.getElementById("line-three");
      const List = document.getElementById("list");
      if (this.isMenu) {
        lineThree.style.transform = "translate(100px)";
        menu.style.width = "80%";
        lineOne.style.transform = "rotate(45deg)";
        lineTwo.style.transform = "rotate(-45deg)";
        lineTwo.style.marginTop = "-7px";
        lineTwo.style.background = "red";
        lineOne.style.background = "red";
        List.style.transform = "translate(0)";
      } else {
        menu.style.width = "0";
        lineOne.style.transform = "rotate(0)";
        lineTwo.style.transform = "rotate(0)";
        lineTwo.style.marginTop = "0";
        lineThree.style.display = "flex";
        lineTwo.style.background = "white";
        lineOne.style.background = "white";
        lineThree.style.transform = "translate(0)";
        List.style.transform = "translate(40px)";
      }
    },
    hideMenu() {},
  },
};
</script>
<style scoped>
.container-header {
  display: flex;
  align-items: center;
  padding: 0 20px;
  height: 80px;
  width: 100%;
  justify-content: space-between;
  position: absolute;
  z-index: 1;
}
.avatar {
  display: flex;
  align-items: center;
  height: 40px;
  z-index: 1;
  color: white;
}
.avatar > img {
  height: 40px;
  width: 40px;
  object-fit: cover;
  border-radius: 50%;
  margin-right: 7px;
}
#menu-btn {
  background: transparent;
  border: none;
  cursor: pointer;
  z-index: 4;
}
.menu {
  display: inline-flex;
  position: relative;
}
.menu-line {
  height: 4px;
  width: 31px;
  margin: 3px 0;
  background: white;
  border-radius: 2px;
  transition: all 1s;
}

@media screen and (max-width: 767px) {
  /*Mobile phones*/
  #mobile-menu {
    position: fixed;
    height: 100%;
    width: 0;
    transition: all 1s;
    right: 0;
    top: 0;
    z-index: 3;
  }
  ul {
    display: flex;
    align-items: center;
    flex-direction: column;
    padding: 60px 20px;
    height: 100%;
    position: absolute;
    background: black;
    color: white;
    width: 100%;
    list-style-type: none;
    gap: 10px;
    transform: translate(20px);
    transition: all 0.5s;
    flex-wrap: nowrap;
  }
  .menu-content-large {
    display: none;
  }
}
@media screen and (min-width: 768px) {
  /*large Screens*/
  .menu-content {
    visibility: hidden;
    position: absolute;
  }
  #menu-btn {
    visibility: hidden;
  }
  ul {
    display: flex;
    align-items: center;
    list-style: none;
    color: white;
    height: 100%;
    gap: 15px;
  }
}
</style>