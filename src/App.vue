<template>
  <div id="app" class="has-background-primary">
    <section>
      <div class="container py-6 px-6">
        <div class="columns">
          <div class="column is-4" v-for="pricing in pricings" v-bind:key="pricing.id">
            <PricingTable>
              <template slot="header">
                <h1 class="title is-1">{{pricing.plan}}</h1>
                <h2 class="subtitle is-5">{{pricing.price}}</h2>
              </template>
              <template slot="body">
                <ul>
                  <li v-for="(feature, index) in pricing.features" v-bind:key="index">{{feature}}</li>
                </ul>
              </template>
              <template slot="footer">
                <button class="button is-primary mt-5">Buy Now</button>
              </template>
            </PricingTable>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import PricingTable from "./components/PricingTable";
export default {
  name: "App",
  components: { PricingTable },
  data() {
    return {
      pricings: [
        {
          id: 1,
          plan: "FREE",
          price: "$0/month",
          features: [
            "Single User",
            "5GB Storage",
            "Unlimited Public Projects",
            "Community Access",
            "Unlimited Private Projects",
            "Dedicated Phone Support",
            "Free 1 Subdomain",
            "Weekly Status Reports"
          ]
        },
        {
          id: 2,
          plan: "PLUS",
          price: "$9/month",
          features: [
            "5 Users",
            "50GB Storage",
            "Unlimited Public Projects",
            "Community Access",
            "Unlimited Private Projects",
            "Dedicated Phone Support",
            "Free 2 Subdomain",
            "Monthly Status Reports"
          ]
        },
        {
          id: 3,
          plan: "PRO",
          price: "$49/month",
          features: [
            "Unlimited Users",
            "150GB Storage",
            "Unlimited Public Projects",
            "Community Access",
            "Unlimited Private Projects",
            "Dedicated Phone Support",
            "Unlimited Free Subdomain",
            "Monthly Status Reports"
          ]
        }
      ]
    };
  }
};
</script>

<style>
#app {
  min-height: 100vh;
  display: grid;
  align-items: center;
}
body {
  font-family: "Roboto";
}
ul {
  line-height: 200%;
}
</style>
