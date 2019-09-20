<template>
    <div>
        {{subtitle}}
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class Subtitle extends Vue {
    @Prop() private subtitle: string;
}
</script>

<style scoped lang="scss">
div {
    position: relative;
    font-family: Chewy;
    font-style: normal;
    font-weight: normal;
    font-size: 55px;
    line-height: 72px;
    letter-spacing: -0.3034px;
    color: #FFFFFE;
    word-wrap: break-word;
}

</style>