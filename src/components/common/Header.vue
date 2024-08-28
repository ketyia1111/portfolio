<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light fixed-top shadow-sm" id="main-nav">
    <div class="container">
      <a class="logo navbar-brand d-flex align-items-center" href="#">
        <slot></slot>
      </a>
      <button
        aria-controls="navbar4"
        aria-expanded="false"
        aria-label="Toggle navigation"
        class="navbar-toggler"
        data-bs-target="#navbar4"
        data-bs-toggle="collapse"
        type="button"
      >
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbar4">
        <ul class="navbar-nav ms-auto">
          <li v-for="link in links" :key="link.name" class="nav-item px-lg-3">
            <a class="nav-link" :href="link.url">{{ link.name }}</a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  props: ["links"],
  name: "AppHeader",
};
</script>

<style scoped>
* {
  font-weight: 600;
}

.navbar {
  background-color: #ffffff;
}

.nav-link {
  color: #555555;
  transition: color 0.3s;
}

.nav-link:hover {
  color: #007bff;
}

.nav-link.active {
  border-bottom: 2px solid #007bff;
}

.logo {
  font-size: 24px;
  display: flex;
  align-items: center;
  text-decoration: none;
  font-weight: bold;
  font-family: 'Roboto', sans-serif;
}

.navbar-toggler {
  border: none;
}

.navbar-toggler-icon {
  background-image: url("data:image/svg+xml;charset=utf8,%3Csvg viewBox='0 0 30 30' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath stroke='rgba%280, 0, 0, 0.5%29' stroke-width='2' stroke-linecap='round' stroke-miterlimit='10' d='M4 7h22M4 15h22M4 23h22'/%3E%3C/svg%3E");
}
</style>
