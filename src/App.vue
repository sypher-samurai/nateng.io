<template>
  <v-app>
    <v-app-bar app color="#25242f" dark elevation="0">
      <div class="d-flex align-center ml-md-6">
        <h3>Neteng.io</h3>
      </div>

      <v-spacer></v-spacer>

      <v-btn href="#" target="_blank" text>
        <span class="mr-2">H<span class="text-lowercase">ome</span></span>
      </v-btn>
      <v-btn href="#" target="_blank" text>
        <span class="mr-2">S<span class="text-lowercase">ervces</span></span>
      </v-btn>
      <v-btn href="#" target="_blank" text>
        <span class="mr-2">P<span class="text-lowercase">rojects</span></span>
      </v-btn>
      <v-btn href="#" target="_blank" text>
        <span class="mr-2"
          >A<span class="text-lowercase">bout</span> U<span
            class="text-lowercase"
            >s</span
          ></span
        >
      </v-btn>
    </v-app-bar>

    <v-main>
      <HelloWorld />
    </v-main>
    <v-footer padless color="#25242f" dark>
      <v-row
        justify="center"
        no-gutters
        class="d-flex align-center justify-space-between mx-4"
      >
        <h3 class="ml-3">
          neteng.io
        </h3>

        <div>
          <v-btn
            v-for="link in links"
            :key="link"
            color="white"
            text
            rounded
            class="my-2"
          >
            {{ link }}
          </v-btn>
        </div>
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",

  components: {
    HelloWorld,
  },

  data: () => ({
    links: ["Service", "Project", "About Us"],
  }),
};
</script>
<style scoped>
.theme--light.v-application {
  background: #25242f;
  color: rgb(253, 253, 255);
}
</style>
