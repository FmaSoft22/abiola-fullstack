<template>
  <div>
    <v-tabs v-model="tab" centered flat hide-slider color="primary">
      <v-tab :ripple="false" v-for="item in tabItems" :key="item.id">{{
        item.name
      }}</v-tab>
    </v-tabs>

    <v-tabs-items v-model="tab">
      <v-tab-item v-for="item in tabContent" :key="item.id">
        <CoolLightBox
          :items="item.content"
          :index="index"
          :fullScreen="true"
          :effect="'fade'"
          @close="index = null"
        >
        </CoolLightBox>
        <div
          class="gallery-wrapper gallery-grid mesonry-list grid-metro3"
          id="animated-thumbnials"
        >
          <div
            v-for="(item, i) in item.content"
            :key="i"
            @click="index = i"
            class="image masonry_item portfolio-33-33"
          >
            <div class="item-portfolio-static ">
              <div class="portfolio-static">
                <div class="thumbnail-inner">
                  <div class="thumbnail">
                    <img :src="item.thumb" alt="portfolio image" />
                  </div>
                </div>

                <div class="content">
                  <div class="inner">
                    <p>{{ item.tag }}</p>
                    <h4><a target="_blank" :href="item.url">{{ item.title }}</a></h4>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </v-tab-item>
    </v-tabs-items>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        tab: null,
        index: null,
        tabItems: [
          {
            id: 1,
            name: "Tout les projets",
          },
          {
            id: 2,
            name: "Site Web",
          },
          {
            id: 4,
            name: "Application Mobile",
          },
        ],
        tabContent: [
          {
            id: 1,
            content: [
              {
                thumb: require("../../assets/images/portfolio/dp-portfolio-08.png"),
                src: require("../../assets/images/portfolio/big/dp-big-portfolio-08.png"),
                tag: "Site Web",
                title: `AfricaUSE-SiteWeb`,
                description:`Plate-forme Internet Multiservices  de gestion de fidélité commerciale, offres d’emploi, taxi,
vente entre particuliers (annonces)`,
                url:`https://www.africause.com`
              },
              {
                thumb: require("../../assets/images/portfolio/dp-portfolio-02.png"),
                src: require("../../assets/images/portfolio/big/dp-big-portfolio-02.png"),
                tag: "Application Mobile",
                title: `AfricaUSE-AppMobile`,
                description:`Application mobile Plate-forme Internet Multiservices  de gestion de fidélité commerciale AfricaUSE`,
                url:`https://www.africause.com/Multimedia/Apps/obatrade.app.africause.apk`
              },
              {
                thumb: require("../../assets/images/portfolio/dp-portfolio-03.png"),
                src: require("../../assets/images/portfolio/big/dp-big-portfolio-03.png"),
                tag: "Site Web",
                title: `Site web Lavage-Auto Sté EGCLEAN (Lyon,France)`,
                url:`http://www.egclean.fr`
              },
              {
                thumb: require("../../assets/images/portfolio/dp-portfolio-04.png"),
                src: require("../../assets/images/portfolio/big/dp-big-portfolio-04.png"),
                tag: "Site Web",
                title: `Site web Catalogue Produits Sté Lodeci-Meuble`,
                url:`https://www.lodedi-meuble.com`
              },
              {
                thumb: require("../../assets/images/portfolio/dp-portfolio-03.jpg"),
                src: require("../../assets/images/portfolio/big/dp-big--portfolio-03.jpg"),
                tag: "Site Web",
                title: `Site Web pour SPA (Salon de beauté, Maquillage)`,
                url:`https://www.lodedi-meuble.com`
              },
              {
                thumb: require("../../assets/images/portfolio/dp-portfolio-03.jpg"),
                src: require("../../assets/images/portfolio/big/dp-big--portfolio-03.jpg"),
                tag: "Site Web",
                title: `Site Web Générateur de CV`,
                url:`https://www.lodedi-meuble.com`
              },
            ],
          },
          {
            id: 2,
            content: [
              {
                thumb: require("../../assets/images/portfolio/dp-portfolio-08.png"),
                src: require("../../assets/images/portfolio/big/dp-big-portfolio-08.png"),
                tag: "Site Web",
                title: `AfricaUSE-SiteWeb`,
                description:`Plate-forme Internet Multiservices  de gestion de fidélité commerciale, offres d’emploi, taxi,
vente entre particuliers (annonces)`,
                url:`https://www.africause.com`
              },
              {
                thumb: require("../../assets/images/portfolio/dp-portfolio-03.png"),
                src: require("../../assets/images/portfolio/big/dp-big-portfolio-03.png"),
                tag: "Site Web",
                title: `Site web Lavage-Auto Sté EGCLEAN (Lyon,France)`,
                url:`http://www.egclean.fr`
              },
              {
                thumb: require("../../assets/images/portfolio/dp-portfolio-04.png"),
                src: require("../../assets/images/portfolio/big/dp-big-portfolio-04.png"),
                tag: "Site Web",
                title: `Site web Catalogue Produits Sté Lodeci-Meuble`,
                url:`https://www.lodedi-meuble.com`
              },
              {
                thumb: require("../../assets/images/portfolio/dp-portfolio-03.jpg"),
                src: require("../../assets/images/portfolio/big/dp-big--portfolio-03.jpg"),
                tag: "Site Web",
                title: `Site Web pour SPA (Salon de beauté, Maquillage)`,
                url:`https://www.lodedi-meuble.com`
              },
              {
                thumb: require("../../assets/images/portfolio/dp-portfolio-03.jpg"),
                src: require("../../assets/images/portfolio/big/dp-big--portfolio-03.jpg"),
                tag: "Site Web",
                title: `Site Web Générateur de CV (Projet Scolaire pour étudiant)`,
                url:`https://www.lodedi-meuble.com`
              },
            ],
          },
          {
            id: 3,
            content: [
              {
                thumb: require("../../assets/images/portfolio/dp-portfolio-02.png"),
                src: require("../../assets/images/portfolio/big/dp-big-portfolio-02.png"),
                tag: "Application Mobile",
                title: `AfricaUSE-AppMobile`,
                description:`Application mobile Plate-forme Internet Multiservices  de gestion de fidélité commerciale AfricaUSE`,
                url:`https://www.africause.com/Multimedia/Apps/obatrade.app.africause.apk`
              },
            ],
          },
          {
            id: 4,
            content: [
              {
                thumb: require("../../assets/images/portfolio/dp-portfolio-01.jpg"),
                src: require("../../assets/images/portfolio/big/dp-big--portfolio-01.jpg"),
                tag: "Mobile App",
                title: `T-shirt design is the part of design`,
              },
              {
                thumb: require("../../assets/images/portfolio/dp-portfolio-03.jpg"),
                src: require("../../assets/images/portfolio/big/dp-big--portfolio-03.jpg"),
                tag: "Mobile App",
                title: `Mobile App landing Design`,
              },
              {
                thumb: require("../../assets/images/portfolio/dp-portfolio-05.jpg"),
                src: require("../../assets/images/portfolio/big/dp-big--portfolio-05.jpg"),
                tag: "Mobile App",
                title: `Getting tickets to the big show`,
              },
            ],
          },
        ],
      };
    },
  };
</script>
