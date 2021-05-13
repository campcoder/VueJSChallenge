<template>
  <div class="parent">
    <table>
      <tr>
        <td><div class="itemContainerTitle">Interner Bedarf</div></td>
        <td></td>
        <td><div class="itemContainerTitle">Einkaufswagen</div></td>
      </tr>
      <tr>
        <td class="itemContainer">
          <draggable :list="internalneeds" group="items">
            <div v-for="element in internalneeds" :key="element.orderName">
              <div class="itemView">
                <p class="itemDetailView">
                  {{ element.orderName }}<br />{{
                    element.orderDate.substring(0, 10)
                  }}
                </p>
              </div>
            </div>
          </draggable>
        </td>
        <td class="separator"></td>
        <td class="itemContainer">
          <draggable :list="shoppingcart" group="items">
            <div v-for="element in shoppingcart" :key="element.orderName">
              <div class="itemView">
                <p class="itemDetailView">
                  {{ element.orderName }}<br />{{
                    element.orderDate.substring(0, 10)
                  }}
                </p>
              </div>
            </div>
          </draggable>
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
//import draggable from "vuedraggable";
import { VueDraggableNext } from "vue-draggable-next";

export default {
  name: "Body",
  components: { draggable: VueDraggableNext },
  data() {
    return {
      internalneeds: [
        {
          orderName: "orderItem 1",
          orderDate: "2021-04-30T23:00:00+0000",
        },
        {
          orderName: "orderItem 2",
          orderDate: "2021-04-30T23:00:00+0000",
        },
        {
          orderName: "orderItem 3",
          orderDate: "2021-04-30T23:00:00+0000",
        },
        {
          orderName: "orderItem 4",
          orderDate: "2021-04-30T23:00:00+0000",
        },
      ],
      shoppingcart: [
        {
          orderName: "orderItem 5",
          orderDate: "2021-04-30T23:00:00+0000",
        },
        {
          orderName: "orderItem 6",
          orderDate: "2021-04-30T23:00:00+0000",
        },
        {
          orderName: "orderItem 7",
          orderDate: "2021-04-30T23:00:00+0000",
        },
        {
          orderName: "orderItem 8",
          orderDate: "2021-04-30T23:00:00+0000",
        },
      ],
    };
  },
};
</script>

<style scoped>
.itemView {
  border-radius: 5px;
  width: 140px;
  height: 50px;
  background-color: lightgray;
  margin-top: 10px;
}
.itemContainer {
  width: 40%;
}

.itemDetailView {
  padding-left: 10px;
}

.itemContainerTitle {
  text-decoration: underline;
  font-weight: bold;
  text-align: center;
}

table {
  margin-left: auto;
  margin-right: auto;
}
.parent {
  width: 100%;
}
.separator {
  width: 20%;
}
</style>
