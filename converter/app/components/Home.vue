<template>
  <Page class='main-page' background="white">
    <ActionBar>
      <DockLayout>
        <Label style="font-size: 20" dock="left" text="Конвертер"/>
      </DockLayout>
    </ActionBar>
    <Label text="123"/>
    <StackLayout   flexWrap="wrap">
      <FlexboxLayout>
      <Image class="icon" src='~/images/currencies.png' @tap="$navigateTo(currecy)" />
      <Label class="title" text="Валюта" @tap="$navigateTo(currecy)"/>
      </FlexboxLayout>
      <FlexboxLayout>
      <Image class="icon" src='~/images/thermometer.png' @tap="$navigateTo(temperature)" />
      <Label class="title" text="Температура" @tap="$navigateTo(temperature)"/>
      </FlexboxLayout>
      <FlexboxLayout>
      <Image class="icon" src='~/images/weight-scale.png' @tap="$navigateTo(weight)" />
      <Label class="title" text="Масса" @tap="$navigateTo(weight)"/>
      </FlexboxLayout>
      <FlexboxLayout>
      <Image class="icon" src='~/images/length.png' @tap="$navigateTo(distance)" />
      <Label class="title" text="Расстояние" @tap="$navigateTo(distance)"/>
      </FlexboxLayout>
      <FlexboxLayout>
      <Image class="icon" src='~/images/angle.png'  @tap="$navigateTo(angle)" />
      <Label class="title" text="Углы" @tap="$navigateTo(angle)" />
      </FlexboxLayout>
    </StackLayout  >
  </Page>
</template>

<script lang="ts">
  import Vue from "nativescript-vue";
  import Currecy from './Currecy.vue';
  import Weight from './Weight.vue';
  import Temperature from './Temperature.vue';
  import Distance from './Distance.vue';
  import Angle from './Angle.vue';

  export default Vue.extend({
    data() {
      return {
        'currecy': Currecy,
        'weight': Weight,
        'temperature': Temperature,
        'distance': Distance,
        'angle': Angle,
      }
    },
    computed: {
      message() {
        return "Blank {N}-Vue app";
      }
    }
  });
</script>

<style scoped lang="scss">
  @import '@nativescript/theme/scss/variables/blue';

  // Custom styles
  .fas {
    @include colorize($color: accent);
  }

  .info {
    font-size: 20;
    horizontal-align: center;
    vertical-align: center;
  }
  
  .icon {
  height: 80;
  width: 80;
  margin-left: 5;
  margin-right: 15;
  margin: 15;
}

.title {
  font-size: 30;
}
</style>
