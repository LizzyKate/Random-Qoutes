<template>
  <div class="container">
    <div class="row max-height align-items-center">
      <div class="col-11 mx-auto col-md-6 quote-container p-5">
        <button
          class="btn-outline-primary text-capitalize my-4 d-block mx-auto"
          id="generate-btn" v-on:click="changeQuote()"
        >generate quote</button>

        <h3 class="text-muted">
          <span class="quote-icon mr-3">
            <i class="fas fa-quote-left fa-3x"></i>
          </span>
          <span id="quote">
            {{words}}
          </span>
          <i class="fas fa-quote-right fa-3x"></i>
        </h3>
        <h5 class="text-right text-capitalize author">
          -
          <span class="quote-author ml-3">{{writer}}</span>
        </h5>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      quotes:[
        {
      quote:
        "Life is too short and sweet to be spent by cribbing and complaining about things. Here are some random quotes about the most wonderful gift that we've got",
      author: " Life"
    },
    {
      quote:
        "Humor is richly rewarding to the person who employs it. It has some value in gaining and holding attention. But it has no persuasive value at all",
      author: "John Kenneth Galbraith"
    },
    {
      quote:
        "God save me from my friends. I can protect myself from my enemies.",
      author: "Claude Louis Hector de Villars "
    },
    {
      quote: "The price of anything is the amount of life you exchange for it.",
      author: "David Thoreau"
    },
    {
      quote:
        "Life is like a landscape. You live in the midst of it but can describe it only from the vantage point of distance. ",
      author: "Charles Lindbergh"
    },
    {
      quote:
        "A critic is someone who never actually goes to the battle, yet who afterwards comes out shooting the wounded.",
      author: " Tyne Daly"
    }
      ],
      writer:'author',
      words:'lorem ipsum dolor sit amet consecteur, adipisicing elit. Tenetur sint iste option placeat dolor labore, reprehenderit.'
    };
  },
  methods:{
    changeQuote(){
      let random = Math.floor(Math.random() * this.quotes.length);
      this.words = this.quotes[random].quote;
      this.writer= this.quotes[random].author;
    }
  }
};
</script>

<style>
.max-height {
  min-height: 100vh;
}
body {
  background: #b09e99;
}
.quote-container {
  background: rgba(255, 255, 255, 0.5);
}
#generate-btn {
  color: white !important;
  background: #64b6ac !important;
  border-color: #64b6ac !important;
  cursor: pointer;
  font-size: 1.5rem;
  padding: 0.5rem 1rem;
}
#generate-btn:hover {
  background: #b09e99 !important;
  border-color: #b09e99 !important;
  color: #333333 !important;
}
.author {
  color: #64b6ac;
}
</style>
