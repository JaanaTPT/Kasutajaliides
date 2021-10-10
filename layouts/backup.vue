<template>
<v-app>
  <v-card height = 1000px>
    
    <v-toolbar>
      <v-toolbar-title></v-toolbar-title>

      <v-spacer></v-spacer>

        <template>
        <v-row align="center">
          <v-text-field class = "search"
            hide-details
            placeholder="Search"
            dense
            append-icon="mdi-magnify"
            light
            solo
            outlined
          ></v-text-field>
          <v-btn icon>
        <v-icon>mdi-microphone</v-icon>
      </v-btn>
        </v-row>
        </template>

      <v-btn icon>
        <v-icon>mdi-video-plus-outline</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-apps</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-bell-outline</v-icon>
      </v-btn>

      <v-btn icon>
        <v-avatar>
        <v-img src="https://picsum.photos/id/1074/367/267"></v-img>
        </v-avatar>
      </v-btn>

    </v-toolbar>
    <br>

  <v-row>
  <v-card >
    
    <v-tabs 
      v-model="tab"
      rounded
    >
      <v-tab 
        v-for="item8 in items8"
        :key="item8.tab"
      >
        {{ item8.tab }}
      </v-tab>
    </v-tabs>

    <v-tabs-items v-model="tab">
      <v-tab-item
        v-for="item8 in items8"
        :key="item8.tab"
      >
        <v-card flat>
          <v-card-text>{{ item8.content }}</v-card-text>
        </v-card>
      </v-tab-item>
    </v-tabs-items>
  </v-card>
  </v-row>
  



    

    <v-navigation-drawer
      absolute
      permanent
      left
    >
    
      
      <template>
        <v-list-item>
          <v-app-bar-nav-icon></v-app-bar-nav-icon>
            <img src="https://lh3.googleusercontent.com/3zkP2SYe7yYoKKe47bsNe44yTgb4Ukh__rBbwXwgkjNRe4PykGG409ozBxzxkrubV7zHKjfxq6y9ShogWtMBMPyB3jiNps91LoNH8A=s500" style = "max-width: 50%;">
        </v-list-item>
      </template>


      <v-list dense>
        <v-list-item
          v-for="item in items"
          :key="item.title"
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

           <v-divider></v-divider>

      <v-list dense>
        <v-list-item
          v-for="item2 in items2"
          :key="item2.title"
        >
          <v-list-item-icon>
            <v-icon>{{ item2.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item2.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

   <v-divider></v-divider>

      <v-list dense>
        <v-list-item id = "sub">
          SUBSCRIPTIONS
          </v-list-item>
        <v-list-item
          v-for="item3 in items3"
          :key="item3.title"
        >
          <v-list-item-avatar>
            <v-avatar>
              <v-img  :src= item3.avatar>
               
                </v-img>
              </v-avatar>
          </v-list-item-avatar>

          <v-list-item-content>
            <v-list-item-title>{{ item3.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
                      <v-divider></v-divider>

      <v-list dense>
         <v-list-item id = "sub">
          MORE FROM YOUTUBE
          </v-list-item>
        <v-list-item
          v-for="item4 in items4"
          :key="item4.title"
        >
          <v-list-item-icon>
            <v-icon>{{ item4.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item4.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

       <v-divider></v-divider>

      <v-list dense>
        <v-list-item
          v-for="item5 in items5"
          :key="item5.title"
        >
          <v-list-item-icon>
            <v-icon>{{ item5.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item5.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <v-divider></v-divider>

      <v-list id = "info" dense >
        <v-list-item
          v-for="item6 in items6"
          :key="item6.title"
        >
          <v-list-item-content>
            <v-list-item-title style="font-size:0.75rem !important; font-weight: bolder; padding-left:0; color:#aaa; line-height: 1.2rem !important;">{{ item6.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <v-list id = "info" dense >
        <v-list-item
          v-for="item7 in items7"
          :key="item7.title"
        >
          <v-list-item-content>
            <v-list-item-title style="font-size:0.75rem !important; font-weight: bolder; padding-left:0; color:#aaa; line-height: 1.2rem !important;">{{ item7.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-list-item id = "sub" style="color:#909090">
          © 2021 Google LLC
          </v-list-item>
      </v-list>


    </v-navigation-drawer>
  </v-card>

</v-app>
</template>


<script>
  export default {
    theme: { disable:true },
    data () {
      return {
        items: [
          { title: 'Home', icon: 'mdi-home-variant' },
          { title: 'Explore', icon: 'mdi-compass' },
          { title: 'Subscriptions', icon: 'mdi-youtube-subscription' },
        ],
        items2: [
          { title: 'Library', icon: 'mdi-filmstrip-box-multiple' },
          { title: 'History', icon: 'mdi-history' },
          { title: 'Your videos', icon: 'mdi-play-box-outline' },
          { title: 'Watch later', icon: 'mdi-clock' },
          { title: 'Goodmast', icon: 'mdi-youtube-tv' },
          { title: 'Show more', icon: 'mdi-check' },
        ],
        items3: [
          { title: 'mupi5', avatar: 'https://i.picsum.photos/id/1005/5760/3840.jpg?hmac=2acSJCOwz9q_dKtDZdSB-OIK1HUcwBeXco_RMMTUgfY'},
          { title: 'BenGen', avatar: 'https://www.minecraft.net/etc.clientlibs/minecraft/clientlibs/main/resources/img/minecraft-creeper-face.jpg' },
          { title: 'CactusArmy', avatar: 'https://randomuser.me/api/portraits/men/17.jpg' },
          { title: 'roni dutta', avatar: 'https://i.picsum.photos/id/1025/4951/3301.jpg?hmac=_aGh5AtoOChip_iaMo8ZvvytfEojcgqbCH7dzaz-H8Y' },
          { title: 'chrisownx', avatar: 'https://randomuser.me/api/portraits/men/7.jpg' },
          { title: 'ZiZZo', avatar: 'https://randomuser.me/api/portraits/women/18.jpg' },
        ],
          items4: [
          { title: 'YouTube Premium', icon: 'mdi-play-box-outline' },
          { title: 'Gaming', icon: 'mdi-youtube-gaming' },
          { title: 'Live', icon: 'mdi-access-point' },
          { title: 'Sports', icon: 'mdi-trophy-variant-outline' },
        ],
         items5: [
          { title: 'Settings', icon: 'mdi-cog-outline' },
          { title: 'Report history', icon: 'mdi-flag-outline' },
          { title: 'Help', icon: 'mdi-help-circle-outline' },
          { title: 'Send feedback', icon: 'mdi-message-alert-outline' },
        ],
        items6: [
          { title: 'About   Press   Copyright'},
          { title: 'Contact us    Creators'},
          { title: 'Advertise   Developers'},
        ],
        items7: [
          { title: 'Terms   Privacy   Policy&Safety'},
          { title: 'How YouTube works'},
          { title: 'Test new features'},
        ],
        items8: [
          { tab: 'Tab X Content', content: 'Tab X Content' },
          { tab: 'Tab X Content', content: 'Tab X Content' },
          { tab: 'Tab X Content', content: 'Tab X Content' },
          { tab: 'Tab X Content', content: 'Tab X Content' },
          { tab: 'Tab X Content', content: 'Tab X Content' },
          { tab: 'Tab X Content', content: 'Tab X Content' },
          { tab: 'Tab X Content', content: 'Tab X Content' },
          { tab: 'Tab X Content', content: 'Tab X Content' },
          { tab: 'Tab X Content', content: 'Tab X Content' },
          { tab: 'Tab X Content', content: 'Tab X Content' },
        ],
      }
    },
  }
</script>

<style lang = "css">

.v-list-item__title, #sub
 {
   line-height: 1.8rem !important;
  font-size:0.9rem !important;
  font-family: sans-serif;
  border-left: 15px !important;;
  padding-left: 15px;
}

#info {
  font-size:0.5rem !important;
  color: red !important;
}

.v-text-field input {
  font-size:0.9rem !important;
  font-family: sans-serif;
}

.v-text-field {
  max-width: 500px !important;
}


</style>

