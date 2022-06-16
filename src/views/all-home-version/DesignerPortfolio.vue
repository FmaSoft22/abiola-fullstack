<template>
  <div>
    <_HeaderSection></_HeaderSection>
    <!-- Start Slider Area  -->
    <div class="slider-wrapper">
      <div
        class="slide designer-portfolio slider-style-3  d-flex align-center justify-center bg_color--5 rn-slider-height"
      >
        <BannerTwo />
      </div>
    </div>
    <div class="section about-area rn-section-gap bg_color--1" id="about">
      <div class="about-wrapper">
        <v-container>
          <AboutFour>
            <img
                slot="thum-img"
                class="w-100"
                src="../../assets/images/about/about-8.png"
                alt="About Images"
            />
          </AboutFour>
        </v-container>
      </div>
    </div>
    <div
        class="section rn-service-area service-area rn-section-gap bg_color--5"
        id="service"
    >
      <v-container>
        <v-row>
          <v-col lg="12">
            <div
                class="section-title service-style--3 text-center mb--20 mb_sm--0 md_md--0"
                id="skill"
            >
              <h2 class="heading-title">Domaine de Compétences</h2>
            </div>
          </v-col>
        </v-row>
        <ServiceThree />
      </v-container>
    </div>
    <div
        class="section rn-portfolio-area rn-section-gap bg_color--1"
        id="projet"
    >
      <v-container>
        <v-row>
          <v-col lg="12">
            <div class="section-title section-title--2 text-center mb--20">
              <h2 class="heading-title">
                Projets réalisés</h2>
            </div>
          </v-col>
        </v-row>
        <PortfolioThree />
      </v-container>
    </div>
    <!-- End Portfolio Area -->
    <!-- Start Contact Area  -->
    <div
        class="section rn-contact-area rn-section-gap bg_color--1"
        id="contact"
    >
      <div class="contact-form--1">
        <v-container>
          <Contact>
            <img
                slot="contact-img"
                class="w-100"
                src="../../assets/images/about/about-6.jpg"
                alt="trydo"
            />
          </Contact>
        </v-container>
      </div>
    </div>
    <!-- End Contact Area  -->
    <!-- Start Footer Area  -->
    <Footer />
    <!-- End Footer Area  -->
  </div>
</template>
<script>
  import HeaderTwo from "../../components/header/HeaderTwo";
  import BannerTwo from "../../components/slider/BannerTwo";
  import PortfolioThree from "../../components/portfolio/PortfolioThree";
  import Footer from "../../components/footer/FooterTwo";
  import _HeaderSection from "@/components/header/_HeaderSection";
  import HeaderOnePageTwo from "@/components/header/HeaderOnePageTwo";
  import BannerThree from "../../components/slider/BannerThree";
  import AboutFour from "../../components/about/AboutFour";
  import ServiceThree from "../../components/service/ServiceThree";
  import PortfolioTwo from "../../components/portfolio/PortfolioFour";
  import Blog from "../../components/blog/Blog";
  import Contact from "../../components/contact/Contact";

  export default {
    components: {
      HeaderTwo,
      _HeaderSection,
      BannerTwo,
      BannerThree,
      AboutFour,
      ServiceThree,
      PortfolioTwo,
      Blog,
      Contact,
      PortfolioThree,
      HeaderOnePageTwo,
      Footer,
    },
    data() {
      return {};
    },
  };
</script>
