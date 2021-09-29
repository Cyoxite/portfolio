<template>
    

<div @click=getbuttontext class="completed" v-bind:key="completed.id" >
<h2> {{completed.name}}<arrow  :class="{ 'down': toggle, 'up': !toggle  }"> </arrow> </h2>
<transition name="fade">
        <div class="Show" v-show='!toggle'>

            <!-- GALLERY FRAGMENT -->
        <div class="gallery">
        <img class="miniature" v-for="photo in completed.photo"
        :key="photo.link" :src="photo.link">
        </div>

            <!-- DESCRIPTION FRAGMENT -->
        <div class="description">
            <h4>Description</h4>
            {{completed.description}}

            <!-- LIST OF FEATURES FRAGMENT -->
            <div class="features" ><h4>Features</h4>
                <ol> 
                <li v-for="feature in completed.feature"
        :key="feature.featurenm"
                
                >{{feature.featurenm}}</li>
                </ol>
            
        </div></div>

        

             <!-- TECHNOLOGY FRAGMENT -->
        <div class="technology"><h4>Technology</h4>
            <ol>
                <li
                v-for="technology in completed.technology"
                :key="technology">
                <img :src="'/images/technology/'+technology + '.svg'" width="65" height="65">
                </li>
            </ol>


        
        </div>
        </div>
        </transition>
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
.completed{
    float:left;
    min-width: 100%;
    border: 2px solid white;
    border-radius: 10px;
    margin-bottom: 10px;
    box-shadow: 10px 5px 5px black;
    
}


.description{
    margin-top: 5px;
    float:left;
    width: 40%;
    

    
}

.features{
    
    width: 100%;
    float: left;
}
.gallery{
margin-top: 5px;
display:inline-block;
width: 55%;

}

.technology{
    float:left;
    min-width: 100%;
    margin-bottom: 23px;
    
}

.miniature{
    max-height: 22%;
    max-width: 22%;
    min-height: 15%;
    min-width: 15%;
    padding-inline: 5px;
}

.features li{
    font-style: italic;
    position: relative;
    padding: 0.1rem;
    

}

.technology li{
    display: inline-block;
    align-content: center;
    padding-inline: 5px;
}

h4{
    position: center;
}

.fade-enter-active, .fade-leave-active {
  transition: opacity .4s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
}
arrow {
     border: solid black;
     border-width: 0 4px 4px 0;
     display: inline-block;
     margin-left: 10px;
     padding: 6px;
     
}
.completed:hover arrow{
  border:solid cyan;
  border-width: 0 4px 4px 0;  
}
 .down {
     transform: rotate(45deg);
     transition: transform 1s ease-in-out;
}
 .up {
     transform: rotate(-135deg);
     transition: transform 1s ease-in-out;
}

</style>