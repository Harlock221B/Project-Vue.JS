<template>
  <div>
    <section id="panel_image">
      <header>
        <nav id="navigation" class="navbar navbar-expand-lg">
          <div class="container-fluid">
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
              <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                <li class="nav-item">
                  <a class="nav-link active" aria-current="page" href="#"
                    >Home</a
                  >
                </li>
                <li class="nav-item">
                  <a class="nav-link" href="#">Nossa História</a>
                </li>

                <li class="nav-item">
                  <a class="nav-link" href="#">Rede</a>
                </li>

                <li class="nav-item">
                  <a class="nav-link" href="#">Trabalhe conosco</a>
                </li>

                <li class="nav-item">
                  <a class="nav-link" href="#">Cardápio</a>
                </li>
              </ul>
              <img id="log" src="/images/ramen.svg" alt="" />
            </div>
          </div>
        </nav>
      </header>

      <main>
        <h1>{{ user.name }}, Bem vindo ao <br />Roberto Manshi!</h1>
        <br />
        <button v-on:click="reserva" id="Reserve">Reserve agora!</button>
      </main>
    </section>

    <section class="sectionIntermediate">
      <div class="card text-center">
        <div class="card-body">
          <h5 class="card-title">Tratamento Especial!</h5>
          <p class="card-text">
            O Manshi conquistou o 10º prêmio de Melhor Restaurante Japonês do
            guia "Comer & Beber" da Revista Veja Campinas em 2019. Além de
            típicas receitas japonesas a Casa oferece, também, especialidades
            diversificadas que permeiam referências tailandesas, chinesas, além
            de trazer aos pratos, elementos e temperos brasileiros. O espaço,
            moderno e descontraído, incorpora estilo e design para servir um
            completo bufê de almoço, festivais completos à noite, pratos à la
            carte, além de uma temakeria interna, sempre à disposição dos
            clientes.
          </p>
          <img src="/images/premium.jpg" alt="" />
          <img src="/images/premium2.jpg" alt="" />
        </div>
      </div>
    </section>

    <section id="foodCarousel">
      <div
        id="carouselExampleIndicators"
        class="carousel slide"
        data-bs-ride="carousel"
      >
        <div class="carousel-inner">
          <div v-for="image in images" :class="'carousel-item ' + image.active">
            <img :src="image.path" class="d-block w-100" :alt="image.name" />
          </div>
        </div>
        <button
          class="carousel-control-prev"
          type="button"
          data-bs-target="#carouselExampleIndicators"
          data-bs-slide="prev"
        >
          <span class="carousel-control-prev-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Previous</span>
        </button>
        <button
          class="carousel-control-next"
          type="button"
          data-bs-target="#carouselExampleIndicators"
          data-bs-slide="next"
        >
          <span class="carousel-control-next-icon" aria-hidden="true"></span>
          <span class="visually-hidden">Next</span>
        </button>
      </div>
    </section>
  </div>
</template>
<script>
export default {
  data() {
    return {
      user: {
        id: 1234,
        name: "Gabriel",
        age: 19,
      },
      images: [
        {
          name: "sushi",
          path: "/images/food1.jpg",
          active: "active",
        },
        {
          name: "Suco de cevada",
          path: "/images/food2.jpg",
          active: "",
        },
        {
          name: "shimeji",
          path: "/images/food3.jpg",
          active: "",
        },
        {
          name: "combo",
          path: "/images/food4.jpg",
          active: "",
        },
        {
          name: "garçon",
          path: "/images/food5.jpg",
          active: "",
        },
        {
          name: "sopa",
          path: "/images/food6.jpg",
          active: "",
        },
      ],
    };
  },
  methods: {
    reserva() {
      alert(this.user.name, ", Reserva Efetuada!");
    },
  },
};
</script>
