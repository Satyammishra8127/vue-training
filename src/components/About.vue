<template>
<div>
    <h1 v-if="show">if else condition</h1>
    <h1 v-else>else condition</h1>
    <button v-on:click="show=!show">Submit</button>
    <h1> for loop </h1>
    <ul>
        <li v-for="item in technology" :key="item">
            {{ item }}
        </li>
    </ul>
    <br />
    <br />
    <ul>
        <li v-for="item in user" :key="item">
            Name is :{{ item.name }}
            <br>
            Email :{{ item.email }}

        </li>
    </ul>

</div>
</template>

<script>
export default {
    name: 'AboutPage',
    data() {
        return {
            show: false,
            technology: ['java', 'php', 'vue', 'react'],
            user: [{
                    name: 'piyush',
                    email: 'sm@test.com'
                },
                {
                    name: 'robin',
                    email: 'sm@test.com'
                },
                {
                    name: 'yogesh',
                    email: 'sm@test.com'
                },
            ]

        }
    }
}
</script>

<style scoped>
h1 {
    color: brown
}

button {
    color: blue
}
</style>
