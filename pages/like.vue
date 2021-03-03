<template>
  <v-layout row justify-center>
    <!-- <v-flex xs12> -->
      <v-col cols="12" sm="8" md="6">
      <v-card >
        <v-card-title>
          好きなもの
        </v-card-title>
        <v-col>
        <v-card-text>
          <v-layout row wrap>
            <v-flex xs9
            >
            <v-layout row wrap>
                <template v-for="(data, i) in datasets">
                  <v-flex :key="i" xs3 class="accent blue">
                    {{ data.name }}
                  </v-flex>
                  <v-flex
                    :key="i"
                    xs9
                    class="accent lighten-5"
                    v-html="data.description"
                  >
                  </v-flex>
                </template>
              </v-layout>
             
            </v-flex>
            
          </v-layout>
        </v-card-text>
        </v-col>
      </v-card>
      </v-col>
    <!-- </v-flex> -->
  </v-layout>
</template>



<script>
export default {
  data(){
    return{
      datasets: [
        {name: '超高層ビル' , description: '東京都庁、サンシャイン60'},
        {name: '場所' , description: '丸の内、池袋、渋谷'},
        {name: '食べ物' , description: 'ハンバーガー、うどん、ラーメン'},
        {name: '動物' , description: '猫'}
      ]
    }
  }
}
</script>