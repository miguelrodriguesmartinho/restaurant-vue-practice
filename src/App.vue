<template>
  <div class="main-container">
    <Header />
    <Categories
      @update-category="updateCategory"
      :categories="getCategories"
      :selectedC="selectedCategory"
    />
    <Items @delete-item="deleteItem" :items="getItems" />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Categories from "./components/Categories.vue";
import Items from "./components/Items.vue";

export default {
  /* eslint-disable */
  name: "App",
  components: {
    Header,
    Categories,
    Items,
  },
  data() {
    return {
      items: [],
      selectedCategory: null,
    };
  },
  created() {
    this.items = [
      {
        id: 8640,
        title: "Lunch Menu",
        description: "Best Lunch Menu",
        id_suggestion_menu_items_menu_item: null,
        icon: {
          image:
            "https://pleezetiquetas.s3.eu-west-2.amazonaws.com/12591_Pleez_IconesMenu_acompanhamentos.png",
        },
        all_week: null,
        subcategories: [
          {
            id: 8641,
            title: "Lunch Menu",
            description: "Best Lunch Menu",
            id_category: 8640,
            menu_items: [
              {
                id: 26525,
                title: "Pumpkin Cream (Especial)",
                description: "",
                image:
                  "https://pleezetiquetas.s3.eu-west-2.amazonaws.com/gettyimages-825855446-612x612.jpg",
                price: 8,
                index: 0,
                dish_to_sell_more: false,
                most_popular: false,
                margin: 0,
                cost: 0,
                id_category_tag: 2,
                video: null,
                id_zonsoft: null,
                items_characteristic_tags: [
                  {
                    id: 690,
                    id_menu_items: 26525,
                    id_characteristics_tag: 7,
                    createdAt: "2022-01-26T15:28:41.000Z",
                    updatedAt: "2022-01-26T15:28:41.000Z",
                    characteristic_tag: {
                      id: 7,
                      label: "Feeling Hungry",
                      color: "#C0D9EF",
                      text_color: "#000000",
                    },
                  },
                  {
                    id: 691,
                    id_menu_items: 26525,
                    id_characteristics_tag: 13,
                    createdAt: "2022-01-26T15:28:41.000Z",
                    updatedAt: "2022-01-26T15:28:41.000Z",
                    characteristic_tag: {
                      id: 13,
                      label: "Popular",
                      color: "#DF9C9B",
                      text_color: "#FFFFFF",
                    },
                  },
                ],
                menu_items_modifiers: [
                  {
                    id: 139,
                    index: 0,
                    id_menu_item: 26525,
                    id_modifier_group: 5,
                    createdAt: "2022-01-26T15:28:41.000Z",
                    updatedAt: "2022-01-26T15:28:41.000Z",
                    modifier_group: {
                      id: 5,
                      name: "Canela",
                      multiple_choice: true,
                      modifiers: [
                        {
                          id: 11,
                          name: "Assada",
                          price: 1,
                          id_zonsoft: null,
                        },
                        { id: 12, name: "Frita", price: 2, id_zonsoft: null },
                      ],
                    },
                  },
                ],
              },
            ],
          },
        ],
      },
      {
        id: 6789,
        title: "Cold Drinks",
        description: "Cold Drinks",
        id_suggestion_menu_items_menu_item: {
          id: 26525,
          title: "Pumpkin Cream (Especial)",
          description: "",
          image:
            "https://pleezetiquetas.s3.eu-west-2.amazonaws.com/gettyimages-825855446-612x612.jpg",
          id_zonsoft: null,
          video: null,
          price: 8,
          index: 0,
          active: true,
          deleted: false,
          dish_to_sell_more: false,
          most_popular: false,
          margin: 0,
          cost: 0,
          id_nutricional_info: null,
          id_menu: 409,
          id_menu_categories: 8641,
          id_establishment: 201,
          id_category_tag: 2,
          createdAt: "2021-10-28T20:36:56.000Z",
          updatedAt: "2022-01-12T16:38:27.000Z",
        },
        icon: {
          image:
            "https://pleezetiquetas.s3.eu-west-2.amazonaws.com/12598_Pleez_IconesMenu_cafetaria.png",
        },
        all_week: null,
        subcategories: [
          {
            id: 6790,
            title: "Cold Drinks",
            description: "Cold Drinks",
            id_category: 6789,
            menu_items: [
              {
                id: 26526,
                title: "Vanilla Sweet Cream",
                description: null,
                image:
                  "https://pleezetiquetas.s3.eu-west-2.amazonaws.com/26526_12636_VanillaSweetCream.webp",
                price: 6.25,
                index: 0,
                dish_to_sell_more: false,
                most_popular: false,
                margin: 0,
                cost: 0,
                id_category_tag: 2,
                video: null,
                id_zonsoft: null,
                items_characteristic_tags: [
                  {
                    id: 747,
                    id_menu_items: 26526,
                    id_characteristics_tag: 5,
                    createdAt: "2022-02-10T12:06:49.000Z",
                    updatedAt: "2022-02-10T12:06:49.000Z",
                    characteristic_tag: {
                      id: 5,
                      label: "To Share",
                      color: "#F5D561",
                      text_color: "#000000",
                    },
                  },
                ],
                menu_items_modifiers: [
                  {
                    id: 142,
                    index: 0,
                    id_menu_item: 26526,
                    id_modifier_group: 5,
                    createdAt: "2022-02-10T12:06:49.000Z",
                    updatedAt: "2022-02-10T12:06:49.000Z",
                    modifier_group: {
                      id: 5,
                      name: "Canela",
                      multiple_choice: true,
                      modifiers: [
                        {
                          id: 11,
                          name: "Assada",
                          price: 1,
                          id_zonsoft: null,
                        },
                        { id: 12, name: "Frita", price: 2, id_zonsoft: null },
                      ],
                    },
                  },
                ],
              },
              {
                id: 26527,
                title: "Cold Brew",
                description: null,
                image:
                  "https://pleezetiquetas.s3.eu-west-2.amazonaws.com/26527_12634_ColdBew.jpg",
                price: 3,
                index: 0,
                dish_to_sell_more: false,
                most_popular: false,
                margin: 0,
                cost: 0,
                id_category_tag: 7,
                video: null,
                id_zonsoft: null,
                items_characteristic_tags: [],
                menu_items_modifiers: [
                  {
                    id: 112,
                    index: 0,
                    id_menu_item: 26527,
                    id_modifier_group: 5,
                    createdAt: "2021-12-27T11:34:18.000Z",
                    updatedAt: "2021-12-27T11:34:18.000Z",
                    modifier_group: {
                      id: 5,
                      name: "Canela",
                      multiple_choice: true,
                      modifiers: [
                        {
                          id: 11,
                          name: "Assada",
                          price: 1,
                          id_zonsoft: null,
                        },
                        { id: 12, name: "Frita", price: 2, id_zonsoft: null },
                      ],
                    },
                  },
                ],
              },
              {
                id: 26528,
                title: "Honey Almond Milk",
                description: null,
                image:
                  "https://pleezetiquetas.s3.eu-west-2.amazonaws.com/26528_12632_HoneyAlmondmilk.webp",
                price: 5,
                index: 0,
                dish_to_sell_more: false,
                most_popular: false,
                margin: 0,
                cost: 0,
                id_category_tag: 7,
                video: null,
                id_zonsoft: null,
                items_characteristic_tags: [],
                menu_items_modifiers: [
                  {
                    id: 113,
                    index: 0,
                    id_menu_item: 26528,
                    id_modifier_group: 5,
                    createdAt: "2021-12-27T11:34:18.000Z",
                    updatedAt: "2021-12-27T11:34:18.000Z",
                    modifier_group: {
                      id: 5,
                      name: "Canela",
                      multiple_choice: true,
                      modifiers: [
                        {
                          id: 11,
                          name: "Assada",
                          price: 1,
                          id_zonsoft: null,
                        },
                        { id: 12, name: "Frita", price: 2, id_zonsoft: null },
                      ],
                    },
                  },
                ],
              },
              {
                id: 26529,
                title: "Nitro Cream",
                description: null,
                image:
                  "https://pleezetiquetas.s3.eu-west-2.amazonaws.com/26529_12639_NitroCold.webp",
                price: 5.99,
                index: 0,
                dish_to_sell_more: false,
                most_popular: false,
                margin: 0,
                cost: 0,
                id_category_tag: 2,
                video: null,
                id_zonsoft: null,
                items_characteristic_tags: [],
                menu_items_modifiers: [
                  {
                    id: 114,
                    index: 0,
                    id_menu_item: 26529,
                    id_modifier_group: 5,
                    createdAt: "2021-12-27T11:34:18.000Z",
                    updatedAt: "2021-12-27T11:34:18.000Z",
                    modifier_group: {
                      id: 5,
                      name: "Canela",
                      multiple_choice: true,
                      modifiers: [
                        {
                          id: 11,
                          name: "Assada",
                          price: 1,
                          id_zonsoft: null,
                        },
                        { id: 12, name: "Frita", price: 2, id_zonsoft: null },
                      ],
                    },
                  },
                ],
              },
              {
                id: 26530,
                title: "Salted Caramel Cream",
                description: null,
                image:
                  "https://pleezetiquetas.s3.eu-west-2.amazonaws.com/26530_12637_SaltedCaramelCream.webp",
                price: 2.99,
                index: 0,
                dish_to_sell_more: false,
                most_popular: false,
                margin: 0,
                cost: 0,
                id_category_tag: 2,
                video: null,
                id_zonsoft: null,
                items_characteristic_tags: [],
                menu_items_modifiers: [
                  {
                    id: 115,
                    index: 0,
                    id_menu_item: 26530,
                    id_modifier_group: 5,
                    createdAt: "2021-12-27T11:34:18.000Z",
                    updatedAt: "2021-12-27T11:34:18.000Z",
                    modifier_group: {
                      id: 5,
                      name: "Canela",
                      multiple_choice: true,
                      modifiers: [
                        {
                          id: 11,
                          name: "Assada",
                          price: 1,
                          id_zonsoft: null,
                        },
                        { id: 12, name: "Frita", price: 2, id_zonsoft: null },
                      ],
                    },
                  },
                ],
              },
              {
                id: 26531,
                title: "Irish Cream",
                description: null,
                image:
                  "https://pleezetiquetas.s3.eu-west-2.amazonaws.com/26531_12635_IrishCream.jpg",
                price: 3.49,
                index: 0,
                dish_to_sell_more: false,
                most_popular: false,
                margin: 0,
                cost: 0,
                id_category_tag: 2,
                video: null,
                id_zonsoft: null,
                items_characteristic_tags: [],
                menu_items_modifiers: [
                  {
                    id: 116,
                    index: 0,
                    id_menu_item: 26531,
                    id_modifier_group: 5,
                    createdAt: "2021-12-27T11:34:18.000Z",
                    updatedAt: "2021-12-27T11:34:18.000Z",
                    modifier_group: {
                      id: 5,
                      name: "Canela",
                      multiple_choice: true,
                      modifiers: [
                        {
                          id: 11,
                          name: "Assada",
                          price: 1,
                          id_zonsoft: null,
                        },
                        { id: 12, name: "Frita", price: 2, id_zonsoft: null },
                      ],
                    },
                  },
                ],
              },
              {
                id: 26532,
                title: "Cordusio Coffe",
                description: null,
                image:
                  "https://pleezetiquetas.s3.eu-west-2.amazonaws.com/26532_12633_Cordusio.jpg",
                price: 1.5,
                index: 0,
                dish_to_sell_more: false,
                most_popular: false,
                margin: 0,
                cost: 0,
                id_category_tag: 2,
                video: null,
                id_zonsoft: null,
                items_characteristic_tags: [],
                menu_items_modifiers: [
                  {
                    id: 117,
                    index: 0,
                    id_menu_item: 26532,
                    id_modifier_group: 5,
                    createdAt: "2021-12-27T11:34:18.000Z",
                    updatedAt: "2021-12-27T11:34:18.000Z",
                    modifier_group: {
                      id: 5,
                      name: "Canela",
                      multiple_choice: true,
                      modifiers: [
                        {
                          id: 11,
                          name: "Assada",
                          price: 1,
                          id_zonsoft: null,
                        },
                        { id: 12, name: "Frita", price: 2, id_zonsoft: null },
                      ],
                    },
                  },
                ],
              },
              {
                id: 26533,
                title: "Iced Coffe",
                description: null,
                image:
                  "https://pleezetiquetas.s3.eu-west-2.amazonaws.com/26533_12631_IcedCoffe.webp",
                price: 4.75,
                index: 0,
                dish_to_sell_more: false,
                most_popular: false,
                margin: 0,
                cost: 0,
                id_category_tag: 2,
                video: null,
                id_zonsoft: null,
                items_characteristic_tags: [],
                menu_items_modifiers: [
                  {
                    id: 118,
                    index: 0,
                    id_menu_item: 26533,
                    id_modifier_group: 5,
                    createdAt: "2021-12-27T11:34:18.000Z",
                    updatedAt: "2021-12-27T11:34:18.000Z",
                    modifier_group: {
                      id: 5,
                      name: "Canela",
                      multiple_choice: true,
                      modifiers: [
                        {
                          id: 11,
                          name: "Assada",
                          price: 1,
                          id_zonsoft: null,
                        },
                        { id: 12, name: "Frita", price: 2, id_zonsoft: null },
                      ],
                    },
                  },
                ],
              },
              {
                id: 33606,
                title: "MBWAY Test",
                description: "",
                image:
                  "https://pleezetiquetas.s3.eu-west-2.amazonaws.com/unnamed.png",
                price: 0.1,
                index: 0,
                dish_to_sell_more: null,
                most_popular: null,
                margin: 0,
                cost: 0,
                id_category_tag: 2,
                video: null,
                id_zonsoft: null,
                items_characteristic_tags: [
                  {
                    id: 630,
                    id_menu_items: 33606,
                    id_characteristics_tag: 6,
                    createdAt: "2022-01-19T16:10:39.000Z",
                    updatedAt: "2022-01-19T16:10:39.000Z",
                    characteristic_tag: {
                      id: 6,
                      label: "Alcoholic ",
                      color: "#A63834",
                      text_color: "#FFFFFF",
                    },
                  },
                ],
                menu_items_modifiers: [],
              },
            ],
          },
        ],
      },
      {
        id: 6791,
        title: "Oatmeal & Yogurt",
        description: "Oatmeal & Yogurt",
        id_suggestion_menu_items_menu_item: {
          id: 26538,
          title: "Hearty Blueberry Oatmeal",
          description: null,
          image:
            "https://pleezetiquetas.s3.eu-west-2.amazonaws.com/26538_12642_HeartyBlueberryOatmeal.webp",
          id_zonsoft: null,
          video: null,
          price: 4.5,
          index: 13,
          active: true,
          deleted: false,
          dish_to_sell_more: false,
          most_popular: false,
          margin: 0,
          cost: 0,
          id_nutricional_info: null,
          id_menu: 409,
          id_menu_categories: 6792,
          id_establishment: 201,
          id_category_tag: 5,
          createdAt: "2021-10-28T20:36:57.000Z",
          updatedAt: "2022-01-09T23:57:39.000Z",
        },
        icon: {
          image:
            "https://pleezetiquetas.s3.eu-west-2.amazonaws.com/12715_Pleez_IconesMenu_shots.png",
        },
        all_week: null,
        subcategories: [
          {
            id: 6792,
            title: "Oatmeal & Yogurt",
            description: "Oatmeal & Yogurt",
            id_category: 6791,
            menu_items: [
              {
                id: 26535,
                title: "Bolo de chocolate com 5 camadas",
                description:
                  "Para gulosos! Feito com pão de ló embebido em café, recheio de ganache de chocolate, chantilly cremoso e puré de framboesa. É melhor pedir já 2 fatias!",
                image:
                  "https://pleezetiquetas.s3.eu-west-2.amazonaws.com/Bolo de chocolate.jpg",
                price: 5,
                index: 0,
                dish_to_sell_more: false,
                most_popular: false,
                margin: 0,
                cost: 0,
                id_category_tag: 5,
                video: null,
                id_zonsoft: null,
                items_characteristic_tags: [
                  {
                    id: 354,
                    id_menu_items: 26535,
                    id_characteristics_tag: 5,
                    createdAt: "2022-01-12T23:02:37.000Z",
                    updatedAt: "2022-01-12T23:02:37.000Z",
                    characteristic_tag: {
                      id: 5,
                      label: "To Share",
                      color: "#F5D561",
                      text_color: "#000000",
                    },
                  },
                  {
                    id: 355,
                    id_menu_items: 26535,
                    id_characteristics_tag: 7,
                    createdAt: "2022-01-12T23:02:37.000Z",
                    updatedAt: "2022-01-12T23:02:37.000Z",
                    characteristic_tag: {
                      id: 7,
                      label: "Feeling Hungry",
                      color: "#C0D9EF",
                      text_color: "#000000",
                    },
                  },
                  {
                    id: 356,
                    id_menu_items: 26535,
                    id_characteristics_tag: 13,
                    createdAt: "2022-01-12T23:02:37.000Z",
                    updatedAt: "2022-01-12T23:02:37.000Z",
                    characteristic_tag: {
                      id: 13,
                      label: "Popular",
                      color: "#DF9C9B",
                      text_color: "#FFFFFF",
                    },
                  },
                ],
                menu_items_modifiers: [
                  {
                    id: 134,
                    index: 0,
                    id_menu_item: 26535,
                    id_modifier_group: 5,
                    createdAt: "2022-01-12T23:02:37.000Z",
                    updatedAt: "2022-01-12T23:02:37.000Z",
                    modifier_group: {
                      id: 5,
                      name: "Canela",
                      multiple_choice: true,
                      modifiers: [
                        {
                          id: 11,
                          name: "Assada",
                          price: 1,
                          id_zonsoft: null,
                        },
                        { id: 12, name: "Frita", price: 2, id_zonsoft: null },
                      ],
                    },
                  },
                ],
              },
              {
                id: 26536,
                title: "Berry Trio Parfait",
                description: null,
                image:
                  "https://pleezetiquetas.s3.eu-west-2.amazonaws.com/26536_12641_Berry_Trio_Parfait.webp",
                price: 3.5,
                index: 0,
                dish_to_sell_more: false,
                most_popular: false,
                margin: 0,
                cost: 0,
                id_category_tag: 5,
                video: null,
                id_zonsoft: null,
                items_characteristic_tags: [],
                menu_items_modifiers: [
                  {
                    id: 121,
                    index: 0,
                    id_menu_item: 26536,
                    id_modifier_group: 5,
                    createdAt: "2021-12-27T11:34:18.000Z",
                    updatedAt: "2021-12-27T11:34:18.000Z",
                    modifier_group: {
                      id: 5,
                      name: "Canela",
                      multiple_choice: true,
                      modifiers: [
                        {
                          id: 11,
                          name: "Assada",
                          price: 1,
                          id_zonsoft: null,
                        },
                        { id: 12, name: "Frita", price: 2, id_zonsoft: null },
                      ],
                    },
                  },
                ],
              },
              {
                id: 26537,
                title: "Siggi's® Yogurt Cup 0% Vanilla",
                description: null,
                image:
                  "https://pleezetiquetas.s3.eu-west-2.amazonaws.com/26537_12644_Siggis_Yogurt_Cup_0_Vanilla.webp",
                price: 2.55,
                index: 0,
                dish_to_sell_more: false,
                most_popular: false,
                margin: 0,
                cost: 0,
                id_category_tag: 5,
                video: null,
                id_zonsoft: null,
                items_characteristic_tags: [],
                menu_items_modifiers: [
                  {
                    id: 123,
                    index: 0,
                    id_menu_item: 26537,
                    id_modifier_group: 5,
                    createdAt: "2021-12-27T11:34:19.000Z",
                    updatedAt: "2021-12-27T11:34:19.000Z",
                    modifier_group: {
                      id: 5,
                      name: "Canela",
                      multiple_choice: true,
                      modifiers: [
                        {
                          id: 11,
                          name: "Assada",
                          price: 1,
                          id_zonsoft: null,
                        },
                        { id: 12, name: "Frita", price: 2, id_zonsoft: null },
                      ],
                    },
                  },
                ],
              },
              {
                id: 26538,
                title: "Hearty Blueberry Oatmeal",
                description: null,
                image:
                  "https://pleezetiquetas.s3.eu-west-2.amazonaws.com/26538_12642_HeartyBlueberryOatmeal.webp",
                price: 4.5,
                index: 0,
                dish_to_sell_more: false,
                most_popular: false,
                margin: 0,
                cost: 0,
                id_category_tag: 5,
                video: null,
                id_zonsoft: null,
                items_characteristic_tags: [],
                menu_items_modifiers: [
                  {
                    id: 124,
                    index: 0,
                    id_menu_item: 26538,
                    id_modifier_group: 5,
                    createdAt: "2021-12-27T11:34:19.000Z",
                    updatedAt: "2021-12-27T11:34:19.000Z",
                    modifier_group: {
                      id: 5,
                      name: "Canela",
                      multiple_choice: true,
                      modifiers: [
                        {
                          id: 11,
                          name: "Assada",
                          price: 1,
                          id_zonsoft: null,
                        },
                        { id: 12, name: "Frita", price: 2, id_zonsoft: null },
                      ],
                    },
                  },
                ],
              },
              {
                id: 31763,
                title: "Salad",
                description: "Very good salad ",
                image: null,
                price: 29,
                index: 0,
                dish_to_sell_more: null,
                most_popular: null,
                margin: null,
                cost: null,
                id_category_tag: 5,
                video: null,
                id_zonsoft: null,
                items_characteristic_tags: [],
                menu_items_modifiers: [
                  {
                    id: 122,
                    index: 0,
                    id_menu_item: 31763,
                    id_modifier_group: 5,
                    createdAt: "2021-12-27T11:34:18.000Z",
                    updatedAt: "2021-12-27T11:34:18.000Z",
                    modifier_group: {
                      id: 5,
                      name: "Canela",
                      multiple_choice: true,
                      modifiers: [
                        {
                          id: 11,
                          name: "Assada",
                          price: 1,
                          id_zonsoft: null,
                        },
                        { id: 12, name: "Frita", price: 2, id_zonsoft: null },
                      ],
                    },
                  },
                ],
              },
            ],
          },
        ],
      },
    ];
  },
  computed: {
    getCategories() {
      const categories = [];

      this.items.forEach((element) => {
        const categorie = {
          id: element.id,
          title: element.title,
          image: element.icon.image,
        };
        categories.push(categorie);
      });
      return categories;
      // console.log(categories);
    },

    getItems() {
      const items = [];
      if (this.selectedCategory === null) {
        return [];
      }
      const category = this.items.find(
        (element) => element.title === this.selectedCategory
      );

      category.subcategories.forEach((subCategorie) => {
        subCategorie.menu_items.forEach((element) => {
          const obj = {
            subCategory: subCategorie.title,
            element: element,
          };
          items.push(obj);
        });
      });
      console.log(items);
      return items;
    },
  },
  methods: {
    deleteItem(id) {
      if (confirm("Are you sure ?")) {
        const items = [];

        this.items.forEach((category) => {
          category.subcategories.forEach((subCategorie) => {
            subCategorie.menu_items = subCategorie.menu_items.filter(
              (el) => el.id !== id
            );
          });
        });
      }
    },
    updateCategory(title) {
      this.selectedCategory = title;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.main-container {
  outline: 2px solid #2c3e50;
  max-width: 900px;
  margin: 0px auto;
  padding: 10px;
}
</style>
