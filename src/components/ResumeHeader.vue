<template>
  <section class="info">

    <div class="info-photo" v-if="info.photo.length !== 0" v-show="clienWidth()"><img :src="info.photo" alt="头像" /></div>

    <div class="info-item name">{{info.name}}</div>
    <div class="info-item sub-text">
      <span class="location">{{info.sex}} {{info.birth}}</span><span class="intention">{{info.jobIntention}}</span>
    </div>
    <div class="info-item sub-text">
      <span class="sub-item">
        <i class="fas fa-mobile-alt"></i>
        <span class="phone">{{info.phone}}</span>
      </span>
      <span class="sub-item">
        <i class="fas fa-envelope"></i>
        <span class="email"><a :href="info.email">{{info.email}}</a></span>
      </span>
    </div>
    <div class="info-item languages">
      <span class="language" v-for="item in info.skillsLabel" :key="item">{{item}}</span>
    </div>
  </section>
</template>

<script>
import Data from '../data'
export default {
  name: 'ResumeHeader',
  data () {
    return Data
  },
  methods: {
    clienWidth() {
      return document.documentElement.clientWidth >= 375;
    }
  }
}
</script>

<style>
section.info {
  display: flex;
  position: relative;
  flex-direction: column;
  align-items: flex-end;
  text-align: right;
}
.info-photo{
  position: absolute;
  width: 100px;
  left: 0;
  top: 0;
  box-shadow: 1px 1px 5px #e7e7e7;
}
.info-photo img{
  width: 100%;
  height: 128px;
}
section.info .info-item:not(:last-child) {
  margin-bottom: 10px;
}
section.info .name {
  font-size: 1.8em;
  color: #212529;
}
section.info .status {
  height: 20px;
  line-height: 14px;
  padding: 3px 5px;
  border-radius: 10px;
  font-size: 12px;
  color: #fff;
  background: #212529;
}
section.info .sub-text {
  font-size: 14px;
}
section.info .location,
section.info .sub-item:not(:last-child) {
  margin-right: 16px;
}
section.info .fas {
  margin-right: 5px;
}
section.info .fas,
section.info .phone,
section.info .email {
  display: inline-block;
  vertical-align: middle;
}
section.info .languages .language {
  min-width: 20px;
  height: 20px;
  padding: 2px 6px;
  border: 1px solid #495057;
  border-radius: 10px;
  margin: 0 5px;
  background-color: transparent;
  line-height: 14px;
  font-size: 12px;
}
</style>
