<script setup>
import Slide from './base/Slide.vue'
import { ref, onMounted } from 'vue'
const active = ref(1)


const smmoothScroll = (id) => {
    document.querySelector('#Slide-'+ id).scrollIntoView({
        behavior: 'smooth',
        inline: 'center',
        block: 'nearest'
    });
}

</script>


<template>
    <div id="TestimonialSlider">
        <div id="Slider-wrapper">
            <main>
                <Slide id="Slide-1"></Slide>
                <Slide id="Slide-2"></Slide>
                <Slide id="Slide-3"></Slide>
                <Slide id="Slide-4"></Slide>
                <Slide id="Slide-5"></Slide>
            </main>
        </div>
        <footer>
            <div class="arrow">
                <svg @click="active==1 ? active = 1 : active = active - 1, smmoothScroll(active)" :class="active === 1 ? 'gray' : ''" style="transform: rotate(180deg);" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M2 10.5C1.17157 10.5 0.5 11.1716 0.5 12C0.5 12.8284 1.17157 13.5 2 13.5L2 10.5ZM23.0607 13.0607C23.6464 12.4749 23.6464 11.5251 23.0607 10.9393L13.5147 1.3934C12.9289 0.807613 11.9792 0.807613 11.3934 1.3934C10.8076 1.97919 10.8076 2.92893 11.3934 3.51472L19.8787 12L11.3934 20.4853C10.8076 21.0711 10.8076 22.0208 11.3934 22.6066C11.9792 23.1924 12.9289 23.1924 13.5147 22.6066L23.0607 13.0607ZM2 13.5L22 13.5L22 10.5L2 10.5L2 13.5Z" fill="white"/>
                </svg>
            </div>
            <div id="wrapper-stars">
                <svg @click="active = 1, smmoothScroll(1)" :class="active === 1 ? 'active' : ''" width="14" height="14" viewBox="0 0 14 14" xmlns="http://www.w3.org/2000/svg">
                    <path d="M7.0099 2.05941L14 0L11.9604 7.0099L14 14L7.0099 11.9604L0 14L2.05941 7.0099L0 0L7.0099 2.05941Z"/>
                </svg>
                <svg @click="active = 2, smmoothScroll(2)" :class="active === 2 ? 'active' : ''" width="14" height="14" viewBox="0 0 14 14" xmlns="http://www.w3.org/2000/svg">
                    <path d="M7.0099 2.05941L14 0L11.9604 7.0099L14 14L7.0099 11.9604L0 14L2.05941 7.0099L0 0L7.0099 2.05941Z"/>
                </svg>
                <svg @click="active = 3, smmoothScroll(3)" :class="active === 3 ? 'active' : ''" width="14" height="14" viewBox="0 0 14 14" xmlns="http://www.w3.org/2000/svg">
                    <path d="M7.0099 2.05941L14 0L11.9604 7.0099L14 14L7.0099 11.9604L0 14L2.05941 7.0099L0 0L7.0099 2.05941Z"/>
                </svg>
                <svg @click="active = 4, smmoothScroll(4)" :class="active === 4 ? 'active' : ''" width="14" height="14" viewBox="0 0 14 14" xmlns="http://www.w3.org/2000/svg">
                    <path d="M7.0099 2.05941L14 0L11.9604 7.0099L14 14L7.0099 11.9604L0 14L2.05941 7.0099L0 0L7.0099 2.05941Z"/>
                </svg>
                <svg @click="active = 5, smmoothScroll(5)" :class="active === 5 ? 'active' : ''" width="14" height="14" viewBox="0 0 14 14" xmlns="http://www.w3.org/2000/svg">
                    <path d="M7.0099 2.05941L14 0L11.9604 7.0099L14 14L7.0099 11.9604L0 14L2.05941 7.0099L0 0L7.0099 2.05941Z"/>
                </svg>
            </div>
            <div class="arrow">
                <svg @click="active==5 ? active = 5 : active = active + 1, smmoothScroll(active)" :class="active === 5 ? 'gray' : ''" width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
                    <path d="M2 10.5C1.17157 10.5 0.5 11.1716 0.5 12C0.5 12.8284 1.17157 13.5 2 13.5L2 10.5ZM23.0607 13.0607C23.6464 12.4749 23.6464 11.5251 23.0607 10.9393L13.5147 1.3934C12.9289 0.807613 11.9792 0.807613 11.3934 1.3934C10.8076 1.97919 10.8076 2.92893 11.3934 3.51472L19.8787 12L11.3934 20.4853C10.8076 21.0711 10.8076 22.0208 11.3934 22.6066C11.9792 23.1924 12.9289 23.1924 13.5147 22.6066L23.0607 13.0607ZM2 13.5L22 13.5L22 10.5L2 10.5L2 13.5Z" fill="white"/>
                </svg>
            </div>
        </footer>
    </div>
</template>


<style lang='scss' scoped>
// Breakpoints
$small : 480px;
$med : 768px;
$large : 1280px;

    #Slider-wrapper{
        background-color: var(--color-dark);
        border-radius: 45px 45px 0px 0px;
        width: 100%;
        height: auto;
        padding: 84px 0px 0px 0px;
        overflow: hidden;
        main{
            display: flex;
            flex-direction: row;
            gap: 50px;
            margin-left: calc(50% - 303px);
            width: 500%;
            @media screen and (max-width: $med){
                margin-left: calc(50% - 200px);
                gap: 200px !important;
                width: 1000% !important;
            }
        }
    }
    footer{
        display: flex;
        justify-content: center;
        width: 100%;
        align-items: center;
        justify-content: space-evenly;
        background-color: var(--color-dark);
        border-radius: 0px 0px 45px 45px;
        padding: 45px 0px 35px;
        .arrow{
            height: 24px;
            svg{
                cursor: pointer;
            }
            .gray{
                opacity: 30%;
                pointer-events: none;
            }
        }
        #wrapper-stars{
            display: flex;
            flex-direction: row;
            gap: 25px;
            svg{
                cursor: pointer;
                fill: white;
                transition: all 0.05s;
            }
            svg.active{
                fill: var(--color-accent);
            }
        }
    }
</style>