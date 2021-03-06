<template>
    <form @submit="submitForm" action="">
        <input type="text" v-model="line1" placeholder="Line1">
        <input type="text" v-model="line2" placeholder="Line2">
        <input type="submit" value="Submit">
    </form>
</template>

<script>
export default{
    name: 'InputStuff',
    data(){
        return{
            line1: '',
            line2: ''
        }
    },
    methods: {
        submitForm(e){
            e.preventDefault();
            if(!this.line1){
                alert("Input something bro")
            }
            const newTask = {
                id: Math.floor(Math.random() * 100000),
                line1: this.line1,
                line2: this.line2,
            }
            this.$emit('add-new-task', newTask)

            this.line1 = ''
            this.line2 = ''
        }
    }
} 
</script>