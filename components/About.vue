<template>
  <section id="about-me">
    <MyParticles />
    <div id="content" class="row">
      <div class="col-lg-6 offset-3">
        <div class="card shadow-lg">
          <div class="card-body row">
            <h2>Basic Info</h2>
            <div class="basic-info row mb-5">
              <BasicInfo title="Age" value="27" />
              <BasicInfo
                title="Curent Location"
                value="Ostrava, Czech Republic"
              />
              <BasicInfo title="Alma mater" value="VSB TU-Ostrava" />
              <BasicInfo title="Company" value="SDE Software solutions" />
              <BasicInfo title="Company" value="SDE Software solutions" />
              <BasicInfo title="Company" value="SDE Software solutions" />
            </div>

            <h2>Technologies</h2>
            <p>
              <i>
                I do prefer to work on backend in .Net, but if project requires
                it, I can work with different technologies on both frontend and
                backend.
              </i>
            </p>
            <div class="col-4 technologies">
              <h5>Frontend</h5>
              <ul>
                <li>Vue js</li>
                <li>React</li>
                <li>Next</li>
              </ul>
            </div>
            <div class="col-4 technologies">
              <h5>Backend</h5>
              <ul>
                <li>C#</li>
                <li>.Net</li>
                <li>Php</li>
                <li>Laravel</li>
                <li>Symfony</li>
              </ul>
            </div>
            <div class="col-4 technologies">
              <h5>Data</h5>
              <ul>
                <li>R</li>
                <li>Python</li>
                <li>Graph theory</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.label {
  display: inline-block;
  width: 50px;
}
.technologies ul {
  list-style: none;
}
.card {
  border-radius: 0px;
  background: #212529aa;
  color: var(--primary-text-color);
  padding: 3rem;
}
#about-me {
  position: relative;
}
#content {
  z-index: 1000;
  position: absolute;
  margin: auto;
  top: 10%;
  width: 100%;
}
</style>
