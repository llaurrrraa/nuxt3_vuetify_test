<template>
  <div>
    <v-container fluid>
      <v-table>
        <thead>
          <tr>
            <th class="text-left" scope="col">
              Name
            </th>
            <th class="text-left">
              Calories
            </th>
          </tr>
        </thead>
        <tbody>
          <tr
            v-for="item in desserts"
            :key="item.name"
          >
            <td>{{ item.name }}</td>
            <td>{{ item.calories }}</td>
          </tr>
        </tbody>
      </v-table>
      <br />
      <p>{{ selected }}</p>
      <v-checkbox
        v-model="selected"
        label="John"
        value="John"
        color="success"
      ></v-checkbox>
      <v-checkbox
        v-model="selected"
        label="Jacob"
        value="Jacob"
      ></v-checkbox>
      <v-radio-group v-model="radios">
        <v-radio label="Radio one" value="one" id="radio-one"></v-radio>
        <v-radio label="Radio two" value="two" id="radio-two"></v-radio>
        <v-radio label="Radio three" value="three" id="radio-three"></v-radio>
      </v-radio-group>
      <v-file-input label="File input"></v-file-input>
    </v-container>
  </div>
</template>

<script setup>
import { ref } from 'vue'
  const desserts = ref([
    {
      name: 'Frozen Yogurt',
      calories: 159,
    },
    {
      name: 'Ice cream sandwich',
      calories: 237,
    },
    {
      name: 'Eclair',
      calories: 262,
    },
    {
      name: 'Cupcake',
      calories: 305,
    },
    {
      name: 'Gingerbread',
      calories: 356,
    },
    {
      name: 'Jelly bean',
      calories: 375,
    },
    {
      name: 'Lollipop',
      calories: 392,
    },
    {
      name: 'Honeycomb',
      calories: 408,
    },
    {
      name: 'Donut',
      calories: 452,
    },
    {
      name: 'KitKat',
      calories: 518,
    },
  ]);
  const selected = ref(["John"]);
  const radios = ref()
</script>