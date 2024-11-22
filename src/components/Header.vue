<script setup>
import Logo from './base/Logo.vue'
import Button from './base/Button.vue'
</script>


<template>
<header>
    <Logo></Logo>
    <nav>
        <input type="checkbox" name="togglemenu" id="menu">
        <ul>
            <li>
                <a href="#LandingPage">About us</a>
            </li>
            <li>
                <a href="#Services">Services</a>
            </li>
            <li>
                <a href="#CaseStudies">Use Cases</a>
            </li>
            <li>
                <a href="/pricing">Pricing</a>
            </li>
            <li>
                <a href="/blog">Blog</a>
            </li>
            <li>
                <Button :type="'secondary'">Request a quote</Button>
            </li>
        </ul>
    </nav>
</header>
</template>


<style lang='scss' scoped>
// Breakpoints
$small : 480px;
$med : 768px;
$large : 1280px;
header{
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 20px 0px;
    nav{
        position: relative;
        display: flex;
        flex-direction: row;
        align-items: center;
        input{
            display: none;
        }
        ul{
            display: flex;
            align-items: center;
            gap: 20px;
            li{
                list-style: none;
                position: relative;
                a{
                    padding: 5px 10px;
                    font-size: 20px;
                    line-height: 28px;
                    text-align: center;
                    color: var(--color-black);
                    user-select: none;
                    text-decoration: none;
                    text-decoration-color: var(--color-accent);
                    border-radius: 15px;
                    &::after{
                        z-index: -1;
                        position: absolute;
                        content: '';
                        width: 100%;
                        height: 100%;
                        top: 0px;
                        left: 0px;
                        transition: all 0.2s ease-in-out;
                        border-radius: 15px;
                        transform-origin: center;
                        background-color: var(--color-accent);
                        transform: scale(0);
                    }
                    &:hover::after{
                        transform: scale(1.4);
                    }
                }
            }
        }
        @media screen and (max-width: $large) {
            cursor: pointer;
            ul{
                display: none;
            }
            input{
                z-index: 1;
                display: block;
                cursor: pointer;
                appearance: none;
                width: 40px;
                height: 4px;
                border-radius: 10px;
                margin: 12px 0px;
                background: var(--color-dark);
                &:checked{
                    background-color: transparent;
                    transition: background-color 0.5s ease-in-out;
                    &::before{
                        transform: rotate(45deg) translate(-3px, 6px);
                    }
                    &::after{
                        transform: rotate(-45deg) translate(-5px, -6px);
                    }
                }
                &::before, &::after{
                    transition: transform 0.5s ease-in-out;
                    position: absolute;
                    content: '';
                    width: 40px;
                    border-radius: 10px;
                    height: 4px;
                    background: var(--color-dark);
                    right: 0px;
                    bottom: 0px;
                    transform-origin: 100% 100%;
                }
                &::after{
                    top: 0px;
                    transform-origin: 100% 0%;

                }
            }
        }
    }
}
</style>