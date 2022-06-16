<template>
  <v-row class="row--35" align="center">
    <v-col lg="5" md="5" cols="12">
      <div class="thumbnail">
        <slot name="thum-img"></slot>
      </div>
    </v-col>
    <v-col lg="7" md="7" cols="12">
      <div class="about-inner inner pt--100 pt_sm--40 pt_md--40">
        <div class="section-title">
          <h2 class="heading-title">A propos de moi</h2>
          <p class="description">
            Développeur full Stack avec <strong style="color:#f9004d;font-weight: bold;">3 ans d’expérience</strong>. Polyvalent, j’ai
            une bonne connaissance des différentes étapes techniques de la
            création d’un site ou d’une application web, de la compréhension
            des besoins utilisateurs au développement frontend et backend
            en passant par la maintenance.<br/><br/>
            Passionné par les maths,les sujets de réflexion, les challenges, j'ai toute suite opté pour la filière Informatique et Génie logiciel
            après mon parcour scolaire car je me disais c'était le seul domaine où je pouvais solutions à mes maux.
            <br/><br/>
            Je me distingue par ma créativité, mon sens de travail accompli, ma soif d'apprendre au jour le jour.
            Ma curiosité et mon ouverture d'exprit me permettent de me perfectionner d'avantage et chercher à découvrir d'autre horizon dans un domaine aussi vaste qu'est l'informatique.
            <br/><!--<br/>C'est d'ailleur ce qui m'a poussé en 2016  à commander depuis la france près de 20 livres en informatique (UML, SCRUM, C#, C++, PHP, JAVASCRIPT,JQUERY, JAVA, ANDROID, .NET, SQL SERVER, MYQSL, MVVM (WFP),SYMFONY etc...) dans le but de me perfectionner d'avantage.-->
          </p>
        </div>
        <!-- End .section-title -->
        <div class="tab-wrapper mt--30">
          <v-row>
            <TabTwo />
          </v-row>
        </div>
      </div>
    </v-col>
  </v-row>
</template>

<script>
  import TabTwo from "../../components/tabs/TabTwo";
  export default {
    components: { TabTwo },
    data() {
      return {};
    },
  };
</script>
