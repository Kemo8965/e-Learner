<template>
  <div>
      <v-container>
        <v-card>
         
            <v-content class="mx-4">
              <v-row>
              <v-col>
                <h2 class="color"> English Language</h2>
                <h3>Teacher</h3><p class="color"> Mr. Katema</p>
                <h3>Subject Code </h3><p class="color">ENG 3002</p>
                <h3>Learning Format</h3><p class="color">Video & Notes</p>
              </v-col>
              
            </v-row>
            
            </v-content>
         
        </v-card>

        <v-card>
          <v-card-title>  Lesson Plan <v-spacer/> <v-btn @click="back" color="warning">
                     <v-icon small >
                      mdi-arrow-left-circle 
                      </v-icon>
                      Back</v-btn> </v-card-title>
         
              <v-card>
                <v-content class="mx-4">
                  <div class="pb-8">
                    <v-content>
                      <v-content class="  mr-20 fill-height" :style="{width:'500px'}">
                        <VideoPlayer/>
                      </v-content>
                      Lesson 1: Intro To English Language
                  <v-spacer/>
                  <v-card-actions>
                    <v-btn
                    color="info">
                      Description
                    </v-btn>
                    <v-spacer/>
                    <v-btn
                    color="success">
                    Start
                    <v-spacer/>
                     <v-icon small >
                      mdi-arrow-right-circle 
                      </v-icon>
                      
                    </v-btn>
                  </v-card-actions>
                  
                    </v-content>
                    
                  </div>
                 <v-divider/>
                 <div class="pb-8">
                  <v-content>
                     <v-content class="  mr-20 fill-height" :style="{width:'500px'}">
                        <VideoPlayer/>
                      </v-content>
                      Lesson 2: English Language in greater depth
                  <v-spacer/>
                  <v-card-actions>
                    <v-btn
                    color="info">
                      Description
                    </v-btn>
                    <v-spacer/>
                    <v-btn
                    color="success">
                    Start
                    <v-spacer/>
                     <v-icon small >
                      mdi-arrow-right-circle 
                      </v-icon>
                      
                    </v-btn>
                  </v-card-actions>
                  
                    </v-content>
                    
                  </div>

                   <v-divider/>
                 <div class="pb-8">
                   <v-content>
                      <v-content class="  mr-20 fill-height" :style="{width:'500px'}">
                        <VideoPlayer/>
                      </v-content>
                      Lesson 3: Nouns & Pronouns
                  <v-spacer/>
                  <v-card-actions>
                    <v-btn
                    color="info">
                      Description
                    </v-btn>
                    <v-spacer/>
                    <v-btn
                    color="success">
                    Start
                    <v-spacer/>
                     <v-icon small >
                      mdi-arrow-right-circle 
                      </v-icon>
                      
                    </v-btn>
                  </v-card-actions>
                  
                    </v-content>
                    
                  </div>

                  <v-divider/>
                 <div class="pb-8">
                   <v-content>
                      <v-content class="  mr-20 fill-height" :style="{width:'500px'}">
                        <VideoPlayer/>
                      </v-content>
                      Lesson 4: Adjectives 
                  <v-spacer/>
                  <v-card-actions>
                    <v-btn
                    color="info">
                      Description
                    </v-btn>
                    <v-spacer/>
                    <v-btn
                    color="success">
                    Start
                    <v-spacer/>
                     <v-icon small >
                      mdi-arrow-right-circle 
                      </v-icon>
                      
                    </v-btn>
                  </v-card-actions>
                  
                    </v-content>
                    
                  </div>

                  <v-divider/>
                 <div class="pb-8">
                   <v-content>
                      <v-content class="  mr-20 fill-height" :style="{width:'500px'}">
                        <VideoPlayer/>
                      </v-content>
                      Lesson 5: Verbs & Adverbs
                  <v-spacer/>
                  <v-card-actions>
                    <v-btn
                    color="info">
                      Description
                    </v-btn>
                    <v-spacer/>
                    <v-btn
                    color="success">
                    Start
                    <v-spacer/>
                     <v-icon small >
                      mdi-arrow-right-circle 
                      </v-icon>
                      
                    </v-btn>
                  </v-card-actions>
                  
                    </v-content>
                    
                  </div>

                  <v-divider/>
                 <div class="pb-8">
                   <v-content>
                      <v-content class="  mr-20 fill-height" :style="{width:'500px'}">
                        <VideoPlayer/>
                      </v-content>
                      Lesson 6: Synonyms & Antonyms
                  <v-spacer/>
                  <v-card-actions>
                    <v-btn
                    color="info">
                      Description
                    </v-btn>
                    <v-spacer/>
                    <v-btn
                    color="success">
                    Start
                    <v-spacer/>
                     <v-icon small >
                      mdi-arrow-right-circle 
                      </v-icon>
                      
                    </v-btn>
                  </v-card-actions>
                  
                    </v-content>
                    
                  </div>

                  <v-divider/>
                 <div class="pb-8">
                   <v-content>
                      <v-content class="  mr-20 fill-height" :style="{width:'500px'}">
                        <VideoPlayer/>
                      </v-content>
                      Lesson 7: Idiomatic expressions
                  <v-spacer/>
                  <v-card-actions>
                    <v-btn
                    color="info">
                      Description
                    </v-btn>
                    <v-spacer/>
                    <v-btn
                    color="success">
                    Start
                    <v-spacer/>
                     <v-icon small >
                      mdi-arrow-right-circle 
                      </v-icon>
                      
                    </v-btn>
                  </v-card-actions>
                  
                    </v-content>
                    
                  </div>

                </v-content>
              </v-card>
            
        </v-card>
      </v-container>
  </div>
</template>

<script>
import VideoPlayer from '../../../components/video-player/video-player'
  export default {
    components:{
      VideoPlayer
    },
    methods:{
      async back(){
        await this.$router.push('/')
      }
    }
  }
</script>

<style lang="scss" scoped>
  .color{
    color: yellowgreen;
  }
</style>