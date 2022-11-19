<template>
    <table style="width:400px">
        <tr><th> <span>{{myprop}}</span></th>
        <th></th></tr>
        <tr>
            <td> <button @click="color = !color">check color</button></td>
            <td>
                  <!-- Use of if-->
                <span v-if="color === true"> Red</span>
                <span v-else-if="color === false">Blue</span>
                <span v-else>Not Red/Blue</span>
            </td>
        </tr>
        <tr>
            <td>
                <!--Use of @click 2-->
                <button @click="awesome = !awesome">toggle</button>
            </td>
            <td>
                <span v-if="awesome">Vue is awesome!</span>
                <span v-else>Oh no 😢</span>
            </td>
        </tr>
        <tr>
            <td> <!--use of for-->
            <span v-for="n in numbers" :key="n"><td> {{ n }}</td></span>
        </td>
        </tr>
        <tr>
            <td>  
            <!--use of v-on:click -->
            <button @click="count++">Add 1</button>
            <p>Count is: {{ count }}</p>
            </td>
        </tr>
    </table>
</template>
<style>
table, th, td {
  border: 1px solid black;
}
</style>
<script>
    export default {
        name: 'MyPractice',
        props: {
            myprop : String
        },
        data() {
            return {
                awesome : true,
                color : true,
                numbers : 10,
                count: 0
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>