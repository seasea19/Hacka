<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <v-img
          :src="require('../assets/election.svg')"
          class="my-3"
          contain
          height="200"
        />

      </v-col>

      <v-col class="mb-4">
        <h1 class="display-2 font-weight-bold mb-3">
          Welcome to The Election For
        </h1>

        <p class="subheading font-weight-regular">
          Please select one of the following options and submit
        </p>
      </v-col>

      <v-col
        class="mb-5"
        cols="12"
      >
        <h2 class="headline font-weight-bold mb-3">
          Select an Option
        </h2>

        <v-row justify="center">
          <v-form>
                   <v-radio-group v-model="selectedOption">
                     <v-radio
                       v-for="option in options"
                       :key="option.value"
                       :label="option.name"
                     />
                   </v-radio-group>
                   <v-btn
                     class="form-submit"
                     @click="submit()"
                   >Submit</v-btn>
                 </v-form>

        </v-row>
      </v-col>

      <v-col
        class="mb-5"
        cols="12"
      >

      </v-col>
    </v-row>
    <div>Icons made by <a href="https://www.flaticon.com/authors/freepik" title="Freepik">Freepik</a> from <a href="https://www.flaticon.com/" title="Flaticon">www.flaticon.com</a></div>

  </v-container>
</template>

<script>
  export default {
    name: 'HelloWorld',
    data: () => ({
      // get this data from your backend and put it in a model or something (like VueX) and then pass it to this component from there
      options: [
        { name: 'Option A', value: 'A' },
        { name: 'Option B', value: 'B' },
        { name: 'Option C', value: 'C' }
      ],
      selectedOption: null,
      title: 'Select an option'
    }),
    methods: {
      submit() {
        // here is where you'd maybe write a POST request to your backend saying the user's username and what they voted for
        console.log(this.options[this.selectedOption].value);
      }
    }
  }
</script>
