<template>
  <div>
    <NavbarR></NavbarR>
    <div class="body-div pt-1">
      <SearchArea></SearchArea>
      <b-container>
        <div class="div-85 mx-auto">
          <b-row class="px-0 m-0">
            <b-col md="3 pl-0 pt-2">
              <LeftsideTitle></LeftsideTitle>
              <CompoListSelector></CompoListSelector>
              <CheckboxComponentscroll></CheckboxComponentscroll>
              <CheckboxComponentscroll2
                filtertoptitle="Hotel Facilities"
              ></CheckboxComponentscroll2>
              <Filterinput></Filterinput>
              <CheckboxComponentnoscroll></CheckboxComponentnoscroll>
              <ListComponent></ListComponent>
            </b-col>
            <b-col md="9 p-0">
              <Hotelcard></Hotelcard>
            </b-col>
          </b-row>
        </div>
      </b-container>
    </div>
    <BottomFooter></BottomFooter>
  </div>
</template>

<script>
import NavbarR from "@/components/listcomponents/NavbarR.vue";
import SearchArea from "@/components/listcomponents/SearchArea.vue";
import Hotelcard from "@/components/listcomponents/Hotelcard.vue";
import LeftsideTitle from "@/components/listcomponents/LeftsideTitle.vue";
import CompoListSelector from "@/components/listcomponents/CompoListSelector.vue";
import CheckboxComponentscroll from "@/components/listcomponents/CheckboxComponentscroll.vue";
import CheckboxComponentscroll2 from "@/components/listcomponents/CheckboxComponentscroll2.vue";
import CheckboxComponentnoscroll from "@/components/listcomponents/CheckboxComponentnoscroll.vue";
import Filterinput from "@/components/listcomponents/Filterinput.vue";
import ListComponent from "@/components/listcomponents/ListComponent.vue";
import BottomFooter from "@/components/listcomponents/BottomFooter.vue";
export default {
  name: "NavBar",
  components: {
    NavbarR,
    SearchArea,
    Hotelcard,
    LeftsideTitle,
    CompoListSelector,
    CheckboxComponentscroll,
    CheckboxComponentscroll2,
    CheckboxComponentnoscroll,
    Filterinput,
    ListComponent,
    BottomFooter
  },
  data() {
    return {};
  }
};
</script>

<style scoped lang="scss">
@import "../assets/scss/_rvariables.scss";
.body-div {
  background-color: $bodybackgroundcolor !important;
  height: auto;

  .div-85 {
    width: 85%;
  }
}
</style>
