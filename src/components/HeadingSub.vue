<script setup>
import Label from './base/Label.vue'
const props = defineProps({
    title: {
        type: String,
        default: 'Title'
    }
})
</script>

<template>
    <header>
        <Label :type="'tertiary'">
            <h2>{{props.title}}</h2>
        </Label>
        <p>
            <slot>
                At our digital marketing agency, we offer a range of services to help businesses grow and succeed online. These services include:
            </slot>
        </p>
    </header>
</template>

<style lang='scss' scoped>
// Breakpoints
$small : 480px;
$med : 768px;
$large : 1280px;
    header{
        display: flex;
        flex-direction: row;
        gap: 40px;
        align-items: center;
        @media screen and (max-width: $med){
            flex-direction: column;
            align-items: flex-start;
        }
        p{
            max-width: 580px;
        }
    }
</style>