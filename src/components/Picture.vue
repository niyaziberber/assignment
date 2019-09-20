<template>
    <div class="picture">
        <div id="image">
            <img id="frame" src="../assets/mountain.jpg">
            <div id="arcHalf">
                <div class="circle" id="circleTop"></div>
                <div class="circle" id="circleBottom"></div>
                <div id="arcQuarter"></div>
                <div id="triangleTop" class="triangle"></div>
                <div id="triangleBottom" class="triangle"></div>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class Picture extends Vue {
}
</script>137px

<style scoped lang="scss">
#triangleTop {
    top: -680px;
    left: 446px;
    transform: rotate(110deg);
}

#triangleBottom {
    top: -355px;
    left: 674px;
    transform: rotate(41deg);
}

#frame {
    position: relative;
    width: 630px;
    height: 630px;
    background: #FBBBD3;
    border: 41px solid #FBBBD3;
    border-radius: 50%;
    top: 158px;
    right: -277px;
}

#arcHalf {
    position: relative;
    border: 2px solid #FFFFFF;
    width: 659px;
    height: 659px;
    -webkit-transform: rotate(32deg);
    transform: rotate(32deg);
    border-radius: 50%;
    border-left-color: transparent;
    border-bottom-color: transparent;
    transform: rotate(32deg);
    right: -270px;
    top: -487px;
}

#arcQuarter {
    left: 31px;
    top: 16px;
    position: relative;
    display: flow;
    border: 2px solid white;
    position: relative;
    width: 648px;
    height: 648px;
    border-radius: 50%;
    border-left-color: transparent;
    border-bottom-color: transparent;
    border-top-color: transparent;
    -webkit-transform: rotate(88deg);
    transform: rotate(51deg);
}

#circleTop {
    width: 10px;
    height: 9px;
    top: 99px;
    left: 83px;
}

#circleBottom {
    top: 555px;
    left: 545px;
    width: 10px;
    height: 10px;
}

.picture {
    position: relative;
    max-width: 400px;
    max-height: 400px;
    left: -11px;
}

.circle {
    border: 1.6px solid white;
    border-radius: 50%;
    position: relative;
}

.triangle {
    position: relative;
    width: 0;
    height: 0;
    border-left: 9px solid transparent;
    border-right: 4px solid transparent;
    border-bottom: 11px solid white;
}

</style>
