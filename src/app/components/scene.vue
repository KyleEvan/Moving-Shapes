<!--

HTML

-->
<template>
  <div id="scene" ref="scene">
    <h1 id="name" ref="name">Kyle</h1>
  </div>
</template>


<!--

JS

-->
<script>
import { ShapeScene } from '../shapes.js';

export default {
 // data(){
 // console.log(this);
 // return this;
 // },
 mounted() {
   // let scene = document.getElementById('scene');
   // let name = document.getElementById('name');

   ShapeScene(this.$refs.scene, this.$refs.name);
   // console.log(initShapes(scene, name));
 }
}
</script>


<!--

Styles/SCSS

 -->
<style lang="scss">
@import '../../style/global.scss';

#scene {
    position: fixed;
    z-index: -1;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;

    svg {
        position: absolute;
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;

        * {
            opacity: 0;
        }
    }
    #name {
        // color: #FF9A91;
        // color: #7A6563;
        margin: 0;
        font-size: 50px;
        text-transform: uppercase;
        font-size: 12vw;
        // font-family: 'Montserrat', sans-serif;
        font-family: 'InterUI', sans-serif;
        font-weight: 700;
        user-select: none;

        span {
            display: inline-block;
            position: relative;
            opacity: 0;
            line-height: 0.8;
            padding: 0 0.05em;
            transform: translateY(100%);
        }
    }
    // .transition > * {
    //     transition: 5s cubic-bezier(0.02, 0.1, 0.15, 1);
    // }

}

/****************************************************************

Fallback:
If the broser doesn't support flexbox, don't display the scene

****************************************************************/
// @supports not (display:flex) {
//     #scene {
//         display: none;
//     }
// }
</style>
