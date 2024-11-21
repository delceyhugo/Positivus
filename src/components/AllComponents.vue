<script setup>
import Button from './base/Button.vue'
import Label from './base/Label.vue'
import Link from './base/Link.vue'
import PlusIcon from './base/PlusIcon.vue'
import Logo from './base/Logo.vue'
</script>


<template>
    <div>
        <Button :type="'primary'"></Button>
        <Button :type="'secondary'"></Button>
        <Button :type="'tertiary'"></Button>

        <Label :type="'primary'"></Label>
        <Label :type="'secondary'"></Label>
        <Label :type="'tertiary'"></Label>

        <Link :type="'primary'" :color="0"></Link>
        <Link :type="'primary'" :color="1"></Link>
        <Link :type="'primary'" :color="2"></Link>

        <Link :type="'secondary'" :color="0"></Link>
        <Link :type="'secondary'" :color="1"></Link>
        <Link :type="'secondary'" :color="2"></Link>
        <Link :type="'secondary'" :color="3"></Link>
        <Link :type="'secondary'" :color="4"></Link>
        <Link :type="'secondary'" :color="5"></Link>

        <PlusIcon :type="'plus'"></PlusIcon>
        <PlusIcon :type="'minus'"></PlusIcon>

        <Logo :color="'white'"></Logo>
        <Logo :color="'black'"></Logo>
    </div>
</template>

<style lang='scss' scoped>

div{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr 1fr;
    gap: 30px;

}

</style>