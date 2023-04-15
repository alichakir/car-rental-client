<template>
  <div
    id="carouselExampleCaptions"
    class="carousel slide"
    data-bs-ride="carousel"
  >
    <div class="carousel-inner">
      <InnerCarousel
        v-for="image in carousel"
        :key="image.title"
        :img="image.img"
        :title="image.title"
        :text="image.text"
      />
    </div>
  </div>
</template>

<script>
import InnerCarousel from "@/components/widgets/InnerCarousel.vue";
export default {
  components: { InnerCarousel },
  data() {
    return {
      carousel: [
        {
          img: require("@/assets/img/hero1.jpg"),
          title: "Excellent Customer Service /Excellent service client",
          text: " excellent customer service, including professional staff, prompt response to customer issues 24/7/   un excellent service client, y compris un personnel professionnel, une réponse rapide  aux problèmes des clients 24h/7j.",
        },
        {
          img: require("@/assets/img/hero2.jpg"),
          title: "Competitive Pricing/Prix compétitifs :",
          text: " Our rental car company offers competitive pricing options, including daily, weekly, and monthly rates, as well as special promotions and discounts./ Notre société de location de voitures propose des options de prix compétitifs, notamment des tarifs journaliers, hebdomadaires et mensuels, ainsi que des promotions et des remises spéciales. ",
        },
        {
          img: require("@/assets/img/hero3.jpg"),
          title: "Flexible Rental Terms / Nos termes de location sont flexibles:",
          text: " flexible rental terms, such as options for short-term and long-term rentals, one-way rentals, and multiple drop-off locations./les conditions de location flexibles, telles que les options de location à court et à long terme, les locations à sens unique et les lieux de dépôt multiples.",
        },
        {
          img: require("@/assets/img/hero4.jpg"),
          title: "Your comfort/votre confrot",
          text: "Your comfort is our priority/votre confort est notre preorite",
        },
      ],
    };
  },
};
</script>

<style></style>
