<template>
  <div class="remuse-body">
    <section-item subtitle="教育经历" classes="education">
      <div
        class="section-subitem"
        v-for="(edu, index) in education"
        :key="index"
      >
        <div class="section-subitem-header">
          <span class="school-name">{{ edu.schoolName }}</span>
          <span class="range sub-text">{{ edu.range }}</span>
        </div>
        <div class="section-subitem-subheader sub-text">{{ edu.majorIn }}</div>
      </div>
    </section-item>
    <section-item subtitle="作品链接">
      <ul class="supplements">
        <li class="sociallink" v-for="(port, index) in portfolio" :key="index">
          <i :class="port.icon"></i>
          <span class="sociallink-text">{{ port.name }}</span>
          <a :href="port.link" target="_blank" rel="noopener noreferrer">{{port.link}}</a>
        </li>
      </ul>
    </section-item>
    <section-item subtitle="简介">
      <ul class="supplements">
        <li class="sociallink" v-for="(prof, index) in profile" :key="index">
          {{ prof }}
        </li>
      </ul>
    </section-item>
    <section-item subtitle="工作经历" classes="experiences">
      <div
        class="section-subitem"
        v-for="(work, index) in workExperience"
        :key="index">
        <div class="section-subitem-header">
          <span class="company-name">{{ work.company }}</span>
          <span class="range sub-text">{{ work.range }}</span>
        </div>
        <div class="section-subitem-subheader sub-text">
          {{ work.position }}
        </div>
      </div>
    </section-item>
    <section-item subtitle="项目经历" classes="personal-projects">
      <div class="project-section" v-for="(project,index) in projectExperience" :key="index">
        <div class="project-name">{{project.name}}</div>
        <div class="project-desc">{{project.describe}}</div>
        <ul class="project-detail">
          <li class="detail" v-for="(det,index) in project.detail" :key="index">
            {{det}}
          </li>
        </ul>
        <div class="project-techs">
          <span class="tech" v-for="(tec,index) in project.tech" :key="index">{{tec}}</span>
        </div>
      </div>
    </section-item>
    <section-item subtitle="技术亮点">
      <ul class="supplements">
        <li class="supplement" v-for="(light, index) in highlight" :key="index">
          {{ light }}
        </li>
      </ul>
    </section-item>
    <section-item subtitle="其他">
      <ul class="supplements">
        <li class="supplement" v-for="(other, index) in others" :key="index">
          {{ other }}
        </li>
      </ul>
    </section-item>
  </div>
</template>

<script>
import SectionItem from './SectionItem'
import Data from '../data'
export default {
  name: 'ResumeBody',
  components: {
    SectionItem
  },
  data () {
    return Data
  }
}
</script>

<style>
</style>
