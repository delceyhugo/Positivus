<script setup>
const props = defineProps({
    setup: {
        type: Object,
    }
})

</script>


<template>
    <article>
        <header>
            <img v-if="setup.img == '1'" src="@/assets/team/team1.webp" alt="picture of a person">
            <img v-if="setup.img == '2'" src="@/assets/team/team2.webp" alt="picture of a person">
            <img v-if="setup.img == '3'" src="@/assets/team/team3.webp" alt="picture of a person">
            <img v-if="setup.img == '4'" src="@/assets/team/team4.webp" alt="picture of a person">
            <img v-if="setup.img == '5'" src="@/assets/team/team5.webp" alt="picture of a person">
            <img v-if="setup.img == '6'" src="@/assets/team/team6.webp" alt="picture of a person">
            <div>
                <h1 class="h4">{{setup.name}}</h1>
                <p>{{setup.job}}</p>
            </div>
            <img class="linkedIn" src="@/assets/linkedin.png" alt="logo of linkedin">
        </header>
        <main>
            <p>
                <slot>
                    10+ years of experience in digital marketing. Expertise in SEO, PPC, and content strategy
                </slot>
            </p>
        </main>
    </article>

</template>


<style lang='scss' scoped>
article{
    display: flex;
    flex-direction: column;
    gap: 20px;
    border-radius: 20px;
    border: 1px solid var(--color-dark);
    background-color: var(--color-bg);
    box-shadow: 0px 5px #191A23;
    padding: 40px 35px;
    position: relative;
    header{
        position: relative;
        display: flex;
        flex-direction: row;
        align-items: flex-end;
        gap: 20px;
        img{
            width: 100px;
            height: auto;
        }
        .linkedIn{
            width: 34px;
            height: 34px;
            position: absolute;
            top: 0px;
            right: 0px;
            cursor: pointer;
        }
    }
    main{
        p{
            margin-top: 30px;
        }
        &::before{
        content: '';
        position: absolute;
        width: calc(100% - 70px);
        height: 2px;
        border-radius: 2px;
        background-color: var(--color-dark);
        }
    }
}

</style>