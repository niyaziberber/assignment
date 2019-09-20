<template>
    <div>
        <textarea type="text" v-model="newText" v-on:input="changeTextArea" :maxlength="maxLength" :placeholder="newPlaceholder"> </textarea>
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component({})
export default class TextareaInput extends Vue {
    public newText: string;
    @Prop() private maxLength: number;
    @Prop() private newPlaceholder: string;
    private changeTextArea() {this.$emit('newTextBody', this.newText); }
}
</script>

<style scoped lang="scss">
input {
    padding: 10px 20px;
    border: 1px solid #CCC;
    border-radius: 5px;
    width: 250px;
}

textarea {
    width: 300px;
    height: 100px;
}
</style> 