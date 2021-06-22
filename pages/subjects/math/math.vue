<template>
  <div>
      <v-container>
        <v-card>
         
            <v-content class="mx-4">
              <v-row>
              <v-col>
                <h2 class="color"> Mathematics</h2>
                <h3>Teacher</h3><p class="color"> Mr. Mwale</p>
                <h3>Subject Code </h3><p class="color">MATH 4001</p>
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
                      Lesson 1: Intro To Mathematics
                  <v-spacer/>
                  <v-card-actions>
                   
                       <Description/>
                   
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
                      Lesson 2: Mathematics in greater depth
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
                      Lesson 3: Cordinate Geometry
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
                      Lesson 4: Functions
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
                      Lesson 5: Linear & Quadratic Equations
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
                      Lesson 6: Inequalities
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
                        <VideoPlayer />
                      </v-content>
                      Lesson 7: Simultaneous Equations
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
import VideoPlayer from '../../../components/math-video-player/video-player'
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
    color: aqua;
  }
</style>