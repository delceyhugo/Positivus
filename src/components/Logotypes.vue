<script setup>
import netflix from '@/assets/compagny-logo/company1.png'
import amazon from '@/assets/compagny-logo/company2.png'
import dribbble from '@/assets/compagny-logo/company3.png'
import zoom from '@/assets/compagny-logo/company4.png'
import notion from '@/assets/compagny-logo/company5.png'
import hubspot from '@/assets/compagny-logo/company6.png'


</script>


<template>
    <div>
        <ul>
            <li><img :src="netflix" alt=""></li>
            <li><img :src="amazon" alt=""></li>
            <li><img :src="dribbble" alt=""></li>
            <li><img :src="zoom" alt=""></li>
            <li><img :src="notion" alt=""></li>
            <li><img :src="hubspot" alt=""></li>
        </ul>
    </div>
</template>


<style lang='scss' scoped>
// Breakpoints
$small : 480px;
$med : 768px;
$large : 1280px;

    div{
        width: 100%;
        height: 48px;
        gap: 200px;
        position: relative;
        ul{
            width: 100%;
            display: grid;
            overflow: hidden;
            grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr;
            @media screen and (max-width: $large) {
                grid-template-columns: 1fr 1fr 1fr;
            }
            @media screen and (max-width: $med) {
                grid-template-columns: 1fr 1fr;
            }
            li{
                display: flex;
                justify-content: center;
                list-style: none;
                img{
                    mix-blend-mode: luminosity;
                    pointer-events: none;
                }
            }
        }
    }

</style>