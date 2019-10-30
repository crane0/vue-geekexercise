<template>
  <div>
    <h2>2.6 新语法</h2>
    <SlotDemo>
      <p>默认插槽</p>
      <template v-slot:title>
        <p>title slot1</p>
        <p>title slot2</p>
      </template>
      <template v-slot:title>
        <p>new title slot1</p>
        <p>new title slot2</p>
      </template>
      <p>我也是默认插槽</p>
      <template v-slot:item="props">
        <p>item slot-scope {{ props }}</p>
      </template>
      <template v-slot:item="props">
        <p>new item slot-scope {{ props }}</p>
      </template>
    </SlotDemo>
    <br />
    <h2>老语法</h2>
    <SlotDemo>
      <p>默认插槽</p>
      <p slot="title">title slot1</p>
      <p slot="title">new title slot2</p>
      <p>我也是默认插槽</p>
      <p slot="item" slot-scope="props">item slot-scope {{ props }}</p>
      <p slot="item" slot-scope="props">new item slot-scope {{ props }}</p>
    </SlotDemo>
  </div>
</template>

<script>
import Slot from "./Slot";
export default {
  components: {
    SlotDemo: Slot,
  },
};
</script>
