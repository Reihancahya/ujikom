<template>
  <nav class="navbar navbar-expand-lg bg-primary sticky-top">
    <div class="container-fluid">
      <a class="navbar-brand text-white" href="#">
        <img
          src="/assets/img/logo.png"
          alt="Logo"
          width="45"
          class="d-inline-block align-self-center"
        />
        Smk Negeri 4 Tasikmalya
      </a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
        <ul class="navbar-nav">
          <nuxt-link to="/">
            <li class="nav-item">
              <a class="nav-link text-white" aria-current="page" href="#"
                >Beranda</a
              >
            </li>
          </nuxt-link>
          <nuxt-link to="/profil">
            <li class="nav-item">
              <a class="nav-link text-white" href="#">Profil</a>
            </li>
          </nuxt-link>
          <nuxt-link to="/eskul">
            <li class="nav-item">
              <a class="nav-link text-white" href="#">Ekstrakurikuler</a>
            </li>
          </nuxt-link>
          <nuxt-link to="/galeri">
            <li class="nav-item">
              <a class="nav-link text-white" href="#">Galeri</a>
            </li>
          </nuxt-link>
          <nuxt-link to="/Biodata">
            <li class="nav-item">
              <a class="nav-link text-white" href="#">Biodata</a>
            </li>
          </nuxt-link>
        </ul>
      </div>
    </div>
  </nav>
</template>
