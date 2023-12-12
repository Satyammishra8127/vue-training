<template>
<div>
    <h1>Simple Form</h1>
    <ul>
        <li v-for="item in error" v-bind:key="item">
            {{ item }} not valid.

        </li>
    </ul>

    <form class="simpleform">
        <label>Email* :</label>
        <input type="text" placeholder="Enter Email" v-model="form.email" />
        <br /><br />
        <label>Password* :</label>
        <input type="text" placeholder="Enter Password" v-model="form.password" />
        <br /><br />
        <label>Country* : </label>
        <select v-model="form.country">
            <option>india</option>
            <option>iron</option>
            <option>indonesia</option>
            <option>japan</option>

        </select>
        <br /><br />
        <h3>Technology*</h3>
        <label>Vue :</label>
        <input type="checkbox" value="Vue" v-model="form.technology" />
        <br /><br />
        <label>React :</label>
        <input type="checkbox" value="React" v-model="form.technology" />
        <br /><br />
        <h3>Gender*</h3>
        <label>Male :</label>
        <input type="radio" value="Male" v-model="form.gender" />
        <br /><br />
        <label>Female :</label>
        <input type="radio" value="Female" v-model="form.gender" />
        <br /><br />
        <button type="button" v-on:click="login">Login</button>

    </form>
</div>
</template>

<script>
export default {
    name: 'SimpleForm',
    data() {
        return {
            form: {
                email: ' ',
                password: ' ',
                technology: [],
                gender: ' ',
                country: ' ',

            },
            error: [],
        }
    },
    methods: {
        login() {
            this.error = [];
            for (const item in this.form) {
                if (this.form[item] === " " || this.form[item].length === 0) {
                    this.error.push(item)
                }

            }
            if (this.error.length === 0) {
                alert(" data submit")
            }
            console.warn("login data", this.form, this.error)
        }
    }
}
</script>

<style scoped>
.simpleform {
    color:black;
    background-color: aqua;
    border: 1px solid;
    width: 170px;
    padding: 20px;
    text-align: center;
    
}
</style>
