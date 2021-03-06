<template>
    <div>
        <h1>{{msg}}</h1>
        <Button msg="Add Todo" @click="ToggleView" />
    </div>
    <div>
        <InputStuff @add-new-task="test" v-show="toggleInput" />
    </div>
    <ul>
        <Task v-for="task in tasks" :key="task.id" :task="task"/>
    </ul>
</template>

<script>
import Button from './Button';
import InputStuff from './InputStuff';
import Task from './Task'

export default {
    name: 'Header',
    components: {
        Button,
        InputStuff,
        Task,
    },
    data(){
        return{
            toggleInput: true,
            tasks : [
            ]
        }
    },
    props: {
        'msg': String,
    },
    methods: {
        ToggleView(){
            this.toggleInput = !this.toggleInput;
        },
        test(newTask){
            this.tasks.push(newTask)
        }
    }
}
</script>

<style scoped>
div{
    display: flex;
}
</style>