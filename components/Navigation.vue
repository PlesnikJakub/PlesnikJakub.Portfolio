<template>
  <header>
    <nav class="navbar navbar-expand-lg fixed-top">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">Jakub Plesník</a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNavAltMarkup"
          aria-controls="navbarNavAltMarkup"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div id="navbarNavAltMarkup" class="collapse navbar-collapse">
          <div class="navbar-nav ms-auto">
            <a class="nav-link active" aria-current="page" href="#Home">Home</a>
            <a class="nav-link" href="#About">About me</a>
            <a class="nav-link" href="#Projects">Projects</a>
            <a class="nav-link" href="#Contact">Contact</a>
          </div>
        </div>
      </div>
    </nav>
  </header>
</template>

<style scoped>
.navbar-brand {
  color: var(--primary-text-color);
}
.navbar {
  background: var(--primary-color) !important;
}
.nav-link {
  color: var(--primary-text-color);
}
.nav-link.active {
  font-weight: bold;
}
</style>
