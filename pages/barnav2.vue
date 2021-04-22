<template>
  <v-container fluid>
    <v-card class="">
      <v-app-bar
        color="#6A76AB"
        dark
        shrink-on-scroll
        prominent
        src="https://picsum.photos/1920/1080?random"
        fade-img-on-scroll
        scroll-target="#scrolling-techniques-3"
        width="100vw"
      >
        <template v-slot:img="{ props }">
          <v-img
            v-bind="props"
            gradient="to top right, rgba(100,115,201,.7), rgba(25,32,72,.7)"
          ></v-img>
        </template>

        <v-app-bar-nav-icon />

        <v-toolbar-title>Title</v-toolbar-title>

        <v-spacer />

        <v-btn icon>
          <v-icon>mdi-magnify</v-icon>
        </v-btn>

        <v-btn icon>
          <v-icon>mdi-heart</v-icon>
        </v-btn>

        <v-btn icon>
          <v-icon>mdi-dots-vertical</v-icon>
        </v-btn>

        <template v-slot:extension>
          <v-tabs align-with-title>
            <v-tab>Tab 1</v-tab>
            <v-tab>Tab 2</v-tab>
            <v-tab>Tab 3</v-tab>
          </v-tabs>
        </template>
      </v-app-bar>
      <v-sheet
        id="scrolling-techniques-3"
        class="overflow-y-auto"
        height="90vh"
        color="yellow"
        opacity="0.5"
      >
        <v-main>
          <!--<v-container class="bord-green" style="height: 100vh;">-->
            <p>Hallu tation</p>
            <p>Hallu tation</p>

            <p>Hallu tation 1</p>

            <p>Hallu tation 2</p>

            <p>Hallu tation 3</p>

            <p>Hallu tation 4</p>
            <p>Hallu tation 5</p>
            <p>Hallu tation 6</p>

            <p>Hallu tation 7</p>

            <p>Hallu tation 8</p>

            <p>Hallu tation 9</p>

            <p>Hallu tation 10</p>
            <p>Hallu tation 11</p>
            <p>Hallu tation 12</p>

            <p>Hallu tation 13</p>

            <p>Hallu tation 14</p>

            <p>Hallu tation 15</p>

            <p>Hallu tation 16</p>
            <p>Hallu tation 17</p>
            <p>Hallu tation 18</p>

            <p>Hallu tation 19</p>

            <p>Hallu tation 20</p>

            <p>Hallu tation 21</p>

            <p>Hallu tation 22</p>
          <!--</v-container>-->
        </v-main>
      </v-sheet>
    </v-card>
  </v-container>
</template>

<style>
.bord-green {
  border: 4px solid green;
  background-color: aquamarine;
  opacity: 0.5;
}
p {
  color: red;
}
</style>
