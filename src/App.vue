<template>
    <div id="app">
        <div class="wrapper">
            <Top/>
            <Content/>
        </div>
    </div>
</template>

<script>
    import Top from './components/Top.vue'
    import Content from './components/Content.vue'

    export default {
        name: 'app',
        components: {
            Top,
            Content
        }
    }
</script>

<style lang="scss">
    @font-face {
        font-family: 'HelveticaNeueCyr';
        src: url('./assets/fonts/HelveticaNeueCyr-Bold.eot');
        src: url('./assets/fonts/HelveticaNeueCyr-Bold.eot?#iefix') format('embedded-opentype'),
        url('./assets/fonts/HelveticaNeueCyr-Bold.woff2') format('woff2'),
        url('./assets/fonts/HelveticaNeueCyr-Bold.woff') format('woff'),
        url('./assets/fonts/HelveticaNeueCyr-Bold.ttf') format('truetype');
        font-weight: bold;
        font-style: normal;
    }

    @font-face {
        font-family: 'HelveticaNeueCyr';
        src: url('./assets/fonts/HelveticaNeueCyr-Light.eot');
        src: url('./assets/fonts/HelveticaNeueCyr-Light.eot?#iefix') format('embedded-opentype'),
        url('./assets/fonts/HelveticaNeueCyr-Light.woff2') format('woff2'),
        url('./assets/fonts/HelveticaNeueCyr-Light.woff') format('woff'),
        url('./assets/fonts/HelveticaNeueCyr-Light.ttf') format('truetype');
        font-weight: 300;
        font-style: normal;
    }

    @font-face {
        font-family: 'HelveticaNeueCyr';
        src: url('./assets/fonts/HelveticaNeueCyr-Medium.eot');
        src: url('./assets/fonts/HelveticaNeueCyr-Medium.eot?#iefix') format('embedded-opentype'),
        url('./assets/fonts/HelveticaNeueCyr-Medium.woff2') format('woff2'),
        url('./assets/fonts/HelveticaNeueCyr-Medium.woff') format('woff'),
        url('./assets/fonts/HelveticaNeueCyr-Medium.ttf') format('truetype');
        font-weight: 500;
        font-style: normal;
    }

    @font-face {
        font-family: 'HelveticaNeueCyr';
        src: url('./assets/fonts/HelveticaNeueCyr-UltraLight.eot');
        src: url('./assets/fonts/HelveticaNeueCyr-UltraLight.eot?#iefix') format('embedded-opentype'),
        url('./assets/fonts/HelveticaNeueCyr-UltraLight.woff2') format('woff2'),
        url('./assets/fonts/HelveticaNeueCyr-UltraLight.woff') format('woff'),
        url('./assets/fonts/HelveticaNeueCyr-UltraLight.ttf') format('truetype');
        font-weight: 200;
        font-style: normal;
    }

    @font-face {
        font-family: 'HelveticaNeueCyr';
        src: url('./assets/fonts/HelveticaNeueCyr-Roman.eot');
        src: url('./assets/fonts/HelveticaNeueCyr-Roman.eot?#iefix') format('embedded-opentype'),
        url('./assets/fonts/HelveticaNeueCyr-Roman.woff2') format('woff2'),
        url('./assets/fonts/HelveticaNeueCyr-Roman.woff') format('woff'),
        url('./assets/fonts/HelveticaNeueCyr-Roman.ttf') format('truetype');
        font-weight: normal;
        font-style: normal;
    }

    * {
        margin: 0;
        padding: 0;
    }

    html,
    body {
        height: 100%;
    }


    body {
        font-family: 'HelveticaNeueCyr', Helvetica, Arial, sans-serif;
        font-weight: normal;
        font-size: 21px;
        text-align: center;
        color: #fff;
        background-color:  #252525;
    }

    a {
        color: #fff;
        text-decoration: none;

        &:hover {

        }
    }

    h3{
        font-size: 35px;
        font-weight: normal;
    }

    .icon {
        height: 21px;
        width: 21px;
        filter: invert(1);
        transition: 0.2s;
        animation-timing-function: ease;

        &__img {
            height: 100%;
            width: 100%;
        }
    }

    .logo {
        filter: grayscale(1) brightness(10);
        display: block;
        width: 176px;

        &__img {
            width: 100%;
            height: 100%;
        }
    }
</style>
