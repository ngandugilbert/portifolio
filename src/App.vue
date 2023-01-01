<template>
  <HeaderVue />
  <div class="intro">
    <img src="@/assets/images/image2.jpeg" alt="" />
    <div class="overlay">
      <h1 id="intro-text">
        Hi,<br />
        I'm Gilbert
      </h1>
      <p>Web <span>developer.</span></p>
      <div class="social">
        <ul>
          <li>
            <img src="@/assets/icons/TwitterIcon.png" alt="" />
          </li>
          <li>
            <a href="http://www.facebook.com/profile.php?id=100085344896959">
              <img src="@/assets/icons/FacebookIcon.png" alt="" />
            </a>
          </li>
          <li>
            <a href="https://github.com/ngandugilbert/">
              <img src="@/assets/icons/GithubIcon.png" alt=""
            /></a>
          </li>
          <li>
            <img src="@/assets/icons/InstagramIcon.png" alt="" />
          </li>
        </ul>
      </div>
    </div>
  </div>
  <ContentVue />
</template>

<script>
import HeaderVue from "./components/Header.vue";
import ContentVue from "./components/Content.vue";

export default {
  name: "App",
  components: {
    HeaderVue,
    ContentVue,
  },
};
</script>

<style scoped>
#app {
  position: relative;
}
.intro {
  position: absolute;
  height: 400px;
  width: 100%;
}
.intro > img {
  height: 100%;
  width: 100%;
  object-fit: cover;
  position: absolute;
}
.overlay {
  display: flex;
  flex-direction: column;
  background: rgba(0, 0, 0, 0.568);
  width: 100%;
  height: 100%;
  position: absolute;
}
#intro-text {
  color: white;
}
.social {
  margin-left: -20px;
  margin-top: 15px;
}
.social ul {
  display: flex;
  list-style: none;
  gap: 20px;
}

@media screen and (max-width: 767px) {
  /*For Mobile Devices*/
  .intro {
    height: 350px;
  }
  #intro-text {
    font-size: 3.8rem;
    margin-top: 85px;
  }
  .overlay p {
    color: white;
    font-size: 1.5rem;
  }
  .overlay {
    padding-left: 20px;
  }
}

@media screen and (min-width: 768px) {
  /*For large Devices*/
  #intro-text {
    font-size: 5.9rem;
    margin-top: 85px;
  }
  .overlay p {
    color: white;
    font-size: 2.5rem;
  }
  .overlay {
    padding-left: 50px;
  }
  br {
    display: none;
  }
}

span {
  border-bottom: 1px solid white;
  padding-bottom: 4px;
}
</style>

