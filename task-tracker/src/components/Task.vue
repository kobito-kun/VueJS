<template>
    <li @dblclick="dbclick">
        <h4 :class="{'true': reeee }">{{task.line1}} | {{task.line2}}</h4>
    </li>
</template>

<script>
export default {
    name: 'Task',
    props: {
        task: Object,
    },
    data(){
        return{
            reeee: true
        }
    },
    methods: {
        dbclick(){
            this.reeee = !this.reeee
            console.log(this.reeee)
        }
    }
}
</script>

<style scoped>
.true{
    background: red;
}
.false{
    background: blue;
}

</style>