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
      <section class="jumbotron d-flex justify-content-center align-items-center">
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
    </main>
  </div>
</template>

<script>
import RowMenu from './components/RowMenu.vue';


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
  }
}
</script>

<style lang="scss">
@import './assets/scss/style.scss';
</style>