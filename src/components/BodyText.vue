<template>
  <div>
      {{bodyText}}
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class BodyText extends Vue {
    @Prop() private bodyText: string;
}

</script>


<style scoped lang="scss">
div {
    color: #FEFEFE;
    font-family: Gaegu;
    font-size: 43px;
    font-style: normal;
    font-weight: normal;
    letter-spacing: -0.7095px;
    line-height: 54px;
    position: relative;
    word-wrap: break-word;
}

</style>