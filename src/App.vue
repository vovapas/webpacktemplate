<template>
    <div class="div-app">
         <div class="container">
            <div class="row">
                <div class="col">
                    <MyComponent />
                </div>
            </div>
            <div class="row">
                <div class="col">
                    <userCard />
                </div>
            </div>
        </div>
    </div>   
</template>

<script>
import MyComponent from './components/MyComponent.vue'
import userCard from './components/userCard.vue'

export default {
    name: 'App',
    components: {
        MyComponent,
        userCard
    }
}
</script>

<style lang="scss" scoped>
    .div-app{
        background-color: greenyellow;
    }
</style>