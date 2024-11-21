<script setup>

const props = defineProps({
    type: {
        type: String,
        default: 'primary'
    },
    color: {
        type: Number,
        default: 0
    },
    href: {
        type: String,
        default: './'
    }
})
</script>

<template>

    <a :href="href" :class="`${type} color-${color}`">
        <p>
            <slot>Label</slot>
        </p>
        <svg width="21" height="20" viewBox="0 0 21 20" fill="black" xmlns="http://www.w3.org/2000/svg">
            <path d="M1.25 13.701C0.532561 14.1152 0.286748 15.0326 0.700962 15.75C1.11518 16.4674 2.03256 16.7133 2.75 16.299L1.25 13.701ZM20.7694 5.38823C20.9838 4.58803 20.5089 3.76552 19.7087 3.55111L6.66874 0.0570541C5.86854 -0.157359 5.04603 0.317515 4.83162 1.11771C4.61721 1.91791 5.09208 2.74042 5.89228 2.95483L17.4834 6.06066L14.3776 17.6518C14.1631 18.452 14.638 19.2745 15.4382 19.4889C16.2384 19.7033 17.0609 19.2284 17.2753 18.4282L20.7694 5.38823ZM2.75 16.299L20.0705 6.29904L18.5705 3.70096L1.25 13.701L2.75 16.299Z"/>
        </svg>

    </a>

</template>


<style lang='scss' scoped>

a{
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 15px;
    text-decoration: none;
    color: var(--color-black);
    cursor: pointer;
    &:active{
        transform: scale(0.95);
    }
    &:hover{
        p{
            text-decoration: underline;
            text-underline-offset: 3px;
            text-decoration-thickness: 2px;
            font-weight: 700 !important;
        }
    }
    p{
        font-size: 20px;
        font-weight: 400;
        line-height: 28px;
        text-align: center;
        user-select: none;
    }
    svg{
        width: 20px;
        fill: var(--color-black);
    }
}

// Primary
a.primary{
    &.color-0{
        p{
            color: var(--color-black)
        }
        svg{
            width: 20px;
            fill: var(--color-black);
        }
    }
    &.color-1{
        p{
            color: var(--color-bg)
        }
        svg{
            width: 20px;
            fill: var(--color-bg);
        }
    }
    &.color-2{
        p{
            color: var(--color-accent)
        }
        svg{
            width: 20px;
            fill: var(--color-accent);
        }
    }

}

// Secondary
a.secondary{
    flex-direction: row-reverse;
    svg{
        border-radius: 25px;
        padding: 10px;
        width: 41px;
        height: 41px;
    }
    &.color-0{
        p{color: var(--color-bg)}
        svg{
            background-color: var(--color-accent);
            fill: var(--color-bg);
        }
    }
    &.color-1{
        p{color: var(--color-black)}
        svg{
            background-color: var(--color-accent);
            fill: var(--color-black);
        }
    }
    &.color-2{
        p{color: var(--color-black)}
        svg{
            background-color: var(--color-black);
            fill: var(--color-bg);
        }
    }
    &.color-3{
        p{color: var(--color-black)}
        svg{
            background-color: var(--color-dark);
            fill: var(--color-accent);
        }
    }
    &.color-4{
        p{color: var(--color-bg)}
        svg{
            background-color: var(--color-bg);
            fill: var(--color-black);
        }
    }
    &.color-5{
        p{color: var(--color-bg)}
        svg{
            background-color: var(--color-bg);
            fill: var(--color-accent);
        }
    }
}
</style>