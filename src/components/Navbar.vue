<template>
  <b-row class="navbar-bg fixed-top">
    <b-col lg="1" />
    <b-col lg="10">
      <nav class="navbar navbar-expand-lg row">
        <b-col lg="2">
          <a class="navbar-brand" href="#">
            <img src="../assets/logo.png" class="img-fluid" />
          </a>
        </b-col>
        <b-col lg="7" />
        <b-col lg="3">
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
                <a class="nav-link" href="#">
                  Home
                  <span class="sr-only">(current)</span>
                </a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#about">About</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#books">Books</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="#contact">Contact us</a>
              </li>
            </ul>
          </div>
        </b-col>
      </nav>
    </b-col>
    <b-col lg="1" />
  </b-row>
</template>

<style scoped lang="scss">
.navbar-bg {
  background: linear-gradient(47deg, #8fc7c9, black);
  .nav-link {
    color: #8fc7c9;
  }
}
</style>
