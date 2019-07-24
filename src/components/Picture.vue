<template>
  <div class="hello">
    <div class="root">


      <div class="left_icon">

        <div class="one_line_icon">
          <button @click="onDrawRect">矩形</button>
          <button @click="onDrawLine">线</button>
          <button>你好</button>
          <button>你好</button>
        </div>
      </div>

      <div class="canvas_container">
        <canvas id="main" class="canvas_cls">
        </canvas>
      </div>


    </div>

  </div>
</template>

<script>
  import {fabric} from 'fabric'


  export default {
    name: 'Picture',
    data() {
      return {
        canvas : null,

      }
    },

    mounted(){
      this.canvas = new fabric.Canvas('main')
      this.canvas.setWidth(400)
      this.canvas.setHeight(400)
    },

    methods: {
      onDrawRect() {
        let rect = new fabric.Rect({
          left : 100,
          top:100,
          fill:'red',
          width:50,
          height:50
        })

        this.canvas.add(rect)
      },

      onDrawLine(){
        let line = new fabric.Line({

        })

      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1, h2 {
    font-weight: normal;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }

  .root {
    display: flex;
    flex-direction: row;
  }

  .left_icon {
    width: 200px;
    background-color: #f6f6f6;
  }

  .canvas_container {
    width: 600px;
    height: 600px;
    margin-left: 20px;
  }

  .canvas_cls {
    width: 600px;
    height: 600px;
    background-color: #f6f6f6;;
  }


  .one_line_icon {
    display: flex;
    justify-content: space-around;
    width: 100%;
  }
</style>
