<template>
    <div id="mp-dialog-select">
        <label>{{ request.title }}</label>
        <select v-model="value">
            <option v-for="option in request.param.options" :value="option.value">{{ option.title }}</option>
        </select>
    </div>
</template>

<style>
    #mp-dialog-select {
        overflow: auto;
    }

    #mp-dialog-select label {
        float: left;
        padding-top: 5px;
        vertical-align: top;
        margin-right: 10px;
        width: 20%;
        font-size: 14px;
        color: #666;
    }

    #mp-dialog-select select{
        float: left;
        display: inline-block;
        width: 70%;
        margin-top: 5px;
        color: #999;
        border: 1px solid #ddd;
    }
</style>

<script>
import abstractInputComponent from './AbstractInputComponent.vue'

export default {
    name: 'dialog-select',
    extends: abstractInputComponent
}
</script>