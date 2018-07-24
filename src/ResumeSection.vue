<template>
  <div class="section">
    <h1>
      <slot name="section-header"></slot>
    </h1>
    <slot name="sub-sections"></slot>
  </div>
</template>

<script>
import SubSection from './SubSection.vue';

export default {
  components: {
    SubSection
  }
}
</script>

<style lang="scss" scoped>
.section {
  width: 98%;
  padding: 12px 19px 3px !important;
  margin: 9px 0px;
  margin-left: 1%;
  background: #fff;
  box-shadow: 0px 0px 30px 0px rgba(0, 0, 0, 0.08), 0px 3px 2px 0px rgba(0, 0, 0, 0.05);
  border-radius: 5px;
}
h1 {
  margin-top: 0px;
  font-family: 'Raleway';
  font-size: 20px;
  font-weight: 800;
  color: #373737;
  margin-bottom: -3px;
}

</style>
