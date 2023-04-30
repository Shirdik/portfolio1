<template>
  <div class="bg-gray-200 px-12 pb-8" id="header">
    <NavBar :email="data.email" />
    <MyHeader :personal=data.personal :social="data.social" />
  </div>
  <div class="bg-gray-50 px-12 ">
    <MySkills :skills=data.skills />
    <MyExperience :experience=data.experience />
    <MyEducation :education=data.education />
    <MyProjects :projects=data.projects />
    <MyFooter :social="data.social" />
  </div>
  <!-- {{ data }} -->
</template>

<script>
import NavBar from './components/NavBar.vue';
import MyHeader from './components/MyHeader.vue';
import MySkills from './components/MySkills.vue';
import MyExperience from './components/MyExperience.vue';
import MyProjects from './components/MyProjects.vue';
import MyEducation from './components/MyEducation.vue';
import MyFooter from './components/MyFooter.vue';
import './output.css'

export default {
  name: 'App',
  components: {
    NavBar,
    MyHeader,
    MySkills,
    MyExperience,
    MyProjects,
    MyEducation,
    MyFooter
  },
  data() {
    return {
      data: {}
    }
  },
  methods: {
    async fetchBooks() {
      return await fetch("https://desolate-dawn-89646.herokuapp.com/api").then(res => res.json()).then(res => this.data = res.document);
    },
  },
  async created() {
    this.fetchBooks();
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Ysabeau:ital,wght@0,1;0,100;0,200;0,400;0,500;0,600;0,700;0,800;0,900;0,1000;1,1;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900;1,1000&display=swap');

body {
  scroll-behavior: smooth;
  font-family: 'Ysabeau', sans-serif;
}
</style>
