<template>
  <v-container fluid>
    <v-form>
      <v-file-input>
        
      </v-file-input>
    </v-form>
    <div class="pills">
      <Pill v-for="word in groupedWords" :key="word.name" :name="word.name" :amount="word.amount" />
    </div>
  </v-container>
</template>

<script>
import Pill from './Pill.vue';

export default {
  name: 'HomePage',
  components: {
    Pill,
  },
  data() {
    return {
      groupedWords: [
        { name: 'apple', amount: 10 },
        { name: 'banana', amount: 20 },
        { name: 'cherry', amount: 30 },
        { name: 'apple', amount: 10 },
        { name: 'banana', amount: 20 },
        { name: 'cherry', amount: 30 },
        { name: 'apple', amount: 10 },
        { name: 'banana', amount: 20 },
        { name: 'cherry', amount: 30 },
        { name: 'apple', amount: 10 },
        { name: 'banana', amount: 20 },
        { name: 'cherry', amount: 30 },
      ],
    };
  },
  mounted() {
    console.log(this.groupedWords);
  },
};
</script>

<style>
.v-file-input{
  margin-top: 100px;
}

.pills{
  margin-top: 60px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

</style>
