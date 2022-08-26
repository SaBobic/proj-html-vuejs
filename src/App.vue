<template>
  <div id="app">
    <MainHeader :main-menu-items="mainMenuItems" />
    <!-- Main -->
    <MainMain :faculties-slider-items="facultiesSliderItems" :events-items="eventsItems" :courses-items="coursesItems"
      :infos-items="infosItems" />
    <!-- Footer -->
    <MainFooter :categories-labels="CategoriesLabels" :get-edu-menu-items="getEduMenuItems"
      :networking-menu-items="NetworkingMenuItems" />
    <!-- Back to top arrow -->
    <aside :class="['c-pointer', { 'd-block': hasScrolled }]" @click="scrollToTop" id="back-to-top-arrow">
      <img src="./assets/img/back-to-top-arrow.svg" alt="Back to top arrow">
    </aside>
  </div>
</template>

<script>
import MainHeader from './components/MainHeader.vue';
import MainMain from './components/MainMain.vue';
import MainFooter from './components/MainFooter.vue';


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
          anchor: "Purchase Theme",
          url: "#",
        },
        {
          id: 2,
          anchor: "Our Benefits",
          url: "#",
        },
        {
          id: 3,
          anchor: "Our Team",
          url: "#",
        },
        {
          id: 4,
          anchor: "Our Services",
          url: "#",
        },
        {
          id: 5,
          anchor: "Other Products",
          url: "#",
        },
        {
          id: 6,
          anchor: "My account",
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
    MainHeader,
    MainFooter,
    MainMain,
  },
  methods: {
    toggleArrow() {
      if (window.scrollY > 700) {
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