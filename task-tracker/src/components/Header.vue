<template>
    <div>
        <h1>{{msg}}</h1>
        <Button msg="Add Todo" @click="ToggleView" />
    </div>
    <div>
        <InputStuff v-show="toggled" />
    </div>
</template>

<script>
import Button from './Button';
import InputStuff from './InputStuff';

export default {
    name: 'Header',
    components: {
        Button,
        InputStuff
    },
    data(){
        toggled: false,
    },
    props: {
        'msg': String,
    },
    ToggleView(){
        this.toggled = !toggled;
    }
}
</script>

<style scoped>
div{
    display: flex;
}
</style>