<template>
  <div>
    <FilterCheckbox filtertoptitle="Dubai Hotels By Star Rating">
      <template slot="checkboxLoopData">
        <div
          class="border-bottom"
          v-for="staring in starings"
          :key="staring.index"
        >
          <div class="checkbox-heading">
            <label :for="staring.uniqid"> {{ staring.name }} </label>
            <span class="float-right">
              <input
                class="checkbox-edit"
                type="checkbox"
                :id="staring.uniqid"
              />
              <label :for="staring.uniqid"></label>
            </span>
          </div>
        </div>
        <div class="showMore invisible mt-2">
          <a href="#" class="font-weight-bold">Show More</a>
        </div>
      </template>
    </FilterCheckbox>
  </div>
</template>

<script>
import FilterCheckbox from "@/components/listcomponents/FilterCheckbox.vue";
export default {
  name: "NavBar",
  components: {
    FilterCheckbox
  },
  data() {
    return {
      starings: [
        {
          name: "5 Star",
          uniqid: "2star5"
        },
        {
          name: "4 Star",
          uniqid: "2star4"
        },
        {
          name: "3 Star",
          uniqid: "2star3"
        }
      ]
    };
  }
};
</script>

<style scoped lang="scss">
@import "../../assets/scss/_rvariables.scss";
.checkboxfilter {
  background-color: #ffffff;
  font-size: 10px;
  color: $dimfont;
  height: 162px;
  padding: 0px;
}

label {
  margin: 0;
  cursor: pointer;
}

input[type="checkbox"] + label {
  display: block;
  cursor: pointer;
}

input[type="checkbox"] {
  display: none;
}

input[type="checkbox"] + label:before {
  content: "\2714";
  border: 1px solid $dimfont;
  border-radius: 0px;
  display: inline-block;
  width: 18px;
  height: 18px;
  padding-left: 4px;
  padding-bottom: 4px;
  vertical-align: bottom;
  color: transparent;
  transition: 0.2s;
}

input[type="checkbox"]:checked + label:before {
  background-color: $orangebtn;
  border-color: $orangebtn;
  color: #fff;
}
</style>
