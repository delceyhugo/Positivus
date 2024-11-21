<script setup>
const props = defineProps({
    type: {
        type: String,
        default: 'primary'
    }
})
</script>

<template>
    <div :class="type">
        <slot >Label</slot>
    </div>
</template>

<style lang="scss" scoped>
.primary{
    :first-child{
        display: inline;
        text-align: center;
        align-self: center;
        border-radius: 7px;
        padding: 0px 7px;
        color: var(--color-bg);
        background-color: var(--color-dark);
    }
}
.secondary{
    :first-child{
        display: inline;
       text-align: center;
        align-self: center;
        border-radius: 7px;
        padding: 0px 7px;
        color: var(--color-black);
        background-color: var(--color-bg);     
    }
}
.tertiary{
    :first-child{
        display: inline;
        text-align: center;
        align-self: center;
        border-radius: 7px;
        padding: 0px 7px;
        color: var(--color-black);
        background-color: var(--color-accent);
    }
}
</style>