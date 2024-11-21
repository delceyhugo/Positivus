<script setup>
import Label from './base/Label.vue'
import Link from './base/Link.vue'
const props = defineProps({
    setup: {
        type: Object,
    }
})
</script>


<template>
    <div class="services-block" :style="`background-color: var(--color-${setup.cardColor})`">
        <Label :type="setup.labelType">
            <h3>{{setup.title}}</h3>
        </Label>
        <img v-if="setup.img=== 'loupe'" src="@/assets/services-illustration/loupe.svg" alt="A magnifying glass">
        <img v-if="setup.img=== 'click'" src="@/assets/services-illustration/click.svg" alt="A mousse click">
        <img v-if="setup.img=== 'screen'" src="@/assets/services-illustration/screen.svg" alt="A screen">
        <img v-if="setup.img=== 'letter'" src="@/assets/services-illustration/letter.svg" alt="Letter">
        <img v-if="setup.img=== 'tab'" src="@/assets/services-illustration/tab.svg" alt="A web browser tab">
        <img v-if="setup.img=== 'chart'" src="@/assets/services-illustration/chart.svg" alt="Some chart">
        <Link :type="setup.linkType" :color="setup.linkColor">Learn more</Link>
    </div>
</template>


<style lang='scss' scoped>
// Breakpoints
$small : 480px;
$med : 768px;
$large : 1280px;

.services-block{
    display: grid;
    justify-items: start;
    padding: 50px;
    border-radius: 45px;
    box-shadow: 0px 5px #191A23;
    border: #191A23 1px solid;
    gap: 20px;
    align-items: center;
    grid-template: 
    "a c" auto
    "b c" auto/1fr 1fr;
    @media screen and (max-width: $large) {
        grid-template: 
        "a" auto
        "c" auto
        "b" auto;
    }
    :first-child{
        grid-area: a;
    }
    img{
        height: auto;
        grid-area: c;
        width: 90%;
        max-height: 200px;
        pointer-events: none;
    }
    :last-child{
        grid-area: b;
    }
}


</style>