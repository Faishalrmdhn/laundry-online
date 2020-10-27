<template>
  <b-container class="mainContainer" fluid>
    <b-row class="navbar"
      ><div class="i">
        <img
          style="max-width: 150px"
          src="../assets/brand.png"
          alt="brand logo"
        />
      </div>
      <div class="i"></div>
      <div class="i"></div>
      <div class="i" style="text-align: center; cursor: pointer">
        <b-icon icon="calendar2-date-fill"></b-icon> Make Appointment
      </div></b-row
    >
    <!-- content,carousel,gallery,testi -->
    <b-row class="contentWrapper"
      ><b-col cols="12" class="content"
        ><b-row align-h="center"
          ><b-col cols="8">
            <h1>Fresh Laundry - Husein Sastranegara</h1>
            <p>Laundry Office Hour :</p>
            <p>Open until 17.00</p></b-col
          ></b-row
        >
        <b-row align-h="center" class="mt-3"
          ><b-col cols="12"><h4>Product</h4> </b-col></b-row
        >
        <b-row align-h="center"
          ><b-col cols="8">
            <div>
              <b-carousel
                id="carousel-1"
                v-model="slide"
                :interval="3000"
                controls
                indicators
                background="#ababab"
                img-width="1024"
                img-height="480"
                style="text-shadow: 1px 1px 2px #333"
                @sliding-start="onSlideStart"
                @sliding-end="onSlideEnd"
              >
                <b-carousel-slide
                  caption="First slide"
                  text="Nulla vitae elit libero, a pharetra augue mollis interdum."
                  img-src="https://picsum.photos/1024/480/?image=52"
                ></b-carousel-slide>

                <b-carousel-slide
                  caption="First slide"
                  text="Nulla vitae elit libero, a pharetra augue mollis interdum."
                  img-src="https://picsum.photos/1024/480/?image=52"
                ></b-carousel-slide>
                <b-carousel-slide
                  caption="First slide"
                  text="Nulla vitae elit libero, a pharetra augue mollis interdum."
                  img-src="https://picsum.photos/1024/480/?image=52"
                ></b-carousel-slide>
              </b-carousel></div></b-col
        ></b-row>
        <b-row align-h="center" class="mt-3"
          ><b-col cols="6"><h4>Updates</h4></b-col></b-row
        >
        <b-row align-h="center"
          ><b-col cols="9">
            <b-card-group deck>
              <b-card
                title="Title"
                img-src="https://picsum.photos/300/300/?image=41"
                img-alt="Image"
                img-top
              >
                <b-card-text>
                  This is a wider card with supporting text below as a natural
                  lead-in to additional content. This content is a little bit
                  longer.
                </b-card-text>
                <template #footer>
                  <small class="text-muted">Last updated 3 mins ago</small>
                </template>
              </b-card>

              <b-card
                title="Title"
                img-src="https://picsum.photos/300/300/?image=41"
                img-alt="Image"
                img-top
              >
                <b-card-text>
                  This card has supporting text below as a natural lead-in to
                  additional content.
                </b-card-text>
                <template #footer>
                  <small class="text-muted">Last updated 3 mins ago</small>
                </template>
              </b-card>

              <b-card
                title="Title"
                img-src="https://picsum.photos/300/300/?image=41"
                img-alt="Image"
                img-top
              >
                <b-card-text>
                  This is a wider card with supporting text below as a natural
                  lead-in to additional content. This card has even longer
                  content than the first to show that equal height action.
                </b-card-text>
                <template #footer>
                  <small class="text-muted">Last updated 3 mins ago</small>
                </template>
              </b-card>
            </b-card-group></b-col
          ></b-row
        >
        <b-row align-h="center" class="mt-3"
          ><b-col cols="6"><h4>Laundry Result</h4> </b-col></b-row
        >
        <b-row align-h="center" class="mt-3"
          ><b-col cols="6"><h4>Testimoni</h4> </b-col></b-row
        >
      </b-col>
    </b-row>
    <b-row class="footer"><b-col cols="12">footer</b-col></b-row>
  </b-container>
</template>

<script>
export default {
  name: "home",
  components: {},
  data() {
    return {
      slide: 0,
      sliding: null,
    };
  },
  methods: {
    onSlideStart(slide) {
      this.sliding = true;
      console.log(slide);
    },
    onSlideEnd(slide) {
      this.sliding = false;
      console.log(slide);
    },
  },
};
</script>

<style scoped>
.mainContainer {
  width: 100%;
  height: auto;
  /* background-color: white; */
}

.navbar {
  background-color: white;
  display: flex;
  flex-grow: row nowrap;
  box-shadow: 5px 5px 5px grey;
  position: sticky;
  top: 0px;
  z-index: 2;
}

.i {
  flex-grow: 1;
}

.contentWrapper {
  margin-top: 30px;
  /* background-color: blue; */
  text-align: center;
  height: 100%;
}

h4 {
  text-decoration: underline;
  text-decoration-style: solid;
}
/* .content {
  background-color: red;
} */

/* .footer {
  margin-top: auto;
} */
</style>
