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
        <BoxesSlider :items="facultiesSliderItems" />
        <img src="./assets/svg/svg-0.svg" alt="">
      </section>
      <div class="danger-wrapper">
        <!-- University Year section -->
        <section id="year">
          <img class="icon" src="./assets/img/Clock-and-Bell.png" alt="">
          <h3>University Year</h3>
          <div>
            <img src="./assets/img/Timeline-Item.png" alt="">
            <div class="timeline-item-wrapper timeline-1">
              <h6>Orientation</h6>
              <p>First day of the university year, all students gather for the opening ceremony and then network with
                others.</p>
            </div>
            <div class="timeline-item-wrapper timeline-2">
              <h6>Demo Classes</h6>
              <p>In the first week, students try to accommodate with the teaching style and choose their optional
                courses.</p>
            </div>
            <div class="timeline-item-wrapper timeline-3">
              <h6>Evaluation</h6>
              <p>At the end of a semester, students take a general evaluation test for every subject they’re learning.
              </p>
            </div>
            <div class="timeline-item-wrapper timeline-4">
              <h6>Graduation Day</h6>
              <p>On the day of graduation, all students gather for the ceremony and then network and party among others.
              </p>
            </div>
          </div>
        </section>
        <!-- Upcoming Events section -->
        <section id="upcoming">
          <img class="icon" src="./assets/img/upcoming-events-calendar-icon.png" alt="">
          <h3>Upcoming Events</h3>
        </section>
      </div>
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
      ],
      facultiesSliderItems: [
        {
          id: 1,
          icon: 'Gavel-v2.png',
          img: 'Gavel-Illustration-e1556884768193.png',
          title: 'Law Faculty',
          text: 'Learning from world-leading academics and practitioners, you’ll not only receive an outstanding grounding in the theory of law, but you will be able to understand how those principles are applied in practice through a range of student-led activities and competitions.',
          url: '#',
        },
        {
          id: 2,
          icon: 'Coins-tabs-v2.png',
          img: 'Economy.png',
          title: 'Economy',
          text: 'Economics focuses on the behaviour and interactions of economic agents and how economies work. Microeconomics analyzes basic elements in the economy, including individual agents and markets, their interactions, and the outcomes of interactions, including unemployment of resource.',
          url: '#',
        },
        {
          id: 3,
          icon: 'Medicine-tabs-v2.png',
          img: 'Medicine.png',
          title: 'Medicine',
          text: 'Medicine is the science and practice of establishing the diagnosis, prognosis, treatment, and prevention of disease. Medicine encompasses a variety of health care practices evolved to maintain and restore health by the prevention and treatment of illness.',
          url: '#',
        },
        {
          id: 4,
          icon: 'Computer-tabs-v2.png',
          img: 'Computer-Science.png',
          title: 'Computer Science',
          text: 'Computer science is the study of processes that interact with data and that can be represented as data in the form of programs. It enables the use of algorithms to manipulate, store, and communicate digital information. A computer scientist studies the theory of computation software systems.',
          url: '#',
        },
        {
          id: 5,
          icon: 'Palette-tabs-v2.png',
          img: 'Graphic-Design.png',
          title: 'Graphic Design',
          text: 'Graphic design is the process of visual communication and problem-solving through the use of typography, photography and illustration. The field is considered a subset of visual communication and communication design, but sometimes the term ``graphic design`` is used synonymously.',
          url: '#',
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