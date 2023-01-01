<template>
  <div class="wrapper">
    <section class="about-me container-fluid">
      <h3 class="title">About Me</h3>
      <div class="about-me-content row">
        <div class="col-md-6 about-text">
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum
            reprehenderit doloribus omnis hic porro quibusdam quam vero esse non
            sequi soluta, odit quaerat quidem, facere aliquam! Enim quibusdam
            cumque explicabo!
          </p>
        </div>
        <div class="col-md-6">
          <img src="@/assets/images/image2.jpeg" alt="profile" />
        </div>
      </div>
    </section>
    <section class="education container-fluid">
      <h3 class="title">Education</h3>
      <div class="education-history row">
        <div class="col-md-4 col-6">
          <p class="level">BSC. Computer Science</p>
          <p class="school">Copperbelt University</p>
          <p class="duration">2020 - Date</p>
        </div>
        <div class="col-md-4 col-6">
          <p class="level">BSC. Computer Science</p>
          <p class="school">Copperbelt University</p>
          <p class="duration">2020 - Date</p>
        </div>
        <div class="col-md-4 col-6">
          <p class="level">BSC. Computer Science</p>
          <p class="school">Copperbelt University</p>
          <p class="duration">2020 - Date</p>
        </div>
      </div>
    </section>
    <section class="technical-skils container-fluid">
      <h3 class="title">Technical Skills</h3>
      <div class="skills row">
        <div class="col-md-4">
          <p class="level">BSC. Computer Science</p>
          <p class="school">Copperbelt University</p>
          <p class="duration">2020 - Date</p>
        </div>
        <div class="col-md-4">
          <p class="level">BSC. Computer Science</p>
          <p class="school">Copperbelt University</p>
          <p class="duration">2020 - Date</p>
        </div>
        <div class="col-md-4">
          <p class="level">BSC. Computer Science</p>
          <p class="school">Copperbelt University</p>
          <p class="duration">2020 - Date</p>
        </div>
      </div>
    </section>
    <!-- <section class="contact-me container-fluid">
      <h3 class="title">Contact Me</h3>
      <form>
        <input
          type="text"
          class="field"
          name="user_name"
          placeholder="Full names"
        />

        <input type="email" placeholder="Email" />
        <textarea
          name="message"
          id="message"
          cols="30"
          rows="10"
          placeholder="Message"
        ></textarea>
      </form>
    </section> -->
  </div>

  <footer>&copy;2022</footer>
</template>
<script>
export default {
  name: "ContentVue",
};
</script>
<style scoped>
.wrapper {
  padding: 420px 20px 0 20px;
}
/* about-me-content */
.about-me-content img {
  height: 100%;
  width: 100%;
}
ul {
  list-style-type: none;
  margin-left: -25px;
}
.about-text {
  padding-bottom: 30px;
}
</style>