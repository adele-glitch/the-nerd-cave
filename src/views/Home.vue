<template>
  <div class="home">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
      <div class="jumbotron custom-font">
      </div>
      <div class="container-overlay custom-font">
        <h1 class="display-4 text-center text-light">Fun for everyone</h1>
        <p class="lead text-center text-light">Table-top games, popular merchandise, comic books and more...</p>
      </div>

      <div class="container text-light text-center">
        <div class="row title-row"><h1 class="custom-font mx-auto">Events</h1></div>

        <div class="row">
          <div class="col-12 col-sm-4 pr-0 pl-0">
            <ul class="event-list list-group " role="tablist">
              <li class="list-group-item flex-fill" :class="{active: index === selectedIndex}" v-for="(item, index) in events" :key="index" @click="changeEventDay(index)">{{item.day}}</li>
            </ul>
          </div>
          <div class="col-12 col-sm-8 event-container">
            <h1 class="custom-font mx-auto">{{selectedEvent.time}}</h1>
            <p v-for="(item, index) in selectedEvent.events" :key="index">{{item}}</p>
          </div>
        </div>

      </div>

      <div class="container text-light">
        <div class="row title-row">
          <h1 class="custom-font mx-auto">Just In</h1>
        </div>
        <div class="row">
          <div class="col-12 col-sm-6 col-md-4 col-lg-3" v-for="(item, index) in newProducts" :key="index">
            <itemCard :product="item"/>
          </div>
        </div>
      </div>

      <div class="container text-light">
        <div class="row title-row">
          <h1 class="custom-font mx-auto">On Sale</h1>
        </div>
        <div class="row">
          <div class="col-12 col-sm-6 col-md-4 col-lg-3" v-for="(item, index) in itemsOnSale" :key="index">
            <itemCard :product="item"/>
          </div>
        </div>
      </div>
  </div>
</template>

<script>
// @ is an alias to /src
import itemCard from '@/components/itemCard.vue'

export default {
  name: 'Home',
  components: {
     itemCard
  },
  data: () => ({
    selectedIndex: 0,
    selectedEvent: {
        day: 'Wednesday',
        time: 'From 19h00',
        events: ['Magic the gathering: Commander', 'DnD League', 'Wargaming tables']
      },
    events: [
      {
        day: 'Wednesday',
        time: 'From 19h00',
        events: ['Magic the gathering: Commander', 'DnD League', 'Wargaming tables']
      },
      {
        day: 'Thursday',
        time: 'From 19h00',
        events: ['Magic the gathering: Pioneer', 'Wargaming tables']
      },
      {
        day: 'Friday',
        time: 'From 19h00',
        events: ['Magic the gathering', 'Yu-Gi-Oh!: Tournament', 'Pokemon: Casual', 'Wargaming tables']
      },
      {
        day: 'Saturday',
        time: 'From 9h30 to 17h00',
        events: ['Pokemon: League', 'Special events', 'Wargaming tables']
      },
      {
        day: 'Sunday',
        time: 'From 10h00 to 15h00',
        events: ['Magic the gathering: Commander and Pauper', 'Wargaming tables']
      }
    ],
    newProducts: [],
    itemsOnSale: []
  }),
  created(){
    //dummy data Yay!
    for (let i = 0; i < 8; i++) {
      this.newProducts.push({
        itemName: 'Descent into Avernus',
        imageUrl: 'descentIntoAvernus.jpg',
        onSale: false,
        price: '780.00'
      })
    }
    for (let i = 0; i < 4; i++) {
      this.itemsOnSale.push({
        itemName: 'Descent into Avernus',
        imageUrl: 'descentIntoAvernus.jpg',
        onSale: true,
        price: '450.00'
      })
    }
    console.log(this.itemsOnSale);
  },
  methods: {
    changeEventDay(index){
      console.log(this.itemsOnSale);
      this.selectedIndex = index
      this.selectedEvent = this.events[index]
    }
  }
}
</script>
