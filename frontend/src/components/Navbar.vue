<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <a class="navbar-brand" href="#">Dashboard</a>
    <button
      class="navbar-toggler"
      type="button"
      data-toggle="collapse"
      data-target="#navbarSupportedContent"
      aria-controls="navbarSupportedContent"
      aria-expanded="false"
      aria-label="Toggle navigation"
    >
      <span class="navbar-toggler-icon"></span>
    </button>

    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav mr-auto">
        <li class="nav-item active">
          <a class="nav-link" href="#"
            >Home <span class="sr-only">(current)</span></a
          >
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Profile</a>
        </li>
        <li class="nav-item dropdown">
          <a
            class="nav-link dropdown-toggle"
            href="#"
            id="navbarDropdown"
            role="button"
            data-toggle="dropdown"
            aria-haspopup="true"
            aria-expanded="false"
          >
            Time
          </a>
          <div class="dropdown-menu" aria-labelledby="navbarDropdown">
            <a class="dropdown-item" href="#">Clock in</a>
            <a class="dropdown-item" href="#">Clock out</a>
            <div class="dropdown-divider"></div>
            <a class="dropdown-item" href="#">Change password</a>
          </div>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Reports</a>
        </li>
      </ul>
      <form class="form-inline my-2 my-lg-0">
        <!-- <input
          class="form-control mr-sm-2"
          type="search"
          placeholder="Search"
          aria-label="Search"
        />
        <button class="btn btn-outline-success my-2 my-sm-0" type="submit">
          Search
        </button> -->
        <button @click="this.$store.dispatch('logout')" :v-if="this.$store.state.isAuthenticated" class="btn btn-outline-success my-2 my-sm-0" type="submit">
          Sign out
        </button>
        
      </form>
    </div>
  </nav>
</template>

<script>
export default {
    
}
</script>