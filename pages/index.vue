<template>
  <div>
    <v-card class="mt-10">
        <v-card-title>
          Subjects
           <v-spacer/>
           
         <AddNewSubject/>
        <v-btn color="warning" class="mx-2">
          <v-icon>
            mdi-refresh-circle
          </v-icon>

          Refresh
        </v-btn>
        </v-card-title>
       
        
      </v-card>
    <v-card class="mt-16">
      
      <v-row class="mx-2 py-4">
        <v-col >
          <v-card >
            <v-card-title>
              English Language
            </v-card-title>
            <v-content class="mb-8 mx-4">
              Lessons: 7
              <v-spacer/>
              Duration: 2 hours
            </v-content>
            <v-btn color="info" class="mb-8 mx-4" @click="eng">
              View Subject
            </v-btn>
            <v-spacer/>
          </v-card>
        </v-col>
        <v-col>
          <v-card >
            <v-card-title>
              Mathematics
            </v-card-title>
             <v-content class="mb-8 mx-4">
              Lessons: 7
              <v-spacer/>
              Duration: 2 hours
            </v-content>
            <v-btn color="info" class="mb-8 mx-4" @click="math">
              View Subject
            </v-btn>
            <v-spacer/>
          </v-card>
        </v-col>
        <v-col>
          <v-card >
            <v-card-title>
              Physics
            </v-card-title>
             <v-content class="mb-8 mx-4">
              Lessons: 7
              <v-spacer/>
              Duration: 2 hours
            </v-content>
            <v-btn color="info" class="mb-8 mx-4" @click="phy">
              View Subject
            </v-btn>
            <v-spacer/>
          </v-card>
        </v-col>
       
      </v-row>

      
    </v-card>

    <v-card class="mt-16">
      <v-row class="mx-2 py-4">
         <v-col>
          <v-card >
            <v-card-title>
              Chemistry
            </v-card-title>
             <v-content class="mb-8 mx-4">
              Lessons: 7
              <v-spacer/>
              Duration: 2 hours
            </v-content>
            <v-btn color="info" class="mb-8 mx-4" @click="che">
              View Subject
            </v-btn>
            <v-spacer/>
          </v-card>
        </v-col>
        <v-col>
           <v-card >
            <v-card-title>
              Additional Math
            </v-card-title>
            
             <v-content class="mb-8 mx-4">
              Lessons: 7
              <v-spacer/>
              Duration: 2 hours
            </v-content>
            <v-btn color="info" class="mb-8 mx-4" @click="addma">
              View Subject
            </v-btn>
            <v-spacer/>
          </v-card>
        </v-col>
        <v-col>
           <v-card >
            <v-card-title>
              Literature
            </v-card-title>
             <v-content class="mb-8 mx-4">
              Lessons: 7
              <v-spacer/>
              Duration: 2 hours
            </v-content>
            <v-btn color="info" class="mb-8 mx-4" @click="lit">
              View Subject
            </v-btn>
            <v-spacer/>
          </v-card>
        </v-col>
       
      </v-row>

      
    </v-card>

    
  </div>
</template>

<script>

  export default {
    methods:{
      async eng(){
        await this.$router.push('/subjects/english/english') 
      },

      async math(){
        await this.$router.push('/subjects/math/math') 
      },

      async phy(){
        await this.$router.push('/subjects/physics/physics') 
      },

      async che(){
        await this.$router.push('/subjects/chemistry/chemistry') 
      },

      async addma(){
        await this.$router.push('/subjects/addma/addma') 
      },

      async lit(){
        await this.$router.push('/subjects/lit/lit') 
      },

    async addNewSubject() {
    await this.$router.push('/inspire')
    },
    }
  }
</script>

<style lang="scss" scoped>

</style>