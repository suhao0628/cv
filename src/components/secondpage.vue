<template>
  <div class="page2">
    <div class="wrapper">
      <div class="project">
        <div class="project-title">{{project.second.title}}</div>
        <br>
        <span class="tag" v-for="(tag, index) in project.second.techTags" :key="index">
          {{ tag }}
        </span>
        <div class="subtitle">Description:</div>
        <div class="project-desc">
          {{project.second.desc}}
        </div>
        <div class="subtitle">Project content:</div>
        <ol class="list">
          <li v-for="(item, index) in project.second.duty" :key="index">
            {{ item }}
          </li>
        </ol>
      </div>
      <div class="title">Evaluation</div>
      <div class="line"></div>
      <ul class="evaluate">
        <li v-for="(item,index) in evaluation" :key="index">{{item}}</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Page2Index',
  props: ['project', 'evaluation'],
  data () {
    return {
    }
  }
}
</script>

<style lang="less" media="print">
@media print {
  a {
    display: inline !important;
  }
}
.page2 {
  margin: 10px auto;
  padding: 20px 0;
  width: 800px;
  height: 1060px;
  background-color: #fff;
  .wrapper {
    margin: 0 50px;
    .title {
      width: 120px;
      height: 35px;
      line-height: 35px;
      text-align: center;
      font-size: 18px;
      font-weight: normal;
      background-color: rgb(65, 65, 65);
      color: #fff;
    };
    .tag {
    display: inline-block;
    background-color: #3498db;
    color: #fff;
    padding: 4px 8px;
    margin-left: 5px;
    border-radius: 3px;
    font-size: 12px;
  }
    .line {
      border-top: 2px solid rgb(65, 65, 65);
    }
    .project {
      margin: 20px 25px;
      font-size: 16px;
      .subtitle {
        margin: 4px 0;
        font-weight: bold;
      }
      .project-title {
        text-align: center;
        font-weight: bold;
      }
      .project-desc {
        text-indent: 2em;
      }
    }
    // .evaluate {
    //   margin: 20px 25px;
    // }
  }
}
</style>
