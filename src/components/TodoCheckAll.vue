<template>
    <div><label><input type="checkbox" :checked="!anyRemaining" @change="allChecked"> Check All</label></div>
</template>
<script>
export default {
    name:"todo-check-all",
    props:{
        anyRemaining:{
            type:Boolean,
            require :true
        },
    },
    methods:{
        allChecked(){
            this.$emit('checkAllTodos', this.anyRemaining)
        }
    }
}
</script>