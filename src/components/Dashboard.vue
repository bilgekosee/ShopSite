<template>
  <v-container fluid>
    <v-card
      color="#3D5A80"
      height="150px"
      tile
      flat
      class="d-flex align-center justify-center"
      dark
    >
      <v-row>
        <v-col cols="12" sm="12">
          <h4 class="text-center">ANIME LIFESTYLE SHOES</h4>
        </v-col>
        <v-col cols="12" sm="12">
          <v-breadcrumbs :items="items" class="justify-center mt-n7" dark>
            <template v-slot:divider>
              <v-icon color="#98C1D9">mdi-chevron-right</v-icon>
            </template>
          </v-breadcrumbs>
        </v-col>
      </v-row>
    </v-card>
    <v-card tile class="mx-16 mt-n10 card1" color="#cce3de">
      <v-row>
        <v-col cols="12" sm="8" class="pr-0">
          <v-card height="250px" tile flat color="#0d3b66">
            <v-row>
              <v-col cols="12" sm="4" class="pl-8 pt-5">
                <v-btn color="#293241" dark class="withoutuppercase" small tile
                  >New
                </v-btn>
                <h6 class="white--text mt-8">ANIME DREAMS</h6>
                <h3 class="white--text mt-5">Anime Cosplay Concept</h3>
                <v-btn
                  rounded
                  color="#1b263b"
                  dark
                  class="withoutuppercase px-8 mt-5"
                  >More Info</v-btn
                >
              </v-col>
              <v-col cols="12" sm="8">
                <v-img
                  src="cosplay.png"
                  max-height="250"
                  width="800px"
                  contain
                  class="mt-n3"
                ></v-img>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
        <v-col cols="12" sm="4" class="pl-0">
          <v-card height="250px" tile flat color="#218380">
            <v-row>
              <v-col cols="12" sm="6" class="pl-8 pt-5">
                <v-btn color="#293241" dark class="withoutuppercase" small tile>
                  new
                </v-btn>
                <h6 class="white--text mt-8">HOODIE</h6>
                <h3 class="white--text mt-5">Sale Collection 2023</h3>
                <v-btn
                  rounded
                  color="#21825D"
                  dark
                  class="withoutuppercase px-8 mt-5"
                  >More Info</v-btn
                >
              </v-col>
              <v-col cols="12" sm="6">
                <v-img
                  src="hoodie.png"
                  max-height="250"
                  width="310"
                  contain
                  class="mt-n3"
                ></v-img>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12" sm="3" class="mt-n6 pr-0">
          <v-toolbar flat outlined>
            <v-toolbar-title><strong>Filter</strong></v-toolbar-title>
            <v-spacer></v-spacer>
            <v-divider vertical></v-divider>
            <v-btn icon class="ml-1">
              <v-icon color="#525252"> mdi-sync </v-icon>
            </v-btn>
          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n6 px-0">
          <v-toolbar flat outlined>
            <v-toolbar-title>
              SPORT BY : <span>Price €-$$</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn icon class="mr-4">
              <v-icon color="#293241">mdi-menu-down</v-icon>
            </v-btn>
          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n6 px-0">
          <v-toolbar flat outlined class="">
            <v-toolbar-title>SHOW : <span>12</span></v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn icon class="mr-4">
              <v-icon color="#293241">mdi-menu-down</v-icon>
            </v-btn>
          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n6 pl-0">
          <v-toolbar flat outlined>
            <v-btn icon class="mr-1">
              <v-icon color="#293241">mdi-apps</v-icon>
            </v-btn>
            <v-divider vertical></v-divider>
            <v-btn icon class="mx-1">
              <v-icon color="#293241">mdi-format-list-bulleted</v-icon>
            </v-btn>
            <v-divider vertical></v-divider>
            <v-toolbar-title class="ml-2">
              <strong>COMPARE :</strong>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-badge color="#EE6C4D" content="4" class="mr-3"></v-badge>
          </v-toolbar>
        </v-col>
        <v-col cols="3" class="py-0 pr-0 mt-n3">
          <v-card flat outlined tile>
            <v-toolbar flat>
              <v-icon color="#293241" class="mr-2">mdi-chevron-down</v-icon>
              <strong>CATEGORIES</strong>
              <v-spacer></v-spacer>
              <v-icon color="#525252" small>mdi-close</v-icon>
            </v-toolbar>
            <v-list dense class="mt-n5">
              <v-list-item v-for="style in styles" :key="style.title">
                <v-list-item-content>
                  <v-list-item-title
                    v-text="style.title"
                    class="ml-8"
                  ></v-list-item-title>
                </v-list-item-content>
                <v-list-item-action>
                  <v-list-item-subtitle
                    v-text="style.count"
                  ></v-list-item-subtitle>
                </v-list-item-action>
              </v-list-item>
            </v-list>
          </v-card>
          <v-card flat outlined tile>
            <v-toolbar flat>
              <v-icon color="#293241" class="mr-2">mdi-chevron-down</v-icon>
              <strong>PRICE</strong>
              <v-spacer></v-spacer>
              <v-icon color="#525252" small>mdi-close</v-icon>
            </v-toolbar>
            <v-toolbar flat>
              <v-text-field
                placeholder="$50"
                filled
                rounded
                dense
                class="mx-2"
              ></v-text-field>
              <v-text-field
                placeholder="$1500"
                filled
                rounded
                dense
                class="mx-2"
              ></v-text-field>
            </v-toolbar>
            <v-range-slider color="#0E3837" max="40" min="30"></v-range-slider>
          </v-card>
          <v-card flat outlined tile>
            <v-toolbar flat>
              <v-icon color="#293241" class="mr-2">mdi-chevron-down</v-icon>
              <strong>BRAND</strong>
              <v-spacer></v-spacer>
              <v-icon color="#525252" small>mdi-close</v-icon>
            </v-toolbar>
            <v-list dense class="mt-n5">
              <v-list-item v-for="brand in brands" :key="brand.title">
                <v-list-item-content>
                  <v-list-item-title
                    v-text="brand.title"
                    class="ml-6"
                  ></v-list-item-title>
                </v-list-item-content>
                <v-list-item-action>
                  <v-checkbox
                    color="#EE6C4D"
                    v-model="brand.state"
                  ></v-checkbox>
                </v-list-item-action>
              </v-list-item>
            </v-list>
          </v-card>
          <v-card flat outlined tile>
            <v-toolbar flat>
              <v-icon color="#293241" class="mr-2">mdi-chevron-down</v-icon>
              <strong>COLOR</strong>
              <v-spacer></v-spacer>
              <v-icon color="#525252" small>mdi-close</v-icon>
            </v-toolbar>
            <v-chip-group column multiple>
              <v-chip
                filter
                outlined
                color="#293241"
                text-color="black"
                class="ml-2"
              ></v-chip>
              <v-chip filter color="#4cc9f0" text-color="black"></v-chip>
              <v-chip filter color="#ffea00" text-color="black"></v-chip>
              <v-chip filter color="#000000" text-color="white"></v-chip>
              <v-chip filter color="#540b0e" text-color="white"></v-chip>
              <v-chip filter color="#97a97c" text-color="white"></v-chip>
              <v-chip filter color="#34623f" text-color="black"></v-chip>
              <v-chip
                filter
                color="#a480cf"
                text-color="black"
                class="ml-2"
              ></v-chip>
              <v-chip filter color="#a4133c" text-color="black"></v-chip>
              <v-chip filter color="#3c096c" text-color="white"></v-chip>
              <v-chip filter color="#583101" text-color="white"></v-chip>
              <v-chip filter color="#ff9b54" text-color="black"></v-chip>
              <v-chip filter color="#1f363d" text-color="white"></v-chip>
              <v-chip filter color="#d00000" text-color="white"></v-chip>
            </v-chip-group>
          </v-card>
          <v-card flat outlined>
            <v-toolbar flat>
              <v-icon color="#293241" class="mr-2">mdi-chevron-down</v-icon>
              <strong>SIZE</strong>
              <v-spacer></v-spacer>
              <v-icon color="#525252" small>mdi-close</v-icon>
            </v-toolbar>
            <v-chip-group
              column
              multiple
              active-class="purple white--text"
              class="ml-2"
            >
              <v-chip
                v-for="size in sizes"
                :key="size"
                :value="size"
                class="size"
              >
                {{ size }}</v-chip
              >
            </v-chip-group>
          </v-card>
        </v-col>
        <v-col cols="9" class="mt-n3">
          <v-row>
            <v-col
              cols="12"
              sm="4"
              v-for="(clothe, i) in clothes"
              :key="i"
              :class="clothe.class"
            >
              <v-hover v-slot:default="{ hover }">
                <v-card height="300" justify="center" flat outlined tile>
                  <v-card-actions>
                    <v-spacer></v-spacer>
                    <v-btn color="#293241" small dark>{{ clothe.sold }}</v-btn>
                  </v-card-actions>
                  <v-img
                    :src="clothe.image"
                    width="200"
                    height="200"
                    contain
                  ></v-img>
                  <v-card-text class="mt-n4">
                    <strong :class="hover ? 'red--text' : 'black--text'">{{
                      clothe.title
                    }}</strong>
                  </v-card-text>
                  <v-expand-transition>
                    <div
                      v-if="hover"
                      class="
                        d-flex
                        transition-fast-in-fast-out
                        blue
                        v-card--reveal
                        display-3
                        white--text
                      "
                      style="height: 100%"
                    >
                      <v-btn rounded color="white">
                        <v-icon>mdi-cart-outlined</v-icon>
                        Buy
                      </v-btn>
                      <v-btn fab small color="white" class="ml-2">
                        <v-icon color="black">mdi-content-copy</v-icon>
                      </v-btn>
                      <v-btn fab small color="white" class="ml-2">
                        <v-icon color="black">mdi-heart-outline</v-icon>
                      </v-btn>
                    </div>
                  </v-expand-transition>
                </v-card>
              </v-hover>
            </v-col>
          </v-row>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n3 pr-0 pb-0">
          <v-toolbar flat outlined></v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n3 px-0 pb-0">
          <v-toolbar flat outlined>
            <v-btn icon class="mr-1">
              <v-icon color="grey">mdi-chevron-up</v-icon>
            </v-btn>
            <v-divider vertical></v-divider>
          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n3 px-0 pb-0">
          <v-toolbar flat outlined class="text-center">
            <v-pagination
              v-model="page"
              :length="4"
              color="#4B5958"
            ></v-pagination>
          </v-toolbar>
        </v-col>
        <v-col cols="12" sm="3" class="mt-n3 pl-0 pb-0">
          <v-toolbar flat outlined>
            <v-btn icon class="mr-1">
              <v-icon color="grey">mdi-chevron-down</v-icon>
            </v-btn>
            <v-divider vertical></v-divider>
          </v-toolbar>
        </v-col>
      </v-row>
    </v-card>
    <v-card
      color="#3D5A80"
      height="250px"
      tile
      flat
      dark
      class="d-flex align-center justify-center mt-n10 card2"
    >
      <v-row>
        <v-col cols="12" sm="12">
          <h4 class="text-center black--text mt-10">
            SUBSCRIBE TO OUR NEWSLETTER
          </h4>
        </v-col>
        <v-col cols="12" sm="12">
          <h6 class="text-center grey-text">
            Hello everyone, first of all, welcome to my site. If you like the
            shoes, I have good news for you. If you want, you can custom design
            shoes. It is our pleasure to prepare the shoes you designed for you.
          </h6>
        </v-col>
        <v-col cols="12" sm="12">
          <v-card flat color="transparent" class="d-flex justify-center">
            <v-text-field
              placeholder="Enter Your Email"
              rounded
              class="shrink"
              background-color="grey"
              filled
              append-icon="mdi-email-outline"
              dense
            ></v-text-field>
          </v-card>
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    page: 1,
    items: [
      {
        text: "Home",
        disabled: false,
        href: "breadcrumbs_home",
      },
      {
        text: "Catalog",
        disabled: false,
        href: "breadcrumbs_catalog",
      },
      {
        text: "Anime",
        disabled: false,
        href: "breadcrumbs_anime",
      },
      {
        text: "Shoes",
        disabled: false,
        href: "breadcrumbs_shoes",
      },
    ],
    styles: [
      {
        title: "My Heo Academia",
        count: "1",
      },
      {
        title: "Attack On Titan",
        count: "23",
      },
      {
        title: "Demon Slayer",
        count: "45",
      },
      {
        title: "Tokyo Ghoul",
        count: "11",
      },
      {
        title: "Naruto",
        count: "15",
      },
      {
        title: "One Piece",
        count: "32",
      },
      {
        title: "Hunter Hunter",
        count: "8",
      },
      {
        title: "Tokyo Revengers",
        count: "15",
      },
      {
        title: "Dororo",
        count: "22",
      },
    ],
    brands: [
      {
        title: "Converse",
        state: true,
      },
      {
        title: "GUCCI",
        state: false,
      },
      {
        title: "Nike",
        state: true,
      },
      {
        title: "Adidas",
        state: false,
      },
    ],
    sizes: [
      "31",
      "32",
      "33",
      "34",
      "35",
      "36",
      "37",
      "38",
      "39",
      "40",
      "41",
      "42",
      "43",
      "44",
      "45",
      "46",
    ],
    clothes: [
      {
        class: "pa-0",
        sold: "-20%",
        image: "1.png",
        title: "One piece",
        price: "$ 145.00",
      },
      {
        class: "pa-0",
        sold: "-30%",
        image: "2.png",
        title: "Blue Hair Anime Boy",
        price: "$ 599.00",
      },
      {
        class: "py-0 pl-0",
        sold: "-17%",
        image: "3.png",
        title: "Anime Boys",
        price: "$ 190.00",
      },
      {
        class: "pa-0",
        sold: "-22%",
        image: "4.png",
        title: "Tanjiro",
        price: "$ 220.00",
      },
      {
        class: "pa-0",
        sold: "-18%",
        image: "5.png",
        title: "Naruto",
        price: "$ 235.00",
      },
      {
        class: "py-0 pl-0",
        sold: "-40%",
        image: "6.png",
        title: "Zenitsu",
        price: "$ 190.00",
      },
      {
        class: "pa-0",
        sold: "-13%",
        image: "7.png",
        title: "My Hero Academia",
        price: "$ 230.00",
      },
      {
        class: "pa-0",
        sold: "-15%",
        image: "8.png",
        title: "Karashi",
        price: "$ 185.00",
      },
      {
        class: "py-0 pl-0",
        sold: "-10%",
        image: "9.png",
        title: "Naruto",
        price: "$ 265.00",
      },
      {
        class: "pa-0",
        sold: "-19%",
        image: "10.png",
        title: "Wen Anime",
        price: "$ 190.00",
      },
      {
        class: "pa-0",
        sold: "-16%",
        image: "11.png",
        title: "Anime Girl",
        price: "$ 175.00",
      },
      {
        class: "py-0 pl-0",
        sold: "-10%",
        image: "12.png",
        title: "My Hero Academia",
        price: "$ 245.00",
      },
    ],
  }),
};
</script>

<style>
.container {
  padding: 0px !important;
}
.v-btn.withoutuppercase {
  text-decoration: none;
}
.v-chip.v-size--default {
  border-radius: 50px !important;
  font-size: 14px !important;
  height: 40px !important;
  width: 40px !important;
}
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: 0.5;
  position: absolute;
  width: 100%;
}
.card1 {
  z-index: 10;
}
.card2 {
  z-index: 1;
}
</style>