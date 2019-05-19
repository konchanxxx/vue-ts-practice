<template>
    <div class="home">
        <p>{{greetText}}</p>
        <MyButton :greet="greetText" @clicked="onMyButtonClicked"></MyButton>
    </div>
</template>

<script lang="ts">
    import {Component, Vue} from 'vue-property-decorator';
    import MyButton from '@/components/MyButton.vue';

    @Component({
        components: {
            MyButton,
        },
    })

    export default class Home extends Vue {
        public greetText: string = "Konchan!!"

        public onMyButtonClicked() {
            this.greetText = "こんにちは";
        }
    }
</script>
