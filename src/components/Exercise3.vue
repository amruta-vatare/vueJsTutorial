<template>
    <div id="app">
        <h3>Sort titles by :</h3>
    <table style="border:none; border-collapse:collapse; cellspacing:0; cellpadding:0">
        <tr><td> <button @click="sortLowest">Lowest Rated</button></td><td> <button @click="sortHighest">Highest Rated</button></td></tr>
    </table>
    <table>
        <thead>
            <tr>
                <th v-for="key in columns" :key="key">{{key}}</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="entry in ratingsInfo" :key="entry">
                <td v-for="key in columns" :key="key">
                    {{entry[key]}}
                </td>
            </tr>
        </tbody>
    </table>
    </div>
</template>
<style>
    body, button {
  font-family: 'Bitter', serif;
}

#app {
  padding: 30px;
  max-width: 400px;
  font-size: 15px;
  margin: 0 auto;
}

table {
  background: #444;
  color: white;
}

th {
  background: #333;
  text-transform: capitalize;
  text-align: left;
}

td, th {
  padding: 10px;
  border-bottom: 1px solid #888;
}

td:first-child {
  width: 300px;
  border-right: 1px solid #888;
}

tr:last-child:td {
    border-bottom: none;
}

button {
  background: orangered;
  border: none;
  padding: 5px 8px;
  border-radius: 4px;
  cursor: pointer;
  margin-right: 10px;
}
</style>
<script>
    export default{
        name: "ExerciseThree",
        props:{},
        data(){
            return{
                columns:["title","rating"],
                ratingsInfo:[
                { title: `White Chicks`, rating: 82 },
        { title: `Grey's Anatomy`, rating: 98 },
        { title: `Prison Break`, rating: 98 },
        { title: `How I Met Your Mother`, rating: 94 },
        { title: `Supernatural`, rating: 95 },
        { title: `Breaking Bad`, rating: 97 },
        { title: `The Vampire Diaries`, rating: 91 },
        { title: `The Walking Dead`, rating: 98 },
        { title: `Pretty Little Liars`, rating: 96 },
        { title: `Once Upon a Time`, rating: 98 },
        { title: `Sherlock`, rating: 95 },
        { title: `Death Note`, rating: 77 },
        { title: `Naruto`, rating: 88 },
        { title: `Arrow`, rating: 96 },
        { title: `Black Mirror`, rating: 80 },
        { title: `The Originals`, rating: 74 },
        { title: `The 100`, rating: 97 },
        { title: `Masha and the Bear`, rating: 81 },
        { title: `Hunter X Hunter`, rating: 57 },
        { title: `Marvel's Luke Cage`, rating: 95 },
        { title: `Marvel's Iron Fist`, rating: 98 }
                ]
            }
        },
        methods:{
            sortLowest() {
                this.ratingsInfo.sort((a, b) => a.rating > b.rating ? 1 : -1);
            },
            sortHighest() {
                this.ratingsInfo.sort((a, b) => a.rating < b.rating ? 1 : -1);
            },
        }
    }
</script>