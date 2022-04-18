<template>
  <div>
    <div v-if="this.tweetList == true">
    <ul class="tweet-list">
      <li>
    <div class="tweet-box" v-for="tweet in tweets" :key="tweet.id">
   <p> {{tweet.message }}</p>
   <p> {{tweet.user }}</p>
   <p> {{tweet.dateCreated }}</p>
    </div>
      </li>
    </ul>
    </div>
    <div v-else>
    <div class="tweet-grid">
    <div class="tweet-box" v-for="tweet in tweets" :key="tweet.id">
   <p> {{tweet.message }}</p>
   <p> {{tweet.user }}</p>
   <p> {{tweet.dateCreated }}</p>
    </div>
    </div>

   
    </div>
<button v-on:click="onToggle">Test</button>
  </div>
</template>

<script>
export default {
  name: "HomePage",
  methods: {
onToggle: function(){
  this.tweetList = !this.tweetList
}
  },
  data() {
    let tweetList = false

    return {
      tweetList,

            tweets: [
        {
          message:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quasi corporis consequuntur voluptatem voluptas itaque incidunt dolor eligendi magni quae esse iste, quam, fuga ratione tempora.",
          user: "BroodVX",
          dateCreated: "04/12/2022",
          id: 0
        },
        {
          message:
            "Lorem ipsum sit amet consectetur adipisicing elit. Quasi corporis consequuntur voluptatem voluptas itaque incidunt dolor eligendi magni quae esse iste, quam, fuga ratione tempora.",
          user: "Bdude",
          dateCreated: "04/11/2022",
              id: 1
        },
        {
          message:
            "Lorem ipsum dolor amet consectetur adipisicing elit. Quasi corporis consequuntur voluptatem voluptas itaque incidunt dolor eligendi magni quae esse iste, quam, fuga ratione tempora.",
          user: "Zheal",
          dateCreated: "04/10/2022",
              id: 2
        },
        {
          message:
            "Lorem ipsum dolor sit consectetur adipisicing elit. Quasi corporis consequuntur voluptatem voluptas itaque incidunt dolor eligendi magni quae esse iste, quam, fuga ratione tempora.",
          user: "Dyne",
          dateCreated: "04/09/2022",
              id: 3
        },
        {
          message:
            "Lorem ipsum dolor sit amet adipisicing elit. Quasi corporis consequuntur voluptatem voluptas itaque incidunt dolor eligendi magni quae esse iste, quam, fuga ratione tempora.",
          user: "MrsBrood",
          dateCreated: "04/08/2022",
              id: 4
        },
      ],
    };
  },
};
</script>

<style  scoped>
.tweet-grid{
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  
}

.tweet-box{

border: 2px solid black;
}

.tweet-list{
  list-style: none;
}
</style>
