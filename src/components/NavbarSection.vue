<template>
  <header class="header" id="head">
    <div class="navbar__section">
      <div class="navbar navbar-expand-lg">
        <div class="container">
          <div class="brand_wrapper">
            <a class="navbar-brand" href="#"
              ><img src="./../../public/images/MainPageImgs/frame1.png" alt=""
            /></a>
            <a class="navbar-brand" href="#"
              ><img src="./../../public/images/MainPageImgs/frame2.png" alt=""
            /></a>
            <a class="navbar-brand last" href="#"
              ><img src="./../../public/images/MainPageImgs/frame3.png" alt=""
            /></a>
          </div>
          <form class="d-flex">
            <label for="search__input">
              <i class="lnr lnr-magnifier"></i>
            </label>
            <input
              id="search__input"
              class="form-control"
              type="search"
              placeholder="Поиск по сайту"
              aria-label="Search"
            />
          </form>
          <button
            class="navbar-toggler"
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#navbarSupportedContent"
            aria-controls="navbarSupportedContent"
            aria-expanded="false"
            aria-label="Toggle navigation"
          >
            <i class="lnr lnr-menu"></i>
          </button>
          <div
            class="collapse_menu collapse navbar-collapse"
            id="navbarSupportedContent"
          >
            <ul class="navbar-nav ml-4 mb-0 mb-lg-0">
              <li class="nav-item">
                <a
                  class="nav-link active"
                  aria-current="page"
                  @click="$router.push('/contacts')"
                  ><i class="lnr lnr-smartphone"></i
                ></a>
              </li>
              <li class="nav-item">
                <router-link class="nav-link" :to="{ name: `News` }"
                  ><i class="fas fa-solid fa-glasses"></i
                ></router-link>
              </li>
              <li class="nav-item">
                <a
                  class="nav-link i"
                  aria-current="page"
                  @click="$router.push('/news')"
                  ><i class="lnr lnr-volume-medium"></i
                ></a>
              </li>
              <li class="nav-item l">
                <span class="m-0 p-0"> | </span>
              </li>
              <li class="nav-item dropdown">
                <a
                  class="nav-link dropdown-toggle"
                  href="#"
                  id="navbarDropdown"
                  role="button"
                  data-bs-toggle="dropdown"
                  aria-expanded="false"
                >
                  Рус
                </a>
                <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
                  <li><a class="dropdown-item" href="#">Eng</a></li>
                </ul>
              </li>
            </ul>
            <div class="nav_btn__box">
              <button class="vxod_btn btn">Вход в программу</button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "NavbarSection",
  mounted() {
    let header = document.querySelector(".header");
    document.addEventListener("scroll", (e) => {
      if (e.path[1].pageYOffset > 0) {
        header.style.position = "sticky";
      } else {
        header.style.position = "";
      }
    });
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
