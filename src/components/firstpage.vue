<template>
  <div class="page1">
    <div class="header">SU HAO</div>
    <div class="wrapper">
      <div class="title">Contact</div>
      <div class="line"></div>
      <div class="content">

        <div class="item">
          Email:&nbsp;<a class="info" href="mailto:basicInformation.email">{{
            basicInformation.email
          }}</a>
        </div>
        <div class="item">
          <a class="info" href="https://github.com/suhao0628?tab=repositories" >GitHub</a>
          &nbsp;&nbsp;&nbsp;
          <a href="https://discordapp.com/users/#3002" class="info">Discord</a>
        </div>
        <br>
      </div>
      <div class="title">Intention</div>
      <div class="line"></div>
      <div class="content">
        <div>
          Interested Position:&nbsp;&nbsp;<span class="info" style="color: #3498db;">{{ jobIntention.position }}</span>
        </div>

      </div>
      <div class="title">Education</div>
      <div class="line"></div>
      <div class="content">
        <div class="item">
          University:&nbsp;<span class="info">{{
            educationalBackground.graduationSchool
          }}</span>
        </div>

        <div class="item">
          Major:&nbsp;<span class="info">{{ educationalBackground.major }}</span>
        </div>
      </div>

      <div class="title">Skills</div>
      <div class="line"></div>
      <ul class="list">
        <b>I'm currently using .NET and VUEjs to build web application </b>
        <li v-for="(item, index) in skills" :key="index">
          <span v-if="item.includes(':')">
            <strong>{{ item.split(':')[0] }}:</strong>{{ item.split(':')[1] }}
          </span>
          <span v-else>{{ item }}</span>
        </li>

      </ul>
      <div class="title">Experiences</div>
      <div class="line"></div>
      <div class="project">
        <div class="project-title">{{project.first.title}}</div>
        <br>
        <span class="tag" style="background-color: #3498db;" v-for="(tag, index) in project.first.techTags" :key="index">
          {{ tag }}
        </span>
        <div class="subtitle">Description:</div>
        <div class="project-desc">
          {{project.first.desc}}
        </div>
        <div class="subtitle">Project content:</div>
        <ol class="list">
          <li v-for="(item, index) in project.first.duty" :key="index">
            {{ item }}
          </li>
        </ol>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Page1Index',
  props: ['basicInformation', 'jobIntention', 'educationalBackground', 'skills', 'certificates', 'project']
}
</script>

<style lang="less" media="print">
@media print {
  a {
    display: inline !important;
  }
}
.page1 {
  margin: 0 auto;
  width: 800px;
  height: 1100px;
  background-color: #fff;
  .header {
    text-align: center;
    height: 45px;
    line-height: 45px;
    background-color: rgb(65, 65, 65);
    color: #fff;
    font-size: 20px;
  }
  .wrapper {
    margin: 20px 50px;
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
  b {
      text-decoration: underline;
    }
    .line {
      border-top: 2px solid rgb(65, 65, 65);
    }
    .content {
      display: flex;
      flex-wrap: wrap;
      margin: 20px 25px;
      font-size: 16px;
      font-weight: bold;
      .item {
        width: 50%;
        height: 25px;
        line-height: 25px;
        .info {
          font-weight: normal;
        }
      }
    }
    .project {
      margin: 20px 25px;
      font-size: 16px;
      .subtitle {
        margin: 2px 0;
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
  }
}
</style>
