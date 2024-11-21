<script setup>
import Link from './base/Link.vue'


</script>


<template>
    <div id="CaseStudies-container">
        <article>
            <p>
                For a local restaurant, we implemented a targeted PPC campaign that resulted in a 50% increase in website traffic and a 25% increase in sales.
            </p>
            <Link :type="'primary'" :color="2">Learn more</Link>
        </article>
        <article>
            <p>
                For a local restaurant, we implemented a targeted PPC campaign that resulted in a 50% increase in website traffic and a 25% increase in sales.
            </p>
            <Link :type="'primary'" :color="2">Learn more</Link>
        </article>
        <article>
            <p>
                For a local restaurant, we implemented a targeted PPC campaign that resulted in a 50% increase in website traffic and a 25% increase in sales.
            </p>
            <Link :type="'primary'" :color="2">Learn more</Link>
        </article>
    </div>

</template>


<style lang='scss' scoped>


#CaseStudies-container{
    display: flex;
    flex-direction: row;
    gap: 128px;
    background: var(--color-dark);
    border-radius: 45px;
    padding: 70px 60px;
    @media screen and (max-width: 1100px) {
        background-color: transparent;
        gap: 20px;
        padding: 0px;
        border-radius: 0px;
        overflow-y: scroll;
        article{
            background-color: var(--color-dark);
            border-radius: 45px;
            padding: 20px 50px;
            min-width: 350px;
            &:not(:first-child):before{
                display: none !important;
            }
        }
    }
    article{
        display: flex;
        flex-direction: column;
        gap: 20px;
        color: white;
        position: relative;
        &:not(:first-child):before{
            left: -64px;
            position: absolute;
            content: "";
            display: block;
            width: 1px;
            height: 100%;
            background: white;
        }
    }
}


</style>