<template>
  <div class="hello1">
     <div class="headerWrapper">
      <div class="logo">
        <img src="../assets/element.png" alt="tupian"/>
      </div>
      <div class="container">
        <ul>
          <li>
            <div>
              <el-input v-model="input" placeholder="请输入内容"></el-input>
            </div>
          </li>
          <li>
            <a @click=goto() class="active">指南</a>
          </li>
          <li>
             <a @click=goto() class="active">组件</a>
          </li>
          <li>
             <a @click=goto() class="active">资源</a>
          </li>
          <li>
            <el-select v-model="value" placeholder="请选择">
              <el-option
                v-for="item in options"
                :key="item.value"
                :label="item.label"
                :value="item.value">
              </el-option>
            </el-select>
          </li>
           <li>
              <el-select v-model="value" placeholder="请选择">
                <el-option
                  v-for="item in options"
                  :key="item.value"
                  :label="item.label"
                  :value="item.value">
                </el-option>
              </el-select>
          </li>
           <li>
             <div class="block">
                <el-color-picker v-model="color1"></el-color-picker>
              </div>
          </li>
        </ul>
        </div>
    </div>
    <div class="main-cnt">

    </div>
  </div>  
</template>
<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
       options: [{
          value: '选项1',
          label: '1.4.13'
        }, {
          value: '选项2',
          label: '2.0.11'
        }, {
          value: '选项3',
          label: '2.1.0'
        }, {
          value: '选项4',
          label: '2.2.2'
        }, {
          value: '选项5',
          label: '2.3.9'
        },
        {
          value: '选项6',
          label: '2.4.5'
        }],
        value: '2.4.5',
        input:'',
        color1: '#409EFF',
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
}
li {
  display: block;
  float: left;
  position: relative;
  margin:0;
  margin-left: 30px;
}
a {
  color: #42b983;
}
.hello{
  overflow-y: hidden;
}
.headerWrapper{
  position: fixed;
  width: 100%;
  height: 80px;
  line-height: 80px;
  left: 0;
  top: 0;
  z-index: 1500;
  box-sizing: border-box;
}
.main-cnt{
  padding: 0;
  margin-top: 0;
  height: 100%;
  min-height: auto;
}
.logo{
  float:left; 
}
 img{
    vertical-align: middle;
  }
.container{
  height: 100%;
  background: transparent;
  padding: 0;
  margin: 0;
  float: right; 
  margin-left:30px;
}
.serch{
  height:32px;
  line-height: 32px;
  -webkit-appearance: none;
  background-color: #fff;
  background-image: none;
  border-radius: 4px;
  border: 1px solid #dcdfe6;
  box-sizing: border-box;
  color: #606266;
  display: inline-block;
  font-size: inherit;
  height: 40px;
  line-height: 40px;
  outline: none;
  padding: 0 15px;
  transition: border-color .2s cubic-bezier(.645,.045,.355,1);
  width: 100%;
}
  
</style>

