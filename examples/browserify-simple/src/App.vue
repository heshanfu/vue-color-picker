<template>
    <div id="app">
        <color-picker v-model="color" />
        <h1>{{ msg }}</h1>
        <pre>{{ color }}</pre>
    </div>
</template>

<script>
import ColorPicker from '@radial-color-picker/vue-color-picker';

export default {
    name: 'app',
    components: { ColorPicker },
    data() {
        return {
            msg: 'Welcome to Your Vue.js App',
            color: {
                hue: 50,
                saturation: 100,
                luminosity: 50,
                alpha: 1,
            },
        };
    },
};
</script>

<style lang="scss">
@import "node_modules/@radial-color-picker/vue-color-picker/dist/vue-color-picker.min";

#app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    display: flex;
    flex-direction: column;
    align-items: center;
    color: #2c3e50;
    margin-top: 40px;
}

h1 {
    font-weight: normal;
}

pre {
    min-width: 275px;
    padding: 15px 30px;
    background: #f8f8f8;
    color: #525252;
    font-size: 15px;
    font-weight: bold;
    line-height: 1.6;
    margin: 0;
}

@media (max-width: 420px) {
    h1 {
        font-size: 1.4em;
    }
}
</style>
