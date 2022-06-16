<template>
  <div class="row mt_dec--30">
    <!-- Start Single Service  -->
    <v-col
      lg="4"
      md="4"
      sm="6"
      cols="12"
      class="mt--30"
      v-for="(service, i) in serviceContent"
      :key="i"
    >
      <div class="single-service service__style--2 bg-color-gray">
        <router-link to="/service-details">
          <div class="service">
            <div class="icon">
              <div v-html="iconSvg(service.icon)"></div>
            </div>
            <div class="content">
              <h3 class="heading-title">{{ service.title }}</h3>
              <p>
                {{ service.desc }}
              </p>
            </div>
          </div>
        </router-link>
      </div>
    </v-col>
    <!-- End Single Service  -->
  </div>
</template>

<script>
  import feather from "feather-icons";
  export default {
    data() {
      return {
        serviceContent: [
          {
            icon: "cast",
            title: "Développement Site Web",
            desc: `HTML 5, CSS 3, JS, JQUERY, PHP, C#, DART(En formation), Symfony, Laravel(Moyen), C# .NET 4.5(MVC, LINQ, ENTIFY FRAMEWORK etc..),
             BULMA, BOOTSTRAP, ANIMATE JS, TAIWIND CSS(Apprentissage)`,
          },
          {
            icon: "monitor",
            title: "Dévelopment Application Mobile",
            desc: `React Native(1 projet en équipe), Flutter (En Apprentissage).`,
          },
          {
            icon: "monitor",
            title: "DevOps & Cloud(En formation)",
            desc: `Quelques compétence en Docker et Kubernetes.(Niveau débuant)`,
          },
          {
            icon: "monitor",
            title: "Modélisation",
            desc: `OOP, UML, SCRUM, REST API, SOA`,
          },
          {
            icon: "monitor",
            title: "Design Web (En formation)",
            desc: `PhotoShop, Illustrator, InDesign, Adobe Xd, Figma, Canva(Au quotidien)`,
          },

        ],
      };
    },
    methods: {
      iconSvg(icon) {
        return feather.icons[icon].toSvg();
      },
    },
  };
</script>
