<template>
    <div class="classCard flex-row">
                <!-- card text -->
                <div class="classCard-text flex-col">
                    <div class="className">
                        <h3>{{nombre}}</h3>
                        <p>Class name</p>
                    </div>
                    <div class="classStats flex-row">
                        <div class="classStats-1 flex-col">
                            <span>{{edad}}</span>
                            <span class="minor">{{edadTipo}}</span>
                        </div>
                        <div class="classStats-2 flex-col">
                            <span>{{numero}}</span>
                            <span class="minor">Class Size</span>
                        </div>
                    </div>                    
                </div>
                <!-- card img -->
                <img class="classCard-img" :src="imagen" :alt="nombre">
                <!-- card btn -->
                <div class="absoluteBtn">
                    READ MORE >
                </div>

            </div>   
</template>

<script>


export default {
    name: 'classCard',
    props: {
        nombre : String,
        imagen : String,
        edad : String,
        edadTipo : String,
        numero : String,
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import "../../assets/css/style.scss";

.classCard {
        
        position: relative;
        width: 49%;
        margin: 1% 0;
        height: 150px;
        color: $white;
        background-color: $darkBlue;
        h3 {
            color: $white;
        }
        .classCard-text {
            width:50%;
            padding: 15px;
            justify-content: space-between;
        }
        .classStats{
            div {
            gap: 5px;
            width: 50%;
            justify-content: center;
            align-items: center;
            }
            .classStats-1 {
                border-right: 1px solid $white;
            }
        } 
        
        img {
            width:50%;
        }
        .minor {
            font-size: 0.8em;
        }
    }
    
</style>