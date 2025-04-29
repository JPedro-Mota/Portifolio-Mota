<template>
  <div class="background-container">
    <video autoplay class="background-video" loop muted>
      <source src="../assets/abstract-twist-wave-colorful-moewalls-com.mp4">
      Seu navegador não suporta vídeos em MP4.
    </video>

    <div class="content">
      <NavBar />

      <div class="main-section">
        <div class="text">
          <p class="title">João Pedro</p>
          <p class="description">
            Olá, sou o João Pedro, desenvolvedor Full-Stack. Atualmente trabalho com Vue.js, Quasar, Java SpringBoot, desenvolvendo aplicações web funcionais e eficientes.
          </p>

          <div class="buttons">
            <button class="btn-contact">Contatos</button>
            <button class="btn-exp">Experiências</button>
          </div>

          <div class="social-icons">
            <a href="https://github.com/JPedro-Mota" target="_blank">
              <v-icon icon="mdi-github" />
            </a>
            <a href="https://www.linkedin.com/in/seulinkedin" target="_blank">
              <v-icon icon="mdi-linkedin" />
            </a>
            <a href="mailto:seuemail@exemplo.com">
              <v-icon icon="mdi-email" />
            </a>
          </div>
        </div>

        <div class="profile-img">
          <img src="../assets/image.png">
        </div>
      </div>

      <p class="title-about">Sobre Mim</p>

      <v-container class="cards-row" fluid>
        <v-row>
          <p class="text-about">
            I'm a passionate fullstack developer with 5+ years of experience building web applications. I specialize in JavaScript, React, Node.js, and modern web technologies.
            My journey in software development started when I built my first website at 15. Since then, I've worked with startups and established companies to create efficient, scalable, and user-friendly applications.
            When I'm not coding, you can find me hiking, reading tech blogs, or contributing to open-source projects. I'm always looking to learn new technologies and improve my skills.
          </p>
          <v-col cols="12" md="5">
            <v-container class="cards-container" fluid>
              <v-row class="cards-row" justify="center">
                <v-col
                  v-for="(card, i) in cards"
                  :key="i"
                  cols="12"
                  md="6"
                  sm="6"
                >
                  <v-card
                    class="pa-4 rounded-xl text-white card-elevation d-flex flex-column fill-height"
                    :class="card.color"
                  >
                    <div class="icon mb-4">
                      <v-icon size="36">{{ card.icon }}</v-icon>
                    </div>
                    <h3 class="font-weight-bold text-h6">{{ card.title }}</h3>
                    <p class="text-body-2">{{ card.text }}</p>
                  </v-card>
                </v-col>
              </v-row>
            </v-container>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script lang="ts" setup>
  import NavBar from '@/components/NavBar.vue';

  const cards = [
    {
      icon: 'mdi-monitor',
      title: 'Frontend Development',
      text: 'Creating responsive and interactive user interfaces with modern frameworks',
      color: 'card-dark',
    },
    {
      icon: 'mdi-server',
      title: 'Backend Development',
      text: 'Building scalable APIs and server-side logic with Java Spring Boot',
      color: 'card-dark',
    },
    {
      icon: 'mdi-database',
      title: 'Database Design',
      text: 'Designing efficient data structures and managing PostgreSQL & MySQL',
      color: 'card-dark',
    },
    {
      icon: 'mdi-cloud',
      title: 'DevOps & Deployment',
      text: 'CI/CD pipelines and cloud deployment on services like Heroku or Docker',
      color: 'card-dark',
    },
  ];
</script>

<style scoped>
html,
body {
  height: 100%;
  margin: 0;
  padding: 0;
  overflow-x: hidden;
}

.background-container {
  position: relative;
  width: 100%;
  min-height: 100vh;
  height: auto;
  overflow-y: auto;
  color: white;
  font-family: 'Gruppo', sans-serif;
}

.background-video {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  filter: opacity(40%);
  z-index: 0;
}

.content {
  position: relative;
  z-index: 1;
}

.main-section {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 5% 10%;
}

.about-section {
  display: flex;
  flex-wrap: wrap;
  padding: 5% 10%;
}

.text {
  max-width: 50%;
}

.title {
  font-size: 72px;
  margin-bottom: 20px;
}

.title-about {
  font-size: 62px;
  margin-bottom: 2vh;
  text-align: center;
  margin-top: 5%;
}

.text-about {
  width: 100vh ;
  margin: 40px;
  font-size: 22px;
  line-height: 1.6;
}

.description {
  font-size: 20px;
  margin-bottom: 30px;
  line-height: 1.5;
}

.buttons {
  display: flex;
  gap: 10px;
  margin-bottom: 20px;
}

.btn-contact,
.btn-exp {
  padding: 10px 20px;
  border: none;
  border-radius: 20px;
  font-size: 16px;
  cursor: pointer;
  transition: 0.3s ease;
}

.btn-contact {
  background: #4ecdc4;
  color: black;
}

.btn-exp {
  background: transparent;
  color: white;
  border: 1px solid #aaa;
}

.btn-exp:hover,
.btn-contact:hover {
  opacity: 0.8;
}

.social-icons {
  font-size: 22px;
  display: flex;
  gap: 15px;
}

.profile-img img {
  border-radius: 50%;
  width: 250px;
  height: 250px;
  object-fit: cover;
  border: 4px solid white;
  box-shadow: 0 0 20px rgba(255, 255, 255, 0.2);
}

.card-dark {
  background-color: #1e1e2f;
}

/* Responsivo */
@media (max-width: 768px) {
  .main-section {
    flex-direction: column;
    align-items: center;
    text-align: center;
    padding: 5% 5%;
  }

  .text {
    max-width: 90%;
  }

  .profile-img {
    margin-top: 30px;
  }

  .text-about {
    width: 90%;
    margin: 0 auto;
  }
}
</style>
