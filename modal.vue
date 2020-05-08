<template>
        <div :id="name" class="overlay">
            <a href="#" class="cancel"></a>
            <div class="custom-modal">

                <slot name="header"></slot>
                <slot name="body"></slot>
                <slot name="footer"></slot>

                <a href="#" class="custom-close">&times;</a>
            </div>
        </div>
</template>
<style>
    .overlay {
        visibility: hidden;
        position: absolute;
        top: 0;
        bottom: 0;
        right: 0;
        left: 0;
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .overlay:target {
        visibility: visible;
        z-index: 10;
    }
    .custom-modal {
        position: relative;
        width: 600px;
        /*background: grey;*/
        /*background: #bcee66;*/
        /*background: #a5e830;*/
        /*background: lightyellow;*/
        background:  #16a9c7;
        border-radius: 5px;
        padding: 1em;
    }

    .custom-modal .custom-close {
        position: absolute;
        top: 0;
        right: 0;
        color: yellow;
        text-decoration: none;
    }
    .cancel {
        position: absolute;
        top: 0;
        bottom: 0;
        right: 0;
        left: 0;
    }
</style>

<script>
    export default {
        props: ['name'],
    }
</script>
