<template>
  <v-layout row justify-center>
    <v-col cols="12" sm="8" md="6">
    <v-card>
      　<v-card-title class="headline">
          好きなもの
        </v-card-title>
        <v-card-text>
          <p>超高層ビル:東京都庁</p>
          <p>建築物：国立新美術館</p>
          <p>食べ物：ラーメン</p>
        </v-card-text>
    </v-card>
    </v-col>
<!-- </v-row>  -->
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