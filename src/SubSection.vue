<template>
  <div class="sub-section">
    <h1 v-if="showSeperator">
      <div class="date-seperator"></div>
      <span :style="this.styleObject" class="sub-section-header">
        <slot name="sub-section-header"></slot>
      </span>
      <span class="dates">
        <slot name="dates"></slot>
      </span>
    </h1>
    <slot name="bullets"></slot>
  </div>
</template>

<script>
export default {
  props: {
    showSeperator: {
      type: Boolean,
      default: true
    }
  },
  mounted () {
    this.styleObject = this.showSeperator ? {marginBottom: '20px'} : '';
  },
  data () {
    return {
      styleObject
    }
  }
}
</script>

<style lang="scss" scoped>
.date-seperator {
  width: 100%;
  height: 2px;
  border-radius: 2px;
  background: rgba(0,0,0,0.1);
}
.sub-section {
  padding-left: 12px;
  font-size: 13px;
}
h1 {
  position: relative;
  //margin-top: px;
  padding-top: 8px;
  padding-bottom: 8px;
  font-size: 18px;
  font-family: 'Raleway';
  font-style: italic;
  color: #474747;
}
.sub-section-header {
  position: absolute;
  background: #fff;
  margin-top: -12px;
  padding-right: 30px;
}
.dates {
  position: absolute;
  right: 0;
  color: rgba(0,0,0,0.5);
  margin-top: -12px;
  background: #fff;
  padding-left: 30px;
}
ul {
  margin-top: -8px;
}
li {
  .bold {
    color: #373737;
  }
  padding-top: 4px;
}

</style>
