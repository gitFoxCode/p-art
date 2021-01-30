<template>
  <svg-sprite />
  <Nav />
  <swiper
    :direction = "DirectionOptions"
    :slides-per-view = "1"
    :space-between = "0"
    :mousewheel = "true"
    :hashNavigation = "hashOptions"
    :scrollbar = "ScrollbarOptions"
    class="projects">
    <swiper-slide
      v-for="(project, index) in projects"
      :key="project.id"
      :virtualIndex="index"
      :data-hash="'project-' + project.id"
      class="project"
      >
      <span class="project__badge">
        {{ project.category }}
      </span>
      <h1 class="project__title"> {{ project.title }} </h1>
      <div class="project__info">
        <p class="project__description">{{ project.description }}</p>
        <div class="project__info__date">
          <div class="column">
            <span class="column__title">
              Date
            </span>
            <span class="column__value">
              {{ project.date }}
            </span>
          </div>
          <div class="column">
            <span class="column__title">
              Time
            </span>
            <span class="column__value">
              {{ project.time }}
            </span>
          </div>
        </div>
      </div>
      <button type="button" class="project__button">Follow me</button>
      <img :src="project.img">
      <footer class="project__footer">
        <span class="footer__text">
          &copy; 2020 All Rights Reserved
        </span>
        <div class="footer__socials">
          <span class="footer__text">Share</span>
          <span class="footer__line"></span>
          <svg-icon icon="facebook" />
          <svg-icon icon="instagram" />
          <svg-icon icon="twitter" />
        </div>
      </footer>
      </swiper-slide> 
      <div class="swiper-scrollbar"></div>
  </swiper>
  
</template>

<script>
import Nav from "./components/Nav.vue";
import { Swiper, SwiperSlide } from 'swiper/vue';
import SwiperCore, { Navigation, HashNavigation, Mousewheel, Pagination, Scrollbar } from 'swiper';
import 'swiper/swiper.scss';
import 'swiper/components/navigation/navigation.scss';
import 'swiper/components/pagination/pagination.scss';
import 'swiper/components/scrollbar/scrollbar.scss';

SwiperCore.use([Navigation, HashNavigation, Mousewheel, Pagination, Scrollbar]);

export default {
  name: "App",
  components: {
    Swiper,
    SwiperSlide,
    Nav
  },
  data(){
    return { 
      hashOptions: {
        watchState: true
      },
      DirectionOptions: 'vertical',
      ScrollbarOptions: {
        el: '.swiper-scrollbar',
        dragSize: 100
      },
      projects: [
      {
        id: 1,
        category: "General category",
        title: "Digital Art",
        description: "For works created usign digital technology, whether in the form of tangible hardware, such as",
        date: "24.08.19",
        time: "14:22 PM",
        img: require('@/assets/projects/art-1.jpg')
      },
      {
        id: 2,
        category: "Roads",
        title: "Droga",
        description: "To jest obraz z drogą, cośtam coś lorem ipsum de solor cssaon msoaw mous el mirro.",
        date: "14.01.20",
        time: "12:33 PM",
        img: require('@/assets/projects/art-2.jpg')
      },
      {
        id: 3,
        category: "Kategoria here",
        title: "Tytul here",
        description: "Jakiś dłuższy opis here",
        date: "14.01.20",
        time: "12:33 PM",
        img: require('@/assets/projects/art-3.jpg')
      },
      {
        id: 4,
        category: "Kategoria here",
        title: "Tytul here",
        description: "Jakiś dłuższy opis here",
        date: "14.01.20",
        time: "12:33 PM",
        img: require('@/assets/projects/art-4.jpg')
      },
      {
        id: 5,
        category: "Kategoria here",
        title: "Tytul here",
        description: "Jakiś dłuższy opis here",
        date: "14.01.20",
        time: "12:33 PM",
        img: require('@/assets/projects/art-5.jpg')
      },
      {
        id: 6,
        category: "Kategoria here",
        title: "Tytul here",
        description: "Jakiś dłuższy opis here",
        date: "14.01.20",
        time: "12:33 PM",
        img: require('@/assets/projects/art-6.jpg')
      },
      {
        id: 7,
        category: "Kategoria here",
        title: "Tytul here",
        description: "Jakiś dłuższy opis here",
        date: "14.01.20",
        time: "12:33 PM",
        img: require('@/assets/projects/art-7.jpg')
      },
      {
        id: 8,
        category: "Kategoria here",
        title: "Tytul here",
        description: "Jakiś dłuższy opis here",
        date: "14.01.20",
        time: "12:33 PM",
        img: require('@/assets/projects/art-8.jpg')
      },
      {
        id: 9,
        category: "Kategoria here",
        title: "Tytul here",
        description: "Jakiś dłuższy opis here",
        date: "14.01.20",
        time: "12:33 PM",
        img: require('@/assets/projects/art-9.jpg')
      },
      {
        id: 10,
        category: "Kategoria here",
        title: "Tytul here",
        description: "Jakiś dłuższy opis here",
        date: "14.01.20",
        time: "12:33 PM",
        img: require('@/assets/projects/art-10.jpg')
      },
      {
        id: 11,
        category: "Kategoria here",
        title: "Tytul here",
        description: "Jakiś dłuższy opis here",
        date: "14.01.20",
        time: "12:33 PM",
        img: require('@/assets/projects/art-11.jpg')
      },
      {
        id: 12,
        category: "Kategoria here",
        title: "Tytul here",
        description: "Jakiś dłuższy opis here",
        date: "14.01.20",
        time: "12:33 PM",
        img: require('@/assets/projects/art-12.jpg')
      },
      {
        id: 13,
        category: "Kategoria here",
        title: "Tytul here",
        description: "Jakiś dłuższy opis here",
        date: "14.01.20",
        time: "12:33 PM",
        img: require('@/assets/projects/art-13.jpg')
      },
      {
        id: 14,
        category: "Kategoria here",
        title: "Tytul here",
        description: "Jakiś dłuższy opis here",
        date: "14.01.20",
        time: "12:33 PM",
        img: require('@/assets/projects/art-14.jpg')
      },
      {
        id: 15,
        category: "Kategoria here",
        title: "Tytul here",
        description: "Jakiś dłuższy opis here",
        date: "14.01.20",
        time: "12:33 PM",
        img: require('@/assets/projects/art-15.jpg')
      },
      {
        id: 16,
        category: "Kategoria here",
        title: "Tytul here",
        description: "Jakiś dłuższy opis here",
        date: "14.01.20",
        time: "12:33 PM",
        img: require('@/assets/projects/art-16.jpg')
      },
      {
        id: 17,
        category: "Kategoria here",
        title: "Tytul here",
        description: "Jakiś dłuższy opis here",
        date: "14.01.20",
        time: "12:33 PM",
        img: require('@/assets/projects/art-17.jpg')
      }
      ]
    }
  },
};
</script>

<style lang="scss">
  @import '~@/assets/css/reset.css';

  *,*::after,*::before{
    box-sizing: border-box;
  }
  html{
    scroll-behavior: smooth;
  }
  body{
    font-size: 18px;
    background-color: #081B29;
  }
  .projects{
    width: 100%;
    height: 100vh;
  }
  .project{
    height: 100vh;
    padding: 200px 10%;
    position: relative;
    overflow: hidden;
    z-index: 1;
    color: #fff;
    font-family: "Poppins", sans-serif;
    text-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1); 
  }
  .project img{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    object-fit: cover;
    z-index: -1;
  }
  .project__badge{
    letter-spacing: 0.5px;
  }
  .project__title{
    font-size: 3em;
    text-transform: uppercase;
    font-weight: bold;
    letter-spacing: 1px;
    margin-top: 20px;
    margin-bottom: 40px;
  }
  .project__description{
    max-width: 300px;
    line-height: 170%;
    font-weight: 300;
  }
  .project__info{
    display: flex;
    align-items: center;
  }
  .project__footer{
    position: absolute;
    display: flex;
    width: 600px;
    justify-content: space-between;
    bottom: 40px;
    z-index: 99;
  }
  .footer__text{
    font-family: "Poppins", sans-serif;
    color: #fff;
    text-transform: uppercase;
    font-size: 0.9em;
  }
  .footer__line{
    display: inline-block;
    width: 40px;
    height: 1px;
    background-color: #fff;
    vertical-align: middle;
    margin: 0 20px;
  }
  .footer__socials{
    color: #fff;
  }
  .footer__socials .icon{
    margin: 0 10px;
    transition: color 0.4s;
  }
  .footer__socials .icon:last-of-type{
    margin-right: 0;
  }
  .footer__socials .icon:hover{
    color: #06B7FA;
    cursor: pointer;
    transition: color 0.4s;
  }
  .project__info__date{
    display: flex;
    margin-left: 50px;
  }
  .column{
    display: flex;
    flex-direction: column;
  }
  .column:last-of-type{
    margin-left: 50px;
  }
  .column__title{
    text-transform: uppercase;
    color: #fff;
  }
  .column__value{
    margin-top: 15px;
    color: #06B7FA;
    text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.2); 
  }
  .project__button{
    position: relative;
    margin-top: 70px;
    padding: 12px 55px;
    font-size: 0.9em;
    text-transform: uppercase;
    color: #fff;
    background-color: transparent;
    font-weight: 600;
    font-family: "Poppins", sans-serif;
    letter-spacing: 3px;
    border: 3px solid #06B7FA;
    border-top-left-radius: 35px;
    border-bottom-right-radius: 35px;
    z-index: 1;
    overflow: hidden;
    border: 3px solid transparent;
    transition: border-color 0.5s;
    outline: none;
  }
  .project__button::after{
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    background-color: #06B7FA;
    width: 100%;
    height: 100%;
    z-index: -1;
    transition: transform 0.5s;
  }
  .project__button:hover,.project__button:focus{
    cursor: pointer;
    transition: border-color 0.5s;
    border-color: #06B7FA;
  }
  .project__button:hover.project__button::after, .project__button:focus.project__button::after{
    transform: translateX(105%);
    transition: transform 0.5s;
  }
</style>
