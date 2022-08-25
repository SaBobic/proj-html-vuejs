<template>
  <div id="app">
    <!-- Header -->
    <header>
      <nav class="d-flex justify-content-between align-items-center">
        <div>
          <BaseLogo />
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
              <MainButton anchor="Browse through courses" url="#" scheme="regular success" />
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
        <svg version="1.0" xmlns="http://www.w3.org/2000/svg" width="2954.667" height="186.667" viewBox="0 0 2216 140">
          <path class="st0"
            d="M324.7 34.8c-76.4 51.8-134.1 82-177.2 92.8-12.2 3.1-33.8 4.3-42.8 2.5-8.1-1.7-18.5-7.2-24.2-12.8-5.7-5.7-10.1-12.2-17.4-26.1C57 79.6 52.6 75 47.7 75c-7.9 0-21.2 9.9-37.9 28.3L0 114v26h1105.2c729.3 0 1104.9-.3 1104.2-1-2.6-2.6-29.5-18-42.9-24.5-46.4-22.7-82.1-27.7-122.7-17.5-4.6 1.2-19.1 5.5-32.3 9.5-40.2 12.4-58.5 16.1-85.5 17.2-33.9 1.3-73.5-5.3-117.9-19.9-14.8-4.8-48.5-17.8-59.7-23l-5.2-2.4-16.3 1.8c-125.9 13.6-219.6 20.5-324.9 23.9-40.1 1.3-166.2.6-196-1-71.9-4-119.7-8.4-173.5-16.2-26.8-3.8-69.6-11.2-83.1-14.4-5-1.1-8-1.3-13.2-.5-3.7.5-18.8 2.3-33.7 3.9C793 88.1 702 89.1 622 79c-51.2-6.5-89.6-15.2-150.5-34-35.4-10.9-84.3-20.7-121.8-24.3-3.5-.3-5.6.9-25 14.1z"
            fill="#20AD96" />
        </svg>
      </section>
      <!-- University Year section -->
      <section class="bg-danger" id="year">
        <div>
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
        </div>
      </section>
      <!-- Upcoming Events section -->
      <section class="bg-danger" id="upcoming">
        <div>
          <img class="icon" src="./assets/img/upcoming-events-calendar-icon.png" alt="">
          <h3>Upcoming Events</h3>
          <EventsCards btn-url="#" :items="eventsItems" />
        </div>
      </section>
      <svg version="1.0" xmlns="http://www.w3.org/2000/svg" width="2821.333" height="177.333" viewBox="0 0 2116 133">
        <path class="st0"
          d="M6 .4c0 .8 22.8 14.1 35.5 20.7 35.6 18.6 68.6 26.7 96.8 23.9 15.1-1.5 29.4-4.8 54.3-12.6 40-12.5 57.6-16.1 84.4-17.1 45.6-1.6 98.7 10.6 160.6 37.1 7.1 3.1 14.2 5.6 15.8 5.6 1.5 0 17.3-1.6 35-3.5 85-9.2 166.6-15.4 259.1-19.7 36.9-1.7 181.6-1.7 215 0 89.4 4.7 163.2 12.9 226.5 25.4 13.3 2.6 24.2 4.3 28.5 4.2 3.9 0 19.4-1.4 34.5-3.2 60.9-7 102.4-9.6 157-9.6 94.2 0 162.8 9.8 244 34.9 44.3 13.6 79.7 21.3 119.4 25.9l13 1.5 30.5-20.3c85.2-56.8 141.9-83.5 181.6-85.3 28.4-1.3 43 7.9 57 35.7 7.9 15.7 12 19.4 19.5 17.1 6.8-2 15.6-8.9 28.9-22.7l13.1-13.6V0H1061C480.8 0 6 .2 6 .4z"
          fill="#20AD96" />
      </svg>
      <!-- Courses section -->
      <section class="container" id="courses">
        <h3>Latest Courses</h3>
        <CoursesCards :items="coursesItems" />
      </section>
      <!-- Infos section -->
      <section class="container" id="infos">
        <FloatingJumbo :items="infosItems" />
      </section>
      <!-- Newsletter section -->
      <section id="newsletter">
        <div class="container">
          <div class="row">
            <div class="col-7 newsletter-text">Subscribe Now to Our Newsletter!</div>
            <div class="col-5 newsletter-input">
              <BaseInput placeholder="Email address..." icon="fa-paper-plane" />
            </div>
          </div>
        </div>
      </section>
      <!-- Partners section -->
      <section id="partners">
        <div class="container text-center">
          <h3>Partners</h3>
          <p>Leverage agile frameworks to provide a robust synopsis for high level overviews. Iterative approaches to
            corporate strategy.
          </p>
          <div>
            <img class="c-pointer" src="./assets/img/partner-1.png" alt="">
            <img class="c-pointer" src="./assets/img/partner-2.png" alt="">
            <img class="c-pointer" src="./assets/img/partner-3.png" alt="">
            <img class="c-pointer" src="./assets/img/partner-4.png" alt="">
            <img class="c-pointer" src="./assets/img/partner-5.png" alt="">
            <img class="c-pointer" src="./assets/img/partner-6.png" alt="">
            <img class="c-pointer" src="./assets/img/partner-7.png" alt="">
            <img class="c-pointer" src="./assets/img/partner-8.png" alt="">
          </div>
        </div>
        <div id="partners-bg-img">
        </div>
      </section>
    </main>
    <!-- Footer -->
    <footer id="footer">
      <nav class="container">
        <div class="row">
          <div class="col-4">
            <BaseLogo />
            <p class="footer-text">EduPrime is the most versatile WordPress theme for educational purposes, showcasing
              universities, courses, secondary schools etc.
            </p>
            <SocialLabels />
          </div>
          <div class="col-4">
            <div class="row">
              <div class="col">
                <VerticalMenu title="GetEduPrime" :items="getEduMenuItems" />
              </div>
              <div class="col">
                <VerticalMenu title="Networking" :items="NetworkingMenuItems" />
              </div>
            </div>
          </div>
          <div class="col-4 text-end">
            <BaseInput class="mb-4" placeholder="Search..." icon="fa-magnifying-glass" />
            <SearchWithLabels title="Search categories" :items="CategoriesLabels" class="mb-3" />
            <div class="text-primary">ModelTheme. All rights reserved.</div>
          </div>
        </div>
      </nav>
    </footer>
    <!-- Back to top arrow -->
    <aside :class="['c-pointer', { 'd-block': hasScrolled }]" ref="arrow" @click="scrollToTop" id="back-to-top-arrow">
      <img src="./assets/img/back-to-top-arrow.svg" alt="">
    </aside>
    <!-- Theme info label -->
    <aside id="theme-info">
      <a href="#"><i class="fa-solid fa-cart-shopping"></i></a>
      <a href="#"><i class="fa-solid fa-book-open"></i></a>
      <a href="#"><i class="fa-solid fa-life-ring"></i></a>
    </aside>
  </div>
</template>

<script>
import RowMenu from './components/RowMenu.vue';
import MainButton from './components/MainButton.vue';
import BoxesSlider from './components/BoxesSlider.vue';
import EventsCards from './components/EventsCards.vue';
import CoursesCards from './components/CoursesCards.vue';
import FloatingJumbo from './components/FloatingJumbo.vue';
import BaseInput from './components/BaseInput.vue';
import VerticalMenu from './components/VerticalMenu.vue';
import BaseLogo from './components/BaseLogo.vue';
import SearchWithLabels from './components/SearchWithLabels.vue';
import SocialLabels from './components/SocialLabels.vue';


export default {
  name: "App",
  data() {
    return {
      hasScrolled: false,
      mainMenuItems: [
        {
          id: 1,
          anchor: "Home",
          link: "#",
          sub: true,
        },
        {
          id: 2,
          anchor: "Courses",
          link: "#",
          sub: true,
        },
        {
          id: 3,
          anchor: "About Us",
          link: "#",
          sub: false,
        },
        {
          id: 4,
          anchor: "News",
          link: "#",
          sub: true,
        },
        {
          id: 5,
          anchor: "Pages",
          link: "#",
          sub: true,
        },
        {
          id: 6,
          anchor: "Contact",
          link: "#",
          sub: false,
        },
        {
          id: 7,
          anchor: "Purchase",
          link: "#",
          sub: false,
        },
      ],
      facultiesSliderItems: [
        {
          id: 1,
          icon: "Gavel-v2.png",
          img: "Gavel-Illustration-e1556884768193.png",
          title: "Law Faculty",
          text: "Learning from world-leading academics and practitioners, you’ll not only receive an outstanding grounding in the theory of law, but you will be able to understand how those principles are applied in practice through a range of student-led activities and competitions.",
          url: "#",
        },
        {
          id: 2,
          icon: "Coins-tabs-v2.png",
          img: "Economy.png",
          title: "Economy",
          text: "Economics focuses on the behaviour and interactions of economic agents and how economies work. Microeconomics analyzes basic elements in the economy, including individual agents and markets, their interactions, and the outcomes of interactions, including unemployment of resource.",
          url: "#",
        },
        {
          id: 3,
          icon: "Medicine-tabs-v2.png",
          img: "Medicine.png",
          title: "Medicine",
          text: "Medicine is the science and practice of establishing the diagnosis, prognosis, treatment, and prevention of disease. Medicine encompasses a variety of health care practices evolved to maintain and restore health by the prevention and treatment of illness.",
          url: "#",
        },
        {
          id: 4,
          icon: "Computer-tabs-v2.png",
          img: "Computer-Science.png",
          title: "Computer Science",
          text: "Computer science is the study of processes that interact with data and that can be represented as data in the form of programs. It enables the use of algorithms to manipulate, store, and communicate digital information. A computer scientist studies the theory of computation software systems.",
          url: "#",
        },
        {
          id: 5,
          icon: "Palette-tabs-v2.png",
          img: "Graphic-Design.png",
          title: "Graphic Design",
          text: "Graphic design is the process of visual communication and problem-solving through the use of typography, photography and illustration. The field is considered a subset of visual communication and communication design, but sometimes the term ``graphic design`` is used synonymously.",
          url: "#",
        },
      ],
      eventsItems: [
        {
          id: 1,
          title: "Coaching Sessions",
          date: "20 May 21:30 PM",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor[...]",
          url: "#",
        },
        {
          id: 2,
          title: "Coaching Sessions",
          date: "24 Mar 18:00 PM",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor[...]",
          url: "#",
        },
        {
          id: 3,
          title: "Coaching Sessions",
          date: "12 Feb 13:30 PM",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor[...]",
          url: "#",
        },
      ],
      coursesItems: [
        {
          id: 1,
          icon: "Decisions-icon.png",
          name: "Make Better Decisions",
          teacher: "James Colins",
          price: "$21.00",
          url: "#",
        },
        {
          id: 2,
          icon: "Speaker-icon.png",
          name: "How to be a speaker",
          teacher: "James Colins",
          price: "Free",
          url: "#",
        },
        {
          id: 3,
          icon: "Network-icon.png",
          name: "Network Introductions",
          teacher: "James Colins",
          price: "Free",
          url: "#",
        },
        {
          id: 4,
          icon: "Brand-icon.png",
          name: "Brand Management",
          teacher: "James Colins",
          price: "Free",
          url: "#",
        },
      ],
      infosItems: [
        {
          id: 1,
          direction: true,
          icon: "Exam-icon.png",
          img: "Exam-Illustration.png",
          title: "The most efficient examination method",
          text: "EduPrime has gathered teachers from around the globe to brainstorm in order to facilitate the evaluation of our students. Every teacher from our university has an influence on how students are evaluated at his/her subject.",
          anchor: "Discover the Method",
          url: "#",
        },
        {
          id: 2,
          direction: false,
          icon: "Exam-icon-1.png",
          img: "Girl-Illustration.png",
          title: "Variable fees for international students",
          text: "EduPrime has gathered teachers from around the globe to brainstorm in order to facilitate the evaluation of our students. Every teacher from our university has an influence on how students are evaluated at his/her subject.",
          anchor: "List of fees",
          url: "#",
        },
      ],
      getEduMenuItems: [
        {
          id: 1,
          anchor: "Request a website",
          url: "#",
        },
        {
          id: 2,
          anchor: "Browse Themes",
          url: "#",
        },
        {
          id: 3,
          anchor: "Payment options",
          url: "#",
        },
        {
          id: 4,
          anchor: "Support System",
          url: "#",
        },
        {
          id: 5,
          anchor: "Checkout",
          url: "#",
        },
        {
          id: 6,
          anchor: "Purchase Theme",
          url: "#",
        },
      ],
      NetworkingMenuItems: [
        {
          id: 1,
          anchor: "Request a website",
          url: "#",
        },
        {
          id: 2,
          anchor: "Browse Themes",
          url: "#",
        },
        {
          id: 3,
          anchor: "Payment options",
          url: "#",
        },
        {
          id: 4,
          anchor: "Support System",
          url: "#",
        },
        {
          id: 5,
          anchor: "Checkout",
          url: "#",
        },
        {
          id: 6,
          anchor: "Purchase Theme",
          url: "#",
        },
      ],
      CategoriesLabels: [
        {
          id: 1,
          anchor: "Economy",
          url: "#",
        },
        {
          id: 2,
          anchor: "Design",
          url: "#",
        },
        {
          id: 3,
          anchor: "Coaching",
          url: "#",
        },
        {
          id: 4,
          anchor: "Business",
          url: "#",
        },
        {
          id: 5,
          anchor: "Medicine",
          url: "#",
        },
        {
          id: 6,
          anchor: "Law",
          url: "#",
        },
        {
          id: 7,
          anchor: "Fitness",
          url: "#",
        },
      ],
    };
  },
  components: {
    BaseLogo,
    RowMenu,
    MainButton,
    BoxesSlider,
    EventsCards,
    CoursesCards,
    FloatingJumbo,
    BaseInput,
    VerticalMenu,
    SearchWithLabels,
    SocialLabels
  },
  methods: {
    toggleArrow() {
      if (window.scrollY > 300) {
        this.hasScrolled = true;
      } else {
        this.hasScrolled = false;
      }
    },
    scrollToTop() {
      window.scrollTo({ top: 0 })
    }
  },
  mounted() {
    window.addEventListener('scroll', this.toggleArrow);
  }
}
</script>

<style lang="scss">
@import './assets/scss/style.scss';
</style>