<template>
  <div>
    <h2>This is the Blog Page</h2>
     <p>Entry 1</p>
     <p>Entry 2</p>
     <p>Entry 3</p>

     <button v-if="showText" @click ="switchViews()">Text is shown only when True</button>
     <button v-else @click ="switchViews()">Text switches when false</button>

    <div class="container">
            <div class="entry" v-for="entry in entries" :key="entry.id">
              <h3>{{ entry.title }}</h3>
              <p> {{ entry.description}} </p>
              <p> {{ entry.content}} </p>

             </div>
    </div>
  </div>
</template>

<script>
export default {
    data() {
     return {
        showText: true,
        entries: [ {
           "id": 1, 
           "title": "Title-1",
           "description": "this is blog entry-1",
           "content": "This is the content of my entry 1"
        },
        {
           "id": 2, 
           "title": "Title-2",
           "description": "this is blog entry-2",
           "content": "This is the content of my entry 1"
        }, 
        {
           "id": 3, 
           "title": "Title-3",
           "description": "this is blog entry-3",
           "content": "This is the content of my entry 1"
        },
       ]
    }
    },

    methods: {
    switchViews(){
        this.showText= !this.showText
    }
    }
};
</script>

<style>

</style>