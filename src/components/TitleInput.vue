<template>
    <div class="titleInput">
        <input type="text" placeholder="Title" v-model="newTitle" v-on:input="changeTitle" :maxlength="maxLength">
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class TitleInput extends Vue {
    private newTitle: string;
    private maxLength: number = 40;
    private changeTitle() {this.$emit('newTitle', this.newTitle); }
}
</script>

<style scoped lang="scss">
input {
    padding: 10px 20px;
    border: 1px solid #CCC;
    border-radius: 5px;
    width: 250px;
}
</style>