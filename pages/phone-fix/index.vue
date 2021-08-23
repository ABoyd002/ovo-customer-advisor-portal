<template>
  <v-container>
    <h1>Phone Fix</h1>

    <v-row>
      <v-col>
        <v-stepper v-model="step">
          <v-stepper-header>
            <v-stepper-step step="1" editable> Step 1 </v-stepper-step>
            <v-divider />
            <v-stepper-step step="2" editable> Step 2 </v-stepper-step>
            <v-divider />
            <v-stepper-step step="3" editable> Step 3 </v-stepper-step>
            <v-divider />
            <v-stepper-step step="4" editable> Step 4 </v-stepper-step>
          </v-stepper-header>

          <v-stepper-items>
            <v-stepper-content step="1"> Test </v-stepper-content>
          </v-stepper-items>
        </v-stepper>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      step: 1,
    };
  },
};
</script>
