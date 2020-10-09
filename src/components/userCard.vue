<template>
    <div class="user-card">
        <h1>Научу зарабатывать от 50 000р. в час</h1>
        <div class="main-information row">
            <div class="col-5">
                <img :src="'assets/img/man.jpg'" width="400px">              
            </div>
            <div class="col-7">
                <div class="info">
                    <h2>
                        {{ getAuthorFullName }}
                    </h2>
                    <strong>Бизнес коуч</strong>
                    <ul>
                        <li>Учу людей делать реальные</li>
                        <li>Не знаю что такое</li>
                        <li>Пообещал, что побреюсь</li>
                    </ul>
                </div>
            </div>            
        </div>
        <p>Участников: {{ users.length }} </p>
        <ul>
            <li
                v-for="(user, index) in users"
                :key="index"
            >
                {{ `${index + 1} ${getFullName(user)}` }}
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'userCard',
    data() {
        return {            
            firstName: 'Игнатий',
            secondName: 'Иларионович',
            lastName: 'Богатов',
            users: [
                {
                    firstName: 'Иван',
                    secondName: 'Иванович',
                    lastName: 'Иванов'
                },
                {
                    firstName: 'Иван',
                    secondName: 'Иванович',
                    lastName: 'Иванов'
                },
                {
                    firstName: 'Иван',
                    secondName: 'Иванович',
                    lastName: 'Иванов'
                }
                
            ]          
        }
    },
    computed: {
        getAuthorFullName() {
            return `${this.firstName} ${this.secondName} ${this.lastName}`.toUpperCase()
        }       
    },
    methods: {
        getFullName(user) {
            return `${user.firstName} ${user.secondName} ${user.lastName}`
        }
    }
}
</script>

<style lang="scss">
    li{
        list-style-type: none;
    }
</style>

