<template>
  <v-col lg="12">
    <div class="tab-default">
      <v-tabs v-model="tab" flat hide-slider>
        <v-tab v-for="item in items" :key="item.id" :ripple="false">
          {{ item.name }}
        </v-tab>
      </v-tabs>

      <v-tabs-items v-model="tab">
        <v-tab-item
          transition="fade-transition"
          v-for="item in tabContent"
          :key="item.id"
        >
          <v-card flat>
            <v-card-text>
              <div class="single-tab-content">
                <ul>
                  <li v-for="(item, i) in item.content" :key="i">
                    <router-link to="/service"
                      >{{ item.title }}
                      <span> - {{ item.name }}</span></router-link
                    >
                    {{ item.desc }}
                  </li>
                </ul>
              </div>
            </v-card-text>
          </v-card>
        </v-tab-item>
      </v-tabs-items>
    </div>
  </v-col>
</template>
<script>
  export default {
    data() {
      return {
        tab: null,
        items: [
          {
            id: 1,
            name: "Compétences",
          },
          {
            id: 3,
            name: "Experience Pro",
          },
          {
            id: 4,
            name: "Diplomes & Formations",
          },
        ],

        tabContent: [
          {
            id: 1,
            content: [
              {
                title: "Language de Programmation",
                name: "",
                desc: "C#, PHP, Java, JavaScript, Type \n" +
                    "Script,Dart(moyen)",
              },
              {
                title: "Langages de mise en forme",
                name: "",
                desc: "HTML 5, CSS3, TAILWIND CSS, \n" +
                    "JQUERY, BOOTSTRAP,BULMA",
              },
              {
                title: "Base de données",
                name: "",
                desc: "MYSQL, SQL SERVEUR",
              },
              {
                title: "Framework Front End",
                name: "",
                desc: "React JS (Moyen), Vue \n" +
                    "JS(Moyen), React\n" +
                    "Native, Mobx, ASP.NET 4.5, \n" +
                    "Laravel 8",
              },
              {
                title: "Architecture & Conception",
                name: "",
                desc: "UML, SCRUM, POO, GIT, SOA,REST",
              },
              {
                title: "Autres",
                name: "",
                desc: "Anglais technique, Permis B",
              },

            ],
          },
          {
            id: 2,
            content: [
              {
                title: "Réalisation d'un site web pour un Salon de beauté(SPA). Fonctionnalités Prise de contact , RDV en ligne, Notification RDV",
                name: "FMA-SOFT - Cotonou, Bénin",
                desc: "Juin 2022 – A aujourdhui",
              },
              {
                title: "Réalisation du site de la société EgClean (Société spécialisée dans le lavage sans eau de véhicule automobile legers). Fonctionnalités Prise de contact , RDV en ligne",
                name: "FMA-SOFT - Cotonou, Bénin",
                desc: "Juin 2022 – A aujourdhui",
              },
              {
                title: "Réalisation du site de la société Lodeci-Meuble (Vente de meubles, commerce générale et divers",
                name: "FMA-SOFT - Cotonou, Bénin",
                desc: "Mars 2022 – A aujourdhui",
              },
              {
                title: "Réalisation d'un générateur de CV pour étudiant en fin de formation",
                name: "FMA-SOFT - Cotonou, Bénin",
                desc: "Février 2022",
              },
              {
                title: "Réalisation d'une Plate-forme Internet Multiservices (Web et \n" +
                    "Mobile) de gestion de fidélité commerciale, offres d’emploi, taxi, \n" +
                    "vente entre particuliers (annonces)",
                name: "Obatrade - Grenoble, France",
                desc: "Mars 2019 –Novembre 2021",
              },
              {
                title: "Stagiaire Ingénieur informatique",
                name: "Winner",
                desc: "Février 2018 – Juin 2018",
              },
            ],
          },
          {
            id: 3,
            content: [
              {
                title: "Master en \n" +
                    "Informatique appliquée à la \n" +
                    "gestion des entreprises",
                name: "UPI-ONM",
                desc: "2017 - 2018",
              },
              {
                title: "Licence en \n" +
                    "Informatique appliquée à la \n" +
                    "gestion des entreprises",
                name: "UPI-ONM",
                desc: "2015 - 2016",
              },
              {
                title: "BTS en informatique appliquée à la \n" +
                    "gestion des entreprises",
                name: "IS-FOPASE",
                desc: "2014- 2015",
              },
            ],
          },
          {
            id: 4,
            content: [
              {
                title: "BSc In CSE",
                name: "ABC Institute, Los Angeles, CA",
                desc: "2009",
              },
              {
                title: "Diploma in Computer Science",
                name: "Gamma Technical Institute",
                desc: "2009",
              },
              {
                title: "Graphic Designer",
                name: "ABC Institute, Los Angeles, CA",
                desc: "2007",
              },
            ],
          },
        ],
      };
    },
  };
</script>
