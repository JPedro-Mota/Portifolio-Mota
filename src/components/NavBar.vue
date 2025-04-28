<template>
  <div class="menu-container">
    <v-card
      class="custom-tabs"
      elevation="0"
    >

      <v-tabs
        bg-color="black"
        class="rounded-tabs"
        fixed-tabs
        grow
      >
        <v-tab style="font-size: 12px; font-family: 'Gowun Dodum', sans-serif;" text="HOME" />
        <v-tab style="font-size: 12px; font-family: 'Gowun Dodum', sans-serif;" text="COMPETÊNCIAS" />
        <v-tab style="font-size: 12px; font-family: 'Gowun Dodum', sans-serif;" text="EXPERIÊNCIA" />
        <v-tab style="font-size: 12px; font-family: 'Gowun Dodum', sans-serif;" text="PROJETOS" />
        <v-tab style="font-size: 12px; font-family: 'Gowun Dodum', sans-serif;" text="CONTATO" />
      </v-tabs>
    </v-card>
  </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Gruppo&display=swap');

.menu-container {
  display: flex;
  justify-content: center;
  position: relative;
  z-index: 1;
}

.custom-tabs {
  border: 1px solid #ffffff33; /* Borda branca com transparência */
  border-bottom-left-radius: 30px;
  border-bottom-right-radius: 30px;
  background-color: black;
  display: inline-block;
  padding: 0;

}

.rounded-tabs {
  border-bottom-left-radius: 20px;
  border-bottom-right-radius: 20px;
  overflow: hidden;
  display: flex;

}
</style>
