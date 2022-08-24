<template>
  <div id="app">
    <!-- Header -->
    <header>
      <nav class="d-flex justify-content-between align-items-center">
        <div>
          <img src="./assets/img/theme_eduprime_logo.png" alt="EduPrime Logo">
        </div>
        <div class="d-flex align-items-center">
          <RowMenu :items="mainMenuItems" />
          <a class="btn-primary" id="header-button" href="#">VIEW COURSES</a>
        </div>
      </nav>
    </header>
    <!-- Main -->
    <main>
      <!-- Jumbotron section -->
      <section class="d-flex justify-content-center align-items-center" id="jumbotron">
        <div class="jumbo-content">
          <h2>Key to your success</h2>
          <p>EduPrime is the most versatile Wordpress theme for educational purposes, showcasing universities,
            courses,
            secondary schools etc.</p>
          <a class="btn-primary" href="#">
            <i class="fa-solid fa-magnifying-glass"></i>
            <span>Search courses</span>
          </a>
          <a class="btn-white" href="#">
            <i class="fa-solid fa-user-plus"></i>
            <span>Apply for university</span>
          </a>
        </div>
        <img src="./assets/img/Wave-1.png" alt="">
      </section>
      <!-- Browse courses section -->
      <section id="browse">
        <div class="container">
          <div class="row">
            <div class="col-6">
              <img class="books" src="./assets/img/Books-icon.png" alt="">
              <h3>Thousands of courses for any type of student</h3>
              <p>At EduPrime, it doesn’t matter what domain you wish to pursue a career in. Here you can find a course
                that
                satisfies your needs within a click away and applies for a course in a matter of minutes. EduPrime is
                ranked
                as the most versatile university in the world, thanks to the number of courses it provides.
              </p>
              <MainButton anchor="Browse through courses" url="#" scheme="regular" />
            </div>
            <div class="col-6 d-flex justify-content-center align-items-center">
              <img class="grad-hat" src="./assets/img/Graduation-Illustration.png" alt="">
            </div>
          </div>
        </div>
      </section>
      <!-- Faculties section -->
      <section id="faculties">
        <h3>Faculties available at EduPrime</h3>
        <p>A single university with a load of course, tailored to satisfy any student's needs.</p>
        <BoxesSlider />
      </section>

    </main>
  </div>
</template>

<script>
import RowMenu from './components/RowMenu.vue';
import MainButton from './components/MainButton.vue';
import BoxesSlider from './components/BoxesSlider.vue';


export default {
  name: 'App',
  data() {
    return {
      mainMenuItems: [
        {
          id: 1,
          anchor: 'Home',
          link: '#',
          sub: true,
        },
        {
          id: 2,
          anchor: 'Courses',
          link: '#',
          sub: true,
        },
        {
          id: 3,
          anchor: 'About Us',
          link: '#',
          sub: false,
        },
        {
          id: 4,
          anchor: 'News',
          link: '#',
          sub: true,
        },
        {
          id: 5,
          anchor: 'Pages',
          link: '#',
          sub: true,
        },
        {
          id: 6,
          anchor: 'Contact',
          link: '#',
          sub: false,
        },
        {
          id: 7,
          anchor: 'Purchase',
          link: '#',
          sub: false,
        },
      ]
    }
  },
  components: {
    RowMenu,
    MainButton,
    BoxesSlider,
  }
}
</script>

<style lang="scss">
@import './assets/scss/style.scss';
</style>