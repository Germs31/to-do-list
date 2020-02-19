<template>
    <div>
        <h1> add to do</h1>
        <form @submit.prevent="addTodo">  
        <input type="text" v-model="title" name="title" placeholder="add todo.."/>
        <button type="submit">Add</button>
        </form>
    </div>
</template>

<script>
export default {
    name: "AddTodo",
    data() {
        return{
            title: ''
        }
    },
    methods: {
        addTodo() {
            console.log(this.title)
            this.title = ''
        }
    }
    
}
</script>

<style lang="stylus">

</style>