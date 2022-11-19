<template>
        <ul>
        <li v-for="comment in comments" :key="comment">
        {{ comment }}
        </li>
        </ul>
    <input v-model="newComment" @keyup.enter="addComment" placeholder="Add a comment" />
  </template>
<script>
export default{
    name:" Exercise2Vue",
    props:{},
    data(){
        return{
                newComment: '',
                comments: [
            'Looks great Julianne!',
            'I love the sea',
            'Where are you at?'
            ]
        }

    },
    methods:{
        addComment() {
      this.comments.push(this.newComment)
      this.newComment = ''
    }
    }
}
</script>