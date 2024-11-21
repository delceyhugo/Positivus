<script setup>
const props = defineProps({
    type: {
        type: String,
        default: 'plus'
    }
})
const emit = defineEmits(['onClick'])

</script>


<template>

    <div @click="$emit('onClick')" v-if="type === 'plus'">
        <svg width="25" height="25" viewBox="0 0 26 26" xmlns="http://www.w3.org/2000/svg">
            <path d="M9.6 25.08V15.36H0V9.72H9.6V0H15.48V9.72H25.08V15.36H15.48V25.08H9.6Z"/>
        </svg>
    </div>

    <div @click="$emit('onClick')" v-if="type === 'minus'">
        <svg width="18" height="6" viewBox="0 0 18 6" xmlns="http://www.w3.org/2000/svg">
            <path d="M0 5.64V0H17.76V5.64H0Z" fill="black"/>
        </svg>
    </div>


</template>


<style lang='scss' scoped>
    div{
        display: flex;
        align-items: center;
        justify-content: center;
        width: 58px;
        height: 58px;
        background-color: var(--color-bg);
        border-radius: 50px;
        border: 1px solid var(--color-dark);
        cursor: pointer;
        &:hover{
            background-color: var(--color-accent);
        }
        svg{
            fill: var(--color-dark);
        }
    }

</style>