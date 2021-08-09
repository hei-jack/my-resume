<template>
  <div id="app" class="container user-select">
    <resume-header/>
    <resume-body/>
  </div>
</template>

<script>
import ResumeHeader from './components/ResumeHeader'
import ResumeBody from './components/ResumeBody'
export default {
  name: 'App',
  components: {
    ResumeHeader,
    ResumeBody
  }
}
</script>

<style>
@import 'assets/css/base.css';
</style>
