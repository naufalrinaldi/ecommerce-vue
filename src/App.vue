<template>
<html>
<body>
    <div class="my-jumbotron" id="my-jumbotron">
<nav class="navbar ml-auto navbar-expand-lg navbar-default fixed-top raja-nav">
    <a class="navbar-brand" href="#">ATHLETA</a>
    <button class="navbar-toggler custom-toggler float-xs-left" type="button" data-toggle="collapse" data-target="#menu-raja" aria-controls="menu-raja" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
      </button>

  <div class="collapse navbar-collapse" id="menu-raja">
    <ul class="navbar-nav mr-auto mt-2 mt-lg-0 kiri">
      <li class="nav-item active">
        <a class="nav-link" href="#">Home</a>
      </li>
      <li class="nav-item active">
        <a class="nav-link" href="#">Blog</a>
      </li>
      <li class="nav-item active">
        <a class="nav-link" href="#">About Us</a>
      </li>
    </ul>
    <ul class="navbar-nav my-2 my-lg-0 kanan">
      <li class="nav-item mx-3  ">
        <a class="nav-link" href=""><img src="/pictures/user.svg" width="20px" height="20px"/></a>
      </li>
      <li class="nav-item mx-2">
        <a class="nav-link" href=""><img src="/pictures/shopping-cart.svg" width="20px" height="20px"/></a>
      </li>
    </ul>
  </div>
</nav>
        <!-- banner -->
        <div>
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="4000"
      controls
      indicators
      background="#ababab"
      img-width="1920"
      img-height="1080"
      style="text-shadow: 1px 1px 2px #333;"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <!-- Text slides with image -->
      <b-carousel-slide img-src="/pictures/banner1.jpg">
        <div class="container text-center" id="jumbo-text-contain">
            <h4 class="display-2 mt-5">Welcome To Athleta !</h4>
            <p class="lead">FASHION START FROM HERE</p>
            <button type="button" class="btn" id="jumbotron-btn">SHOP NOW !</button>
        </div>
      </b-carousel-slide>

      <!-- Slides with custom text -->
      <b-carousel-slide img-src="/pictures/banner2.jpg">
        <div class="container text-center" id="jumbo-text-contain">
            <h4 class="display-2 mt-5">Welcome To Athleta !</h4>
            <p class="lead">FASHION START FROM HERE</p>
            <button type="button" class="btn" id="jumbotron-btn">SHOP NOW !</button>
        </div>
      </b-carousel-slide>

      <!-- Slides with image only -->
      <b-carousel-slide img-src="/pictures/banner3.jpg">
        <div class="container text-center" id="jumbo-text-contain">
            <h4 class="display-2 mt-5">Welcome To Athleta !</h4>
            <p class="lead">FASHION START FROM HERE</p>
            <button type="button" class="btn" id="jumbotron-btn">SHOP NOW !</button>
        </div>
      </b-carousel-slide>
    </b-carousel>
  </div>
    </div>
<div id="category-sect">
    <h4 class="font-weight-bold pt-5 text-center"> Shop By Category </h4>
      <section id="tabs" class="project-tab">
        <div class="container-fluid">
            <div class="row justify-content-center">
                <div class="col-md-12">
                    <b-tabs content-class="mt-3" fill>
                    <b-tab title="Man" active>
                    <ul class="container mt-4">
                          <div class="row">
                        <div v-for="(man, index) in mans" :key="index" class="my-3 mr-2 text-center">
                          <div class="product-image">
                            <img :src="/pictures/ + fileman + index + filetype" class="img-responsive h-100 w-100 "/>
                            </div>
                          <div class="product-details">
                            <h6 class="display-6 mt-3">{{ man.name }}</h6>
                            <h6 class="display-6 text-muted">Rp.{{ man.price }}</h6>
                          </div>
                        </div>
                    </div>
                    </ul>
                    </b-tab>
                    <b-tab title="Woman">
                      <ul class="container mt-4">
                          <div class="row">
                        <div v-for="(woman, index) in womans" :key="index" class="my-3 mr-2 text-center">
                          <div class="product-image">
                            <img :src="/pictures/ + filewomen + index + filetype" class="img-responsive h-100 w-100"/>
                            </div>
                          <div class="product-details">
                            <h6 class="display-6 mt-3">{{ woman.name }}</h6>
                            <h6 class="display-6 text-muted">Rp.{{ woman.price }}</h6>
                          </div>
                        </div>
                    </div>
                    </ul>
                      </b-tab>
                    <b-tab title="Accecories">
                      <ul class="container mt-4">
                          <div class="row">
                        <div v-for="(accecories, index) in accecoriess" :key="index" class="my-3 mr-2 text-center">
                          <div class="product-image">
                            <img :src="/pictures/ + fileacc + index + filetype" class="img-responsive h-100 w-100 "/>
                            </div>
                          <div class="product-details">
                            <h6 class="display-6 mt-3">{{ accecories.name }}</h6>
                            <h6 class="display-6 text-muted">Rp.{{ accecories.price }}</h6>
                          </div>
                        </div>
                    </div>
                    </ul>
                    </b-tab>
                  </b-tabs>

                    </div>
                </div>
            </div>
            </section>
        </div>
</body>
<footer class="page-footer blue pt-5 mt-5">
<div class="container-fluid text-center text-md-left">
      <div class="row">
        <div class="col-md-6 mt-md-0 mt-3">
          <img class="px-5 w-50 my-3" src="/pictures/gray.png" />
          <p class="text-md-left px-5">Athleta adalah salah satu perusahaan mode internasional terbesar. Perusahaan ini dimiliki oleh Paltex, salah satu grup distribusi terbesar di dunia. Pelanggan adalah bagian terpenting dalam model bisnis kami, yang mencakup desain, produksi, distribusi, dan penjualan melalui jaringan ritel kami yang luas.</p>

        </div>

        <hr class="clearfix w-100 d-md-none pb-3">
        <div class="col-md-3 mb-md-0 mb-3">

          <h5 class="text-uppercase">Layanan Kami</h5>

          <ul class="list-unstyled">
            <li>
              <a href="#!">Link 1</a>
            </li>
            <li>
              <a href="#!">Link 2</a>
            </li>
            <li>
              <a href="#!">Link 3</a>
            </li>
            <li>
              <a href="#!">Link 4</a>
            </li>
          </ul>

        </div>
        <div class="col-md-3 mb-md-0 mb-3">

          <h5 class="text-uppercase">TENTANG KAMi</h5>

          <ul class="list-unstyled">
            <li>
              <a href="#!">Link 1</a>
            </li>
            <li>
              <a href="#!">Link 2</a>
            </li>
            <li>
              <a href="#!">Link 3</a>
            </li>
            <li>
              <a href="#!">Link 4</a>
            </li>
          </ul>

        </div>

      </div>

    </div>

    <div class="footer-copyright text-right py-3 mr-3">© 2020 Copyright:
      <p> Rueve</p>
    </div>
  </footer>

</html>
  <!-- <div id="app">
    <h1 v-for="(shirt, index) in shirts" :key="index">{{ shirt.name }}</h1>
    <h1 v-for="(tshirt, index) in tshirts" :key="index">{{ tshirt.price }}</h1>
    </div> -->
</template>

<script>
import axios from 'axios'
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

export default {
  name: 'App',
  data () {
    return {
      slide: 0,
      sliding: null,
      fileman: 'man',
      filewomen: 'woman',
      fileacc: 'a',
      filetype: '.jpg',
      mans: [],
      womans: [],
      accecoriess: []
    }
  },
  async created () {
    const baseURI = 'https://my-json-server.typicode.com/naufalrinaldi/ecommerce-vue/db'
    axios.get(baseURI)
      .then((result) => {
        this.mans = result.data.mans
        this.womans = result.data.womans
        this.accecoriess = result.data.accecoriess
      })
  }
}

</script>

<style>
@media (min-width: 992px) {
      .navbar-brand {
        position: absolute;
        left: 50%;
        transform: translateX(-50%);
        font-family: "Poppins",sans-serif;
        color: #23232c;
        letter-spacing: 2.5px;
      }
    }
    .kiri {
      margin-left: 40px;
    }
    .kanan {
      margin-right: 40px;
    }
    @media (max-width: 991px) {
      .navbar-brand {
        height: 0;
        margin-top: -90px;
        left: 10%;
      }
      .navbar-nav{
        margin-top: 10px;
        margin-left: 40%;
      }
    }
    .raja-nav{
      background-color: white;
      padding-top: 25px;
      padding-bottom: 25px;
      font-family: Laila, serif;
      font-size: 1.2rem;
      color: #23232c;
      font-weight: 600;
      text-transform: uppercase;
    }
    .navbar-nav > li > a:hover {
      /*  */
    }
    .navbar-toggler-icon {
      background-image: url("data:image/svg+xml;charset=utf8,%3Csvg viewBox='0 0 32 32' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath stroke='rgba(34, 155, 168, 1)' stroke-width='2' stroke-linecap='round' stroke-miterlimit='10' d='M4 8h24M4 16h24M4 24h24'/%3E%3C/svg%3E");
    }
    .navbar-nav > li{
      margin-right: 20px;
    }
    .navbar-nav > li > a{
      color: #23232c;
      font-size: 14px;
      font-family: "Poppins",sans-serif;
    }
    .navbar-toggler {
      margin-left: 90%;
    }

    /* .carousel-item {
      height: 100vh;
      min-height: 350px;
      background: no-repeat center center scroll;
      -webkit-background-size: cover;
      -moz-background-size: cover;
      -o-background-size: cover;
      background-size: cover;
    } */
    .img-carousel {
      object-fit: cover;
      height: 100%;
    }

    .carousel-caption{
      top: 50%;
      transform: translateY(-50%);
      margin-top: 3%;
      color: whitesmoke;
    }

#my-jumbotron {
    /* background-image: url("/pictures/banner1.jpg"); */
    background-size: cover;
    overflow: hidden;
}
/* #jumbo-text-contain {
      top: 25%;
      transform: translateY(-50%);
      margin-top: 3%;
      color: whitesmoke;
} */
#jumbotron-btn {
    font-size: 20px;
    border: 3px solid ;
    border-radius: 0;
    transition: 0.3s;
}
#jumbotron-btn:hover {
    color:white ;
    border: 1px solid white;
}
#products-container li{
    list-style-type: none;
    height: 250px;
}
.product-image {
    background: #f4f4ef;
    width: 250px;
    height: 370px;
    margin-right: 10px;
    transition: 0.7s ease-in-out;
}
.product-image:hover {
  box-shadow: 0px 4px 8px 0px rgba(0, 0, 0, 2);
}
.project-tab {
    padding: 10%;
    margin-top: -8%;
}
.project-tab #tabs{
    background: #007b5e;
    color: #eee;
}
.project-tab #tabs h6.section-title{
    color: #eee;
}
.project-tab #tabs .nav-tabs .nav-item.show .nav-link, .nav-tabs .nav-link.active {
    color: #eee;
    background-color: transparent;
    border-color: transparent transparent #f3f3f3;
    border-bottom: 3px solid !important;
    font-size: 16px;
    font-weight: bold;
}
.project-tab .nav-link {
    border: 1px solid transparent;
    border-top-left-radius: .25rem;
    border-top-right-radius: .25rem;
    color: #acbebe;
    font-size: 16px;
    font-weight: 600;
}
.project-tab .nav-link:hover {
    border: none;
}
.project-tab thead{
    background: #f3f3f3;
    color: #eee;
}
.project-tab a{
    text-decoration: none;
    color: #eee;
    font-weight: 600;
}
.page-footer {
    color: white;
    background: #80c5c2;
}
.row{
  justify-content: center;
}
</style>
