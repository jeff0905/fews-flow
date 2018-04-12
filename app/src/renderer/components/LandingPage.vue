<template>
  <div id="wrapper">
    <main>
      <div class="left-side">
        <span class="title">
          欢迎来到前端世界, be happy to work!
        </span>
        <section class="project-section">
          <div class="projects">
              <div class="name">项目框架</div>
              <div class="items">
                <div class="item">
                  <div class="item-logo"></div>
                  <div class="item-name">活动框架</div>
                  <div class="item-desp">市场，运营所做的活动页面的框架</div>
                </div>
              </div>
          </div>
          <div class="projects">
              <div class="name">H5应用-vue</div>
              <div class="items">
                <div class="item">
                  <div class="item-logo"></div>
                  <div class="item-name">活动框架</div>
                  <div class="item-desp">市场，运营所做的活动页面的框架</div>
                </div>
              </div>
          </div>
        </section>
      </div>

      <div class="right-side">
        <div class="doc">
          <div class="title">我的仓库</div>
          <p>
            这里收藏了很多前端,框架, 工具,.....
          </p>
         </div>
        <div class="lists">
          <div class="list">
              <div class="name">工具</div>
              <ul class="items">
                  <li class="item">
                   <button @click="open('https://simulatedgreg.gitbooks.io/electron-vue/content/')">Webpack</button><br><br>
                  </li>
              </ul>
          </div>
          <div class="title alt">Other Documentation</div>
          <button class="alt" @click="open('https://electron.atom.io/docs/')">Electron</button>
          <button class="alt" @click="open('https://vuejs.org/v2/guide/')">Vue.js</button>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
  // import SystemInformation from './LandingPage/SystemInformation'

  export default {
    name: 'landing-page',
    // components: { SystemInformation },
    methods: {
      open (link) {
        this.$electron.shell.openExternal(link)
      }
    }
  }
</script>

<style lang="less">
  // @import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body { font-family: 'Source Sans Pro', sans-serif; }

  #wrapper {
    background:
      radial-gradient(
        ellipse at top left,
        rgba(255, 255, 255, 1) 40%,
        rgba(229, 229, 229, .9) 100%
      );
    height: 100vh;
    padding: 60px 80px;
    width: 100vw;
  }

  #logo {
    height: auto;
    margin-bottom: 20px;
    width: 420px;
  }

  main {
    display: flex;
    justify-content: space-between;
  }

  main > div { flex-basis: 50%; }

  .left-side {
    display: flex;
    flex-direction: column;

    .project-section{
      display:flex;
      flex-direction: row;
      .projects {
        flex:1;
        background: #ddd;
        // color:#fff;
        margin:0 10px;
        box-shadow:0 0 2px 2px rgba(0,0,0,.15);
        &:hover{
          cursor: pointer;
        }
      }
    }
  }

  .welcome {
    color: #555;
    font-size: 23px;
    margin-bottom: 10px;
  }

  .title {
    color: #2c3e50;
    font-size: 20px;
    font-weight: bold;
    margin-bottom: 6px;
  }

  .title.alt {
    font-size: 18px;
    margin-bottom: 10px;
  }

  .doc p {
    color: black;
    margin-bottom: 10px;
  }

  .doc button {
    font-size: .8em;
    cursor: pointer;
    outline: none;
    padding: 0.75em 2em;
    border-radius: 2em;
    display: inline-block;
    color: #fff;
    background-color: #4fc08d;
    transition: all 0.15s ease;
    box-sizing: border-box;
    border: 1px solid #4fc08d;
  }

  .doc button.alt {
    color: #42b983;
    background-color: transparent;
  }
</style>
