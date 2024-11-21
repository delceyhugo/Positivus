<script setup>
const props = defineProps({
    type: {
        type: String,
        default: 'primary'
    }
})
</script>


<template>
    <button :class="type">
        <p>
            <slot>Label</slot>
        </p>
    </button>
</template>


<style lang="scss" scoped>

button{
    padding: 20px 35px;
    border-radius: 14px;
    cursor: pointer;
    transition: all 0.2s ease-out;
    &:active{
        transform: scale(0.95);
    }
    p{
        font-size: 20px;
        line-height: 28px;
        font-weight: 400;
    }
}
button.primary{
    background-color: var(--color-dark);
    border: 1px solid var(--color-dark);
    &:hover{
        background-color: transparent;
        border: 1px solid var(--color-dark);
        p{color: var(--color-black);}
    }
    p{
        color: var(--color-bg);
    }
}
button.secondary{
    background-color: transparent;
    border: 1px solid var(--color-dark);
    &:hover{
        background-color: var(--color-dark);
        border: 1px solid var(--color-dark);
        p{color: var(--color-bg);}
    }
    p{
        color: var(--color-black);
    }
}
button.tertiary{
    background-color: var(--color-accent);
    border: 1px solid var(--color-accent);
    &:hover{
        background-color: transparent;
    }
    p{
        color: var(--color-black);
    }
}

</style>