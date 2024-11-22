<script setup>
import Button from './base/Button.vue'
</script>


<template>
    <main>
        <div class="anim-from-left" id="Contact-form">
            <form action="">
                <fieldset>
                    <div>
                        <input checked name="type" id="SayHi" type="radio" value="SayHi">
                        <label for="SayHi">Say Hi</label>
                    </div>
                    <div>
                        <input name="type" id="GetaQuote" type="radio" value="GetaQuote">
                        <label for="GetaQuote">Get a Quote</label>
                    </div>
                </fieldset>

                <div class="form-group">
                    <label for="name">Name</label>
                    <input id="name" name="name" type="text" placeholder="Name" autocomplete="name">
                </div>

                <div class="form-group">
                    <label for="email">Email*</label>
                    <input id="email" name="email" type="email" placeholder="Email" autocomplete="email">
                </div>

                <div class="form-group">
                    <label for="message">Message*</label>
                    <textarea id="message" name="message" cols="30" rows="6" placeholder="Message" autocomplete="off"></textarea>
                </div>

                <Button :type="'primary'">Send Message</Button>
            </form>
        </div>
        <img src="@/assets/contact.png" alt="illustration for contact">
    </main>

</template>


<style lang='scss' scoped
// Breakpoints
$small : 480px;
$med : 768px;
$large : 1280px;

main{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    background-color: var(--color-bg);
    border-radius: 45px;
    padding: 4vw 5vw;
    overflow: hidden;
    position: relative;
    #Contact-form{
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        gap: 40px;
        width: 100%;
        max-width: 700px;
        z-index: 2;
        form{
            display: flex;
            flex-direction: column;
            gap: 25px;
            fieldset{
                display: flex;
                flex-direction: row;
                gap: 50px;
                align-items: center;
                border: none;
                div{
                    display: flex;
                    flex-direction: row;
                    gap: 10px;
                    align-items: center;
                    input{
                        width: 28px;
                        height: 28px;
                        border-radius: 29px;
                        border: 1px solid var(--color-dark);
                        -webkit-appearance: none;
                        -moz-appearance: none;
                        appearance: none;
                        padding: 0px;
                        cursor: pointer;
                        &:checked::after{
                            content: '';
                            width: 16px;
                            height: 16px;
                            border-radius: 29px;
                            margin: 5px;
                            background-color: var(--color-accent);
                            display: block;
                        }
                    }
                }
                label{
                    cursor: pointer;
                }
            }
            .form-group{
                display: flex;
                flex-direction: column;
                gap: 5px;
                label{
                    font-size: 20px;
                    font-weight: 500;
                }
                input, textarea{
                    padding: 20px;
                    border-radius: 14px;
                    border: 1px solid var(--color-dark);
                    background-color: var(--color-bg);
                }
            }
        }
    }
    img{
        position: absolute;
        right: -325px;
        z-index: 1;
        @media screen and (max-width: $med){
            display: none;
        }
    }

}

</style>