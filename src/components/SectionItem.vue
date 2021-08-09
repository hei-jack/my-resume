<template>
  <section class="section-item" :class="classes">
    <div class="section-header">
      <div class="section-title">{{ subtitle }}</div>
      <div class="section-headerline"></div>
    </div>
    <div class="section-content">
      <slot>你确定不传入些什么吗？</slot>
    </div>
  </section>
</template>

<script>
export default {
  name: 'SectionItem',
  props: {
    classes: {
      type: String,
      default: 'others'
    },
    subtitle: {
      type: String,
      required: true
    }
  }
}
</script>

<style>
</style>
