<template>
  <div class="index-wrap">
    <header>猫眼电影</header>
    <Ad></Ad>
    <nav class="topbar">
      <div class="city-entry">
        <span>北京</span>
        <i class="yo-ico">&#xf033;</i>
      </div>
      <div class="swich-hot">
        <ul>
          <router-link to="/index/movies/intheaters" tag="li" active-class="active">正在热映</router-link>
          <router-link :to="{path:'/index/movies/comingsoon'}" tag="li" active-class="active">即将上映</router-link>
        </ul>
      </div>
      <div class="btn-search yo-ico">&#xf067;</div>
    </nav>
    <main>
      <router-view></router-view>
    </main>
    <!-- <footer>
            <ul>
                <router-link to="/index/movies" tag="li" active-class="active">
                    <span>
                        <svg width="25" height="25" viewBox="0 0 50 50" xmlns="http://www.w3.org/2000/svg">
                            <title>电影1</title>
                            <g fill="#696969" fill-rule="evenodd">
                                <path d="M24.994 47c-.71 0-1.422-.034-2.136-.102C12.445 45.913 4.14 37.645 3.11 27.24c-.657-6.63 1.65-13.115 6.332-17.796 4.68-4.68 11.162-6.992 17.796-6.333 10.36 1.027 18.624 9.29 19.65 19.65.592 5.984-1.192 11.796-5.022 16.365-.162.193-.158.463.007.63l3.425 3.424c.586.584.586 1.534 0 2.12-.586.586-1.535.586-2.12 0l-3.426-3.425c-1.274-1.273-1.353-3.284-.185-4.677 3.307-3.946 4.847-8.97 4.335-14.142-.886-8.942-8.018-16.074-16.96-16.96-5.732-.562-11.336 1.426-15.38 5.47-4.042 4.042-6.034 9.647-5.467 15.378.89 8.98 8.058 16.117 17.045 16.968 3.867.37 7.68-.417 11.03-2.267.725-.4 1.637-.138 2.037.588.4.725.137 1.638-.588 2.038-3.26 1.8-6.896 2.73-10.626 2.73"></path>
                                <path d="M28 16c0 1.657-1.343 3-3 3s-3-1.343-3-3 1.343-3 3-3 3 1.343 3 3M28 34c0 1.657-1.343 3-3 3s-3-1.343-3-3 1.343-3 3-3 3 1.343 3 3M34 28c-1.657 0-3-1.343-3-3s1.343-3 3-3 3 1.343 3 3-1.343 3-3 3M16 28c-1.657 0-3-1.343-3-3s1.343-3 3-3 3 1.343 3 3-1.343 3-3 3"></path>
                            </g>
                        </svg>
                    </span>
                    <span>电影</span>
                </router-link>
                <router-link to="/index/theaters" tag="li" active-class="active">
                    <span>
                        <svg width="25" height="25" viewBox="0 0 50 50" xmlns="http://www.w3.org/2000/svg">
                            <title>影院1</title>
                            <g fill="#696969" fill-rule="evenodd">
                                <path d="M40.5 45h-31c-.83 0-1.5-.67-1.5-1.5S8.67 42 9.5 42h31c.83 0 1.5.67 1.5 1.5s-.67 1.5-1.5 1.5M9.4 8C8.077 8 7 9.077 7 10.4v23.217l7.484-11.388c.27-.414.728-.666 1.22-.677.517-.027.96.222 1.25.622.098.133 2.608 3.435 7.884 3.435 5.358 0 8.192-3.738 8.22-3.776.293-.396.75-.633 1.255-.605.492.015.944.272 1.21.686L43 33.53V10.395C43 9.075 41.926 8 40.606 8H9.4zm35.1 32.13c-.5 0-.98-.25-1.26-.687l-9.214-14.31c-1.664 1.47-4.75 3.477-9.188 3.477-4.353 0-7.278-1.805-8.872-3.174l-9.212 14.02c-.364.553-1.05.802-1.684.612-.635-.19-1.07-.774-1.07-1.437V10.4C4 7.422 6.422 5 9.4 5h31.206C43.58 5 46 7.42 46 10.395V38.63c0 .667-.438 1.253-1.077 1.44-.14.042-.282.06-.423.06z"></path>
                            </g>
                        </svg>
                    </span>
                    <span>影院</span>
                </router-link>
                <router-link to="/index/profile" tag="li" active-class="active">
                    <span>
                        <svg width="25" height="25" viewBox="0 0 50 50" xmlns="http://www.w3.org/2000/svg">
                            <title>我的1</title>
                            <g fill="#696969" fill-rule="evenodd">
                                <path d="M19.916 35.913c-.014-.016-.02-.036-.033-.05-.314-.32-.737-.455-1.153-.432C13.586 33.066 10 27.9 10 21.908 10 13.687 16.728 7 25 7c8.27 0 15 6.687 15 14.907 0 8.22-6.73 14.906-15 14.906-1.787 0-3.493-.328-5.084-.9zm14.502 1.225C39.558 33.98 43 28.343 43 21.908 43 12.032 34.925 4 25 4S7 12.033 7 21.907c0 6.657 3.68 12.466 9.113 15.552l-6.086 5.97c-.59.58-.6 1.53-.02 2.12.294.3.682.45 1.07.45.38 0 .76-.143 1.052-.43l6.916-6.785c1.867.654 3.865 1.028 5.954 1.028 2.324 0 4.54-.455 6.58-1.256l7.15 7.014c.292.287.672.43 1.05.43.39 0 .78-.15 1.072-.45.58-.59.57-1.54-.02-2.12l-6.414-6.292z"></path>
                                <path d="M30.358 25.068c-.77-.31-1.642.064-1.95.832-.554 1.375-1.89 2.263-3.408 2.263-1.503 0-2.835-.877-3.395-2.234-.316-.766-1.19-1.13-1.96-.815-.765.316-1.13 1.193-.813 1.96 1.024 2.483 3.446 4.088 6.168 4.088 2.75 0 5.178-1.627 6.19-4.144.31-.77-.063-1.643-.832-1.952"></path>
                            </g>
                        </svg>
                    </span>
                    <span>我的</span>
                </router-link>
            </ul>
    </footer>-->

    <van-tabbar v-model="active" route active-color="#e54748">
      <van-tabbar-item replace to="/index/movies/Intheaters">
        <span>电影</span>
        <img slot="icon" slot-scope="props" :src="props.active ? icon[0].active : icon[0].inactive" />
      </van-tabbar-item>
      <van-tabbar-item icon="search" replace to="/index/Theaters">
        <span>影院</span>
        <img slot="icon" slot-scope="props" :src="props.active ? icon[1].active : icon[1].inactive" />
      </van-tabbar-item>
      <van-tabbar-item icon="setting-o" replace to="/index/Profile">
        <span>我的</span>
        <img slot="icon" slot-scope="props" :src="props.active ? icon[2].active : icon[2].inactive" />
      </van-tabbar-item>
    </van-tabbar>
  </div>
</template>

<script>
import Vue from "vue";
import { Tabbar, TabbarItem } from "vant";
import Ad from "./movies/Ad"

Vue.use(Tabbar).use(TabbarItem);

import movieImg from "assets/movie.png";
import movieColorImg from "assets/movie-color.png";
import myImg from "assets/my.png";
import myColorImg from "assets/my-color.png";
import cinemaImg from "assets/cinema.png";
import cinemaColorImg from "assets/cinema-color.png";

export default {
    components:{
        
            Ad
    },
  data() {
    return {
      active: 0,
      icon: [
        {
          active: movieColorImg,
          inactive: movieImg
        },
        {
          active: cinemaColorImg,
          inactive: cinemaImg
        },
        {
          active: myColorImg,
          inactive: myImg
        }
      ]
    };
  }
};
</script>

<style lang="stylus" scoped>
header {
  height: 0.44rem;
  text-align: center;
  line-height: 0.44rem;
  color: #ffffff;
  font-size: 0.18rem;
  font-weight: 400;
  background: #e54847;
}

nav {
  height: 0.44rem;
  display: flex;

  >div:first-child {
    flex: 16;
    padding-left: 0.15rem;
    font-size: 0.16rem;
    display: flex;
    align-items: center;
    color: #666;
  }

  >div:nth-child(2) {
    flex: 43;

    ul {
      display: flex;
      width: 100%;
      height: 100%;

      li {
        line-height: 0.42rem;
        text-align: center;
        color: #666;
        flex: 1;
        font-weight: 900;
        margin: 0 0.05rem;

        &.active {
          color: #e54847;
          border-bottom: 0.02rem solid #e54847;
        }
      }
    }
  }

  >div:last-child {
    flex: 16;
    padding-right: 0.15rem;
    padding-left: 0.1rem;
    line-height: 0.44rem;
    text-align: right;
    font-size: 0.18rem;
    color: #e54847;
  }
}

.index-wrap {
  display: flex;
  height: 100%;
  flex-direction: column;
}

main {
  flex: 1;
  height: 100%;
  background: #FFF;
  padding-bottom: 50px;
}
</style>