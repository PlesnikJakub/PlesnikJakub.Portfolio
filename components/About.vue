<template>
  <section id="about-me">
    <MyParticles />
    <div id="content">
      <h1 class="display-4 text-white">
        Thanks.
      </h1>
      <div class="d-flex flex-wrap">
        <a
          href="https://drive.google.com/file/d/1j5BaNiTBU-DEwL9GmP_4OTNCjP6iGmE3/view?usp=sharing"
          class="btn btn-light btn-lg mr-2"
          target="_blank"
          ><i class="fa fa-file"></i> View CV</a
        >
        <a
          href="https://www.linkedin.com/in/rajeevsinghnaruka/"
          target="_blank"
          class="btn btn-dark btn-lg"
          ><i class="fa fa-linkedin"></i> LinkedIn</a
        >
      </div>
    </div>
  </section>
</template>

<style scoped>
#content {
  z-index: 1000;
  position: absolute;
  margin: auto;
  top: 50%;
  left: 250px;
}
</style>
