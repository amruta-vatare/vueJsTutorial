<template>
    <table style="width:400px">
  <tr>
    <th>1st Number</th>
    <th>2nd Number</th>
    <th>Addition</th>
  </tr>
  <tr>
    <td>
        <input type="number" v-model.number="num1"/>
    </td>
    <td>
        <input type="number" v-model.number="num2"/>
    </td>
    <td>
        <span>{{result}}</span>
    </td>
  </tr>
  <tr>
    <td>
        <select name="cars" id="cars" v-model="name">
            <option value="volvo">Volvo</option>
            <option value="saab">Saab</option>
            <option value="mercedes">Mercedes</option>
            <option value="audi">Audi</option>
        </select>
    </td>
    <td> <p v-if="name">My favorite kind of car is {{ name }}</p></td>
  </tr>
</table>
</template>
<script>
export default{
    name:'NumberAddition',
    props:{},
    data(){
        return{
            num1 : 0,
            num2 : 0,
            result: 0,
            name: ''
        }
    },
    methods:{
        addNum(){
            this.result = this.num1 + this.num2;
        }
    },
    watch: {
        num1(newValue, oldValue) {
            this.addNum();
      console.log(`The counter has changed! It was ${oldValue}, it's now ${newValue}`)
    },
    num2(newValue, oldValue) {
        this.addNum();
        console.log(`The counter has changed! It was ${oldValue}, it's now ${newValue}`)
    }
  }
}
</script>