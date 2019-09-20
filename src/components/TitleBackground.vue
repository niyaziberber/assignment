<template>
    <div class="titleBackground">
        <div class="diagonal"></div>
        <hr id="rightLine">
        <hr id="bottomLeftLine">
        <hr id="topLeftLine">
        <div class="circle" id="circleLeft"></div>
        <div class="circle" id="circleRight"></div>
        <div id="leftHalfSquare"></div>
        <div class="triangle"></div>
        <div id="rightHalfSquare"></div>
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class TitleBackground extends Vue {
}
</script>

<style scoped lang="scss">
#circleLeft {
    left: 229px;
    top: -111px;
}

#circleRight {
    left: 955px;
    top: -108px;
}

#leftHalfSquare {
    position: relative;
    width: 54px;
    height: 54px;
    border: 1px solid white;
    border-right-color: transparent;
    border-top-color: transparent;
    top: 92px;
    left: -8px;
}

#rightHalfSquare {
    position: relative;
    width: 54px;
    height: 54px;
    border: 1px solid white;
    border-left-color: transparent;
    border-top-color: transparent;
    left: 904px;
    top: 30px;
}

#rightLine {
    border: 1.10px solid white;
    position: relative;
    width: 180px;
    top: -59px;
    left: 380px;
    transform: rotate(-1deg);
}

#bottomLeftLine {
    border: 1.10px solid white;
    position: relative;
    width: 208px;
    top: -65px;
    left: -359px;
    -webkit-transform: rotate(-1deg);
    transform: rotate(-1deg);
}

#topLeftLine {
    border: 1px solid white;
    position: relative;
    width: 133px;
    top: -91px;
    left: -384px;
    -webkit-transform: rotate(-1deg);
    transform: rotate(-1deg);
}

.titleBackground {
    position: relative;
    width: 950px;
    height: 243px;
    background-color: #FBBBD3;
    top: 203px;
    left: 123px;
}

.diagonal {
    top: -18px;
    position: relative;
    width: 0;
    height: 0;
    border-style: solid;
    border-width: 0px 0 17px 950px;
    border-color: transparent transparent #FBBBD3 transparent;
}

.circle {
    border: 1.6px solid white;
    border-radius: 50%;
    position: relative;
    width: 9px;
    height: 9px;
}


.triangle {
    position: relative;
    width: 0;
    height: 0;
    border-left: 7px solid transparent;
    border-right: 4px solid transparent;
    border-bottom: 8px solid white;
    right: 25.3px;
    top: 21.1px;
    transform: rotate(79deg);
}
</style>