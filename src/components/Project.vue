<template>
    

<div class="completed" v-bind:key="completed.id" >
<h2> {{completed.name}} <button @click=getbuttontext>{{buttontext}}</button></h2>
        <div class="Show" v-show='!toggle'>

            <!-- GALLERY FRAGMENT -->
        <div class="gallery">
        <img class="miniature" v-for="photo in completed.photo"
        :key="photo.link" :src="photo.link">
        </div>

            <!-- DESCRIPTION FRAGMENT -->
        <div class="description">{{completed.description}}</div>

            <!-- LIST OF FEATURES FRAGMENT -->
            <div class="features" >
                <ol> <h4>Features</h4>
                <li v-for="feature in completed.feature"
        :key="feature.featurenm"
                
                >{{feature.featurenm}}</li>
                </ol>
            
        </div>

             <!-- TECHNOLOGY FRAGMENT -->
        <div class="technology">Technology
            <ol>
                <li
                v-for="technology in completed.technology"
                :key="technology"
                >
                {{technology}}
                </li>
            </ol>


        </div>
        </div>
</div>

</template>

<script>
export default {
    data () {
   return {
     toggle: true,
     buttontext: 'show more',
   }
    },
    props: 
    ['completed'],
    methods: {
        getbuttontext: function (){
            this.toggle = !this.toggle;
            if (this.toggle == false){
                this.buttontext = 'hide'
                return
            } else {
                this.buttontext = 'show more'
                return
            }
            }

        
            
        }

    }


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.miniature{
    max-height: 9%;
    max-width: 9%;
    padding-inline: 5px;
}
</style>