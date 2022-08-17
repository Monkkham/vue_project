<template>
    <v-container class="grey lighten-5">
        <v-row no-gutters>
        <v-col
            v-for="n in 1"
            :key="n"
            cols="12"
            sm="4"
        >
            <v-card
            class="pa-12"
            outlined
            tile
            >
                    <v-list dense>
                    <v-list-item-group
                        v-model="item"
                        color="primary"
                    >
                    
                        <v-list-item
                        v-for="(item, index) in items"
                        :key="index++"
                        >
                        <v-btn block>
      <v-list-item-title :style="{'color': item.color}">{{ index }}. {{ item.name }}</v-list-item-title>
      <h1 v-if="'name' === 'Vue'">Monk</h1>
  </v-btn>
                    
                        </v-list-item>
                    </v-list-item-group>
                    </v-list>
                </v-card>
        </v-col>
        </v-row>
    </v-container>
</template>

<script>
export default {
    data: () => ({
      items: [
  {
    "name":"Vue", color: 'green',
  },
  {
    "name":"React", color: 'blue',
  },
  {
    "name":"Angular", color: 'red',
  }
],
    }),
}
</script>
