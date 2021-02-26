<template>
  <div id="app">
    <div>
      <b-navbar variant="dark" type="dark" class="mb-5">
        <b-navbar-brand>Wade Loccisano</b-navbar-brand>
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
        <b-collapse id="nav-collapse" is-nav>
            <b-navbar-nav class="ml-auto d-none d-md-flex">
              <b-nav-item href="https://drive.google.com/file/d/17tyC2-tGcICv6fQMn2sVXJHrIYt45Y21/view?usp=sharing">Resume</b-nav-item>
              <b-nav-item href="https://www.linkedin.com/in/wade-loccisano">LinkedIn</b-nav-item>
              <b-nav-item href="https://github.com/wade-loccisano">Github</b-nav-item>
              <!-- <b-nav-item to="/about">Email</b-nav-item> -->
            </b-navbar-nav>
            <b-navbar-nav class="ml-auto d-md-none">
              <b-dropdown text="Info" right size="sm">
                <b-dropdown-item href="https://drive.google.com/file/d/17tyC2-tGcICv6fQMn2sVXJHrIYt45Y21/view?usp=sharing">Resume</b-dropdown-item>
                <b-dropdown-item href="https://www.linkedin.com/in/wade-loccisano">LinkedIn</b-dropdown-item>
                <b-dropdown-item href="https://github.com/wade-loccisano">Github</b-dropdown-item>
                <!-- <b-dropdown-item to="/about">Email</b-dropdown-item> -->
              </b-dropdown>
            </b-navbar-nav>
        </b-collapse>
      </b-navbar>
  </div>
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.navbar {
  font-size: 1.35rem !important;
}
.navbar-brand {
  font-size: 1.85rem !important;
}

</style>
