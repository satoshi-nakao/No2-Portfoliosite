<template>
  <v-app>
   
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
      color="primary"
    >
      <v-btn color="primary" :to=" '/' ">TOP</v-btn>
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <v-menu offset-y>
      <template v-slot:activator="{on}">
      <v-btn
        icon 
        v-on="on" 
      >
        <v-icon>mdi-menu</v-icon>
      </v-btn>
      </template>
    <v-list>
    <v-list-item
     v-for="(item, index) in items"
     :key="index"
     :to="item.to"
     >
      <v-list-item-title >{{ item.name }}</v-list-item-title>
    </v-list-item>
    </v-list>
    </v-menu>
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <!-- <v-navigation-drawer
      v-model="rightDrawer"
      :right="right"
      temporary
      fixed
    >
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light>
              mdi-repeat
            </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer> -->
    <v-footer
      :absolute="!fixed"
      app
      color="primary"
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {name :'Like',to :"/like"},
        {name :'Skill',to :"skill"},
        {name : 'Want',to :"want"},
      ],
      title: 'My page'
    }
  }
}
</script>
