<template>
  <v-tab-item class="pt-2">
    <v-expansion-panels>
      <v-subheader>Base Game</v-subheader>
      <GameParts v-for="game, i in basegame" :key="'b'+i" :game="game"/>
      <v-subheader>River</v-subheader>
      <GameParts v-for="game, i in rivers" :key="'r'+i" :game="game"/>
      <v-subheader>Big Box Expansions</v-subheader>
      <GameParts v-for="game, i in bigbox" :key="'i'+i" :game="game"/>
      <v-subheader>Main Expansions</v-subheader>
      <GameParts v-for="game, i in major" :key="'e'+i" :game="game"/>
      <v-subheader>Mini Expansions</v-subheader>
      <GameParts v-for="game, i in minor" :key="'m'+i" :game="game"/>
    </v-expansion-panels>
  </v-tab-item>
</template>

<script>
import GameParts from './parts/GameParts.vue'

export default {
  name: 'parts',
  components: {
    GameParts,
  },
  //props: {},
  data: ()=>({
    basegame: [
      {name: "Base Game",
        path: "Base",
        tiles: {
          total: 72,
          unique: 24,
          amount: [
            2,4,1,4,
            5,2,1,3,
            2,3,3,3,
            2,3,2,3,
            1,3,2,1,
            8,9,4],
        },
        meeples: [
          {image: "Figure_Meeples_Base.png", amount: 8},
        ],
      },
      {name: "The Abbot",
        path: "Abbot",
        meeples: [
          {image: "Figure_Abbots_Base.png", amount: 1},
        ],
      },
      {name: "20th Anniversary Edition",
        path: "Anniversary",
        tiles: {
          total: 72,
          unique: 24,
          amount: [
            2,4,1,4,
            5,2,1,3,
            2,3,3,3,
            2,3,2,3,
            1,3,2,1,
            8,9,4],
        },
        meeples: [
          {image: "Figure_Meeples_Base.png", amount: 8},
          {image: "Figure_Abbots_Base.png", amount: 1},
        ],
      },
      {name: "20th Anniversary Expansion",
        path: "Arrows",
        tiles: {
          unique: 15,
        },
      },
      {name: "The Wheel of Fortune",
        path: "Wheel",
        tiles: {
          total: 72,
          unique: 34,
          amount: [
            1,2,1,1,
            2,1,2,2,
            2,1,1,2,
            2,2,2,1,
            4,1,1,2,
            4,2,1,7,
            1,8,4],
        },
        pieces: [
          {image: "Figure_BigPinkPig.png", amount: 1},
        ],
        meeples: [
          {image: "Figure_Meeples_Base.png", amount: 8},
        ],
      },
    ],
    rivers: [
      {name: "The River",
        path: "River",
        tiles: {
          unique: 12,
        },
      },
      {name: "20th Anniversary River",
        path: "RiverAE",
        tiles: {
          total: 18,
          unique: 17,
          size: {17:2},
        },
      },
      {name: "River II",
        path: "River2",
        tiles: {
          unique: 12,
        },
      },
    ],
    bigbox: [
      {name: "The Ferries",
        path: "Ferrie",
        tiles: {
          total: 8,
          unique: 3,
          amount: [3,4],
        },
        pieces: [
          {image: "Figure_Ferry.png", amount: 8},
        ],
      },
      {name: "The Flier",
        path: "Flier",
        tiles: {
          unique: 8,
        },
        pieces: [
          {image: "Figure_Die.png", amount: 1},
        ],
      },
      {name: "The Messages",
        path: "Message",
        tiles: {
          total: 0,
          unique: 8,
        },
        meeples: [
          {image: "Figure_Messengers.png", amount: 1},
        ],
      },
      {name: "The Goldmines",
        path: "Goldmine",
        tiles: {
          total: 8,
          unique: 9,
        },
        pieces: [
          {image: "Figure_Gold.png", amount: 1},
        ],
      },
      {name: "Mage and Witch",
        path: "Mage",
        tiles: {
          unique: 8,
        },
        pieces: [
          {image: "Figure_Mage.png", amount: 1},
          {image: "Figure_Witch.png", amount: 1},
        ],
      },
      {name: "The Robbers",
        path: "Robber",
        tiles: {
          unique: 6,
        },
        meeples: [
          {image: "Figure_Robbers.png", amount: 1},
        ],
      },
      {name: "Crop Circles",
        path: "Crop",
        tiles: {
          unique: 6,
        },
      },
    ],
    major: [
      {name: "Inns and Cathedrals",
        path: "Inn",
        tiles: {
          total: 18,
          unique: 17,
          amount: {10:2},
        },
        pieces: [
          {image: "Figure_Abbot_pink.png", amount: 1},
        ],
        meeples: [
          {image: "Figure_MeeplesLarge.png", amount: 1},
          {image: "Figure_Meeples_pink.png", amount: 1},
        ],
      },
      {name: "Traders and Builders",
        path: "Trader",
        tiles: {
          unique: 24,
        },
        meeples: [
          {image: "Figure_Builders.png", amount: 1},
          {image: "Figure_Pigs.png", amount: 1},
        ],
      },
      {name: "The Princess & the Dragon",
        path: "Dragon",
        tiles: {
          total: 30,
          unique: 29,
          amount: {6:2},
        },
        pieces: [
          {image: "Figure_Dragon.png", amount: 1},
          {image: "Figure_Fairy.png", amount: 1},
        ],
      },
      {name: "The Tower",
        path: "Tower",
        tiles: {
          total: 18,
          unique: 17,
          amount: {10:2},
        },
        pieces: [
          {image: "Figure_Tower.png", amount: 30},
        ],
      },
      {name: "Abbey & Mayor",
        path: "Abbey",
        tiles: {
          total: 18,
          unique: 13,
          amount: [6],
        },
        meeples: [
          {image: "Figure_Mayors.png", amount: 1},
          {image: "Figure_Barns.png", amount: 1},
          {image: "Figure_Wagons.png", amount: 1},
        ],
      },
      {name: "Count, King and Robber",
        sub: "- Heretics",
        path: "Heretic",
        tiles: {
          unique: 5,
        },
      },
      {name: "Count, King and Robber",
        sub: "- King and Robber",
        path: "King",
        tiles: {
          total: 5,
          unique: 7,
        },
      },
      {name: "Count, King and Robber",
        sub: "- Count of Carcassonne",
        path: "City",
        tiles: {
          size: 2,
          total: 12,
          unique: 2,
        },
        pieces: [
          {image: "Figure_Count.png", amount: 1},
        ],
      },
      {name: "Bridges, Castles and Bazaars",
        path: "Bridge",
        tiles: {
          total: 12,
          unique: 11,
          amount: {3:2},
        },
        pieces: [
          {image: "Figure_Bridge.png", amount: 12},
          {image: "Token_Castle_C2.png", amount: 12},
        ],
      },
      {name: "Hills & Sheep",
        path: "Hill",
        tiles: {
          total: 18,
          unique: 16,
          amount: {
            10:2,
            11:2},
        },
        pieces: [
          {image: "Token_HillsSheep_Sheep1_C2.png", amount: 4},
          {image: "Token_HillsSheep_Sheep2_C2.png", amount: 5},
          {image: "Token_HillsSheep_Sheep3_C2.png", amount: 5},
          {image: "Token_HillsSheep_Sheep4_C2.png", amount: 2},
          {image: "Token_HillsSheep_Wolf_C2.png", amount: 2},
        ],
      },
      {name: "Under the Big Top",
        path: "Circus",
        tiles: {
          total: 18,
          unique: 16,
          amount: {
            10:2,
            11:2},
        },
        pieces: [
          {image: "Figure_Roundtop.png", amount: 1},
          {image: "Token_UnderTheBigTop_Flea_C2.png", amount: 1},
          {image: "Token_UnderTheBigTop_Monkey_C2.png", amount: 4},
          {image: "Token_UnderTheBigTop_Seal_C2.png", amount: 5},
          {image: "Token_UnderTheBigTop_Bear_C2.png", amount: 3},
          {image: "Token_UnderTheBigTop_Tiger_C2.png", amount: 2},
          {image: "Token_UnderTheBigTop_Elephant_C2.png", amount: 1},
        ],
        meeples: [
          {image: "Figure_Ringmasters_C2.png", amount: 1},
        ],
      },
      {name: "Mists over Carcassonne",
        path: "Mist",
        tiles: {
          total: 60,
          unique: 24,
          amount: [
            2, 1, 1, 1,
            1, 2, 2, 1,
            1, 1, 3, 1,
            1, 1, 2, 1,
            1, 1, 1, 1,
            1, 1, 1, 1,
          ],
        },
        /*meeples: [
          {image: "Figure_Ringmasters_C2.png", amount: 1},
        ],*/
      },
    ],
    minor: [
      {name: "German Castles",
        path: "Castle",
        tiles: {
          size: 2,
          total: 12,
          unique: 6,
        },
      },
      {name: "German Cathedrals",
        path: "Cathedral",
        tiles: {
          unique: 6,
        },
      },
      {name: "German Monasteries",
        path: "Monastery",
        tiles: {
          unique: 6,
        },
      },
      {name: "Japanese Temples",
        path: "Temples",
        tiles: {
          unique: 6,
        },
      },
      {name: "The Watchtowers",
        path: "Watchtower",
        tiles: {
          unique: 12,
        },
      },
      {name: "The Peasant Revolts",
        path: "Peasant",
        tiles: {
          unique: 12,
        },
      },
      {name: "Halflings",
        path: "Halfling",
        tiles: {
          ext: "png",
          total: 12,
          unique: 24,
        },
      },
      {name: "The Signposts",
        path: "Signposts",
        tiles: {
          unique: 12,
        },
      },
      {name: "The Tollkeepers",
        path: "Tollkeeper",
        tiles: {
          unique: 10,
        },
        pieces: [
          {image: "Token_Tollkeeper_pink.png", amount: 1},
          {image: "Token_Tollkeeper_blue.png", amount: 1},
          {image: "Token_Tollkeeper_green.png", amount: 1},
          {image: "Token_Tollkeeper_yellow.png", amount: 1},
          {image: "Token_Tollkeeper_red.png", amount: 1},
          {image: "Token_Tollkeeper_black.png", amount: 1},
        ],
      },
      {name: "The Festival",
        path: "Festival",
        tiles: {
          unique: 10,
        },
      },
      {name: "The Bets",
        path: "Bets",
        tiles: {
          unique: 10,
        },
        pieces: [
          {image: "Tokens.png", amount: 36},
        ]
      },
      {name: "The Markets of Leipzig",
        path: "Market",
        tiles: {
          size: 2,
          total: 8,
          unique: 4,
        },
      },
      {name: "The Fruit-Bearing Trees",
        path: "Tree",
        tiles: {
          unique: 6,
        },
        pieces: [
          {image: "Token_apple.png", amount: 4},
          {image: "Token_apricot.png", amount: 4},
          {image: "Token_cherry.png", amount: 4},
          {image: "Token_elder.png", amount: 4},
          {image: "Token_plum.png", amount: 4},
          {image: "Token_quince.png", amount: 4},
        ]
      },
      {name: "The Bathhouses",
        path: "Bathhouse",
        tiles: {
          unique: 6,
        },
      },
      {name: "The School",
        path: "School",
        tiles: {
          unique: 2,
        },
      },
      {name: "The Labyrinths",
        path: "Labyrinth",
        tiles: {
          unique: 2,
        },
      },
      {name: "Ukraine Promo",
        path: "Ukraine",
        tiles: {
          unique: 1,
        },
      },
      {name: "The Gifts",
        path: "Gifts",
        pieces: [
          {image: "Cards.png", amount: 1},
        ],
      },
    ]
  }),
  //computed: {},
  //methods: {},
  //watch: {},
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>
