<template>
    <div class="div-mycomponent">
        <button v-on:click="buttonMinus">-</button>
        <input 
            type="number"
            v-bind:value="count"
            :min="minCount"
            :max="maxCount"            
        >
        <button v-on:click="buttonPlus">+</button>
    </div>
</template>

<script>
export default {
    name: 'MyComponent',
    data() {
        return {
            count: 1,
            maxCount: 10,
            minCount: 1
        }
    },
    methods: {
        buttonPlus() {
            if(this.count < this.maxCount){
                this.count++
            }            
        },
        buttonMinus() {
            if(this.count > this.minCount){
                this.count--
            }
        }
    }
}
</script>

<style lang="scss" scoped>
    .div-mycomponent{
        button{
            background-color: indigo;
            color: white;
        }
    }
</style>