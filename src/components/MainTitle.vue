<template>
  <div>
    {{title}}
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class MainTitle extends Vue {
  @Prop() private title: string;
}

</script>



<style scoped lang="scss">
div {
  position: relative;
  font-family: Chewy;
  font-style: normal;
  font-weight: normal;
  font-size: 82px;
  line-height: 107px;
  letter-spacing: -0.3034px;
  color: #FFFFFE;
  word-wrap: break-word;
}

</style>