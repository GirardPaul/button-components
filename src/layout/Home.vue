<script setup>
import Sidebar from "../components/Sidebar.vue";
import Button from "../components/Button.vue";
import { ref } from "vue";

const btnDefault = ref("<Button />");
const btnOutline = ref('<Button variant="outline" />');
const btnText = ref('<Button variant="text" />');
const btnDisableShadow = ref("<Button disableShadow />");
const btnDisabled = ref("<Button disabled />");
const btnVariantDisabled = ref('<Button variant="text" disabled />');
const btnStartIcon = ref('<Button startIcon="local_grocery_store" />');
const btnEndIcon = ref('<Button endIcon="local_grocery_store" />');
const btnSm = ref('<Button size="sm" />');
const btnMd = ref('<Button size="md" />');
const btnLg = ref('<Button size="lg" />');
const btnColorDefault = ref('<Button color="default" />');
const btnColorPrimary = ref('<Button color="primary" />');
const btnColorSecondary = ref('<Button color="secondary" />');
const btnColorDanger = ref('<Button color="danger" />');
</script>

<template>
  <div class="flex">
    <Sidebar />
    <div class="full flex flex-column buttons-container">
      <h3>Buttons</h3>
      <div class="flex flex-wrap">
        <div class="col">
          <p>{{ btnDefault }}</p>
          <Button>Default</Button>
        </div>
      </div>
      <div class="flex flex-wrap mt-45">
        <div class="col">
          <p>{{ btnOutline }}</p>
          <Button variant="outline">Default</Button>
        </div>
      </div>
      <div class="flex flex-wrap mt-45">
        <div class="col">
          <p>{{ btnText }}</p>
          <Button variant="text">Default</Button>
        </div>
      </div>
      <div class="flex flex-wrap mt-45">
        <div class="col">
          <p>{{ btnDisableShadow }}</p>
          <Button disableShadow>Default</Button>
        </div>
      </div>
      <div class="flex flex-wrap mt-45">
        <div class="col">
          <p>{{ btnDisabled }}</p>
          <Button disabled>Default</Button>
        </div>
        <div class="col">
          <p>{{ btnVariantDisabled }}</p>
          <Button variant="text" disabled>Default</Button>
        </div>
      </div>
      <div class="flex flex-wrap mt-45">
        <div class="col">
          <p>{{ btnStartIcon }}</p>
          <Button startIcon="local_grocery_store">Default</Button>
        </div>
        <div class="col">
          <p>{{ btnEndIcon }}</p>
          <Button endIcon="local_grocery_store">Default</Button>
        </div>
      </div>
      <div class="flex flex-wrap mt-45">
        <div class="col">
          <p>{{ btnSm }}</p>
          <Button size="sm">Default</Button>
        </div>
        <div class="col">
          <p>{{ btnMd }}</p>
          <Button size="md">Default</Button>
        </div>
        <div class="col">
          <p>{{ btnLg }}</p>
          <Button size="lg">Default</Button>
        </div>
      </div>
      <div class="flex flex-wrap mt-45">
        <div class="col">
          <p>{{ btnColorDefault }}</p>
          <Button color="default">Default</Button>
        </div>
        <div class="col">
          <p>{{ btnColorPrimary }}</p>
          <Button color="primary">Default</Button>
        </div>
        <div class="col">
          <p>{{ btnColorSecondary }}</p>
          <Button color="secondary">Secondary</Button>
        </div>
        <div class="col">
          <p>{{ btnColorDanger }}</p>
          <Button color="danger">Danger</Button>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
p {
  font-size: 12px;
  font-weight: 400;
}
.mt-45 {
  margin-top: 45px;
}
.full {
  width: 100%;
}
.col {
  flex: 0 0 auto;
}
.buttons-container {
  padding: 50px 82px;
}
h3 {
  font-weight: 500;
  font-size: 24px;
}
.flex {
  display: flex;
}
.flex-wrap {
  flex-wrap: wrap;
}
.flex-column {
  flex-direction: column;
}

@media screen and (min-width: 992px) {
  .col {
    width: 25% !important;
  }
}
@media screen and (max-width: 991px) {
  .col {
    width: 50% !important;
  }
}
@media screen and (max-width: 767px) {
  .col {
    width: 100% !important;
  }
}
</style>
