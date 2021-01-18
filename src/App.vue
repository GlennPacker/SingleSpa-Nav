<template>
  <div>
    <nav class="navbar-links">
      <div>
        <ul>
          <li>
            <router-link
              to="/basic-page"
              class="nav-link"
              active-class="active-nav-link"
              >
                Basic Page
              </router-link
            >
          </li>
        </ul>
        <ul>
          <li>
            <router-link
              to="/state-share"
              class="nav-link"
              active-class="active-nav-link"
              >
                State Sharing
              </router-link
            >
          </li>
        </ul>
      </div>
    </nav>
    <router-view />
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
nav {
  position: fixed;
  left: 0;
  top: 0;
  height: 100vh;
  /* css var comes from the styleguide */
  width: var(--navbar-width);
  background-color: white;
  transition: left 0.2s ease-in-out;
  box-shadow: 0.2rem 0 0.2rem var(--light-gray);
  z-index: 1000;
}
.navbar-links {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100%;
}
.logo-row {
  display: flex;
  align-items: center;
  font-weight: bold;
  font-size: 1.8rem;
}
.logo {
  height: 4rem;
}
.product-name {
  padding-left: 0.6rem;
}
.logo-link.nav-link,
.logo-link:focus.nav-link:focus {
  height: 4rem;
}
.nav-link:hover {
  background-color: #dfdfdf;
}
ul {
  margin: 0;
  padding: 0;
  list-style-type: none;
}
li {
  list-style: none;
}
.nav-link,
.nav-link:focus,
.nav-link:visited {
  text-decoration: none;
  color: black;
  display: flex;
  align-items: center;
  min-height: 5.6rem;
  padding: 0.8rem 1.6rem;
}
.nav-link > div {
  text-overflow: ellipsis;
  white-space: nowrap;
  width: 100%;
  overflow: hidden;
}
.active-nav-link {
  background-color: #f3f3f3;
}
</style>
