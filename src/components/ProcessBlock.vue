<script setup>
import { ref } from 'vue'
import Plus from './base/PlusIcon.vue'

const active = ref(false)

const props = defineProps({
    title: {
        type: String,
        default: 'Consultation'
    },
    number: {
        type: String,
        default: '01'
    },
    type: {
        type: String,
        default: 'plus'
    }
})


</script>


<template>
    <div @click="active = !active" id="ProcessBlock" :class="{active: active}">
        <header>
            <div>
                <h1>{{number}}</h1>
                <h2>{{title}}</h2>
            </div>
            <Plus v-if="active" @onClick="active = true" :type="'minus'"></Plus>
            <Plus v-if="!active" @onClick="active = false" :type="'plus'"></Plus>
        </header>
        <p v-if="active">
            <slot>Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit doloremque porro totam id repellat earum, distinctio perferendis ipsum laborum rerum nihil maiores accusamus temporibus explicabo facere magni provident cumque ad.</slot>
        </p>
    </div>
</template>


<style lang='scss' scoped>
// Breakpoints
$small : 480px;
$med : 768px;
$large : 1280px;

    #ProcessBlock{
        display: flex;
        flex-direction: column;
        gap: 30px;
        padding: 30px 70px;
        border-radius: 20px;
        border: 1px solid var(--color-dark);
        background-color: var(--color-bg);
        box-shadow: 0px 5px #191A23;
        position: relative;
        cursor: pointer;
        @media screen and (max-width: $large) {
            padding: 2vw 4vw;
            h1{
                font-size: 40px !important;
            }
            h2{
                font-size: 20px !important;
            }
            header{
                gap: 15px !important;
                div{
                    gap: 15px !important;
                }
                >:last-child{
                    width: 40px;
                    height: 40px;
                    padding: 5px;
                    :last-child{
                        padding: 3px !important;
                    }
                }
            }
        }
        @media screen and (max-width: $med) {
            h1{
                font-size: 30px !important;
            }
            h2{
                font-size: 15px !important;
            }
            header{
                >:last-child{
                    width: 40px;
                    height: 40px;
                    :last-child{
                        padding: 5px !important;
                    }

                }
            }
        }
        &.active{
            background-color: var(--color-accent);        
        }
        header{
            display: flex;
            flex-direction: row;
            gap: 20px;
            align-items: center;
            justify-content: space-between;
            div{
                display: flex;
                flex-direction: row;
                gap: 30px;
                align-items: center;
                h1{
                    font-size: 60px;
                    font-weight: 500;
                }
                h2{
                    font-size: 30px;
                    font-weight: 500;
                }
            }
        }
        p{
            padding: 20px 0px;
            &::before{
                content: '';
                position: absolute;
                width: calc(100% - 140px);
                height: 2px;
                border-radius: 2px;
                background-color: var(--color-dark);
                top: 50%;
            }
        }
    }

</style>