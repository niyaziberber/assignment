<template>
  
  <div id="app" class="container-fluid">
    <div class="row">
      <div class="col content">
        <div class="row">
          <div class="col">
            <TitleBackground></TitleBackground>
            <MainTitle :title="mainTitle" class="title"></MainTitle>
          </div>
        </div>
        <div class="row">
          <div class="col">
          <Subtitle :subtitle="subtitle" class="subtitle"></Subtitle>
          </div>
        </div>
        <div class="row">
          <div class="col">
          <BodyText :bodyText="bodyText" class="bodyText"></BodyText> 
          </div>
        </div>
      </div>
      <div class="col">
        <div id="style"></div>
        <Picture></Picture>
      </div>
    </div>  
    <div class="row" id="inputRow">
      <div class="col">
        <TitleInput @newTitle="updateTitle"></TitleInput>
      </div>
      <div class="col">
        <TextareaInput @newTextBody="updateSubtitle" :maxLength=50 newPlaceholder="Subtitle"></TextareaInput>
      </div>
      <div class="col">
        <TextareaInput @newTextBody="updateBodyText" :maxLength=150 newPlaceholder="Body"></TextareaInput>
      </div>  
    </div> 
  </div>

</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Picture from './components/Picture.vue';
import MainTitle from './components/MainTitle.vue';
import BodyText from './components/BodyText.vue';
import TitleInput from './components/TitleInput.vue';
import TextareaInput from './components/TextareaInput.vue';
import Subtitle from './components/Subtitle.vue';
import TitleBackground from './components/TitleBackground.vue';

@Component({
  components: {Picture, MainTitle, BodyText, TitleInput, TextareaInput, Subtitle, TitleBackground},

})

export default class App extends Vue {

  public mainTitle: string = 'Lorem ipsum dolor sit amet, consectetur adipiscing';
  public subtitle: string = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit';
  public bodyText: string = 'Lorem ipsum dolor sit amet, consectetur dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur cillum dolore eu...';

  public updateTitle(title: string) {
    this.mainTitle = title;
  }
  public updateBodyText(bodyText: string) {
    this.bodyText = bodyText;
  }
  public updateSubtitle(subtitle: string) {
    this.subtitle = subtitle;
  }

}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css?family=Chewy|Gaegu&display=swap');
$primary: #AA98D8;
$secondary: #FBBBD3;
#app {
    position: relative;
    font-family: 'Avenir',Helvetica,Arial,sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    overflow: hidden;
    background-color: $primary;
    width: 1920px;
    height: 1080px;
}
#style {
    position: absolute;
    float: right;
    width: 582.94px;
    height: 582.94px;
    border: 46.858px solid #FFFED4;
    border-radius: 50%;
    height: 582.94px;
    right: -258px;
    top: -136.09px;
}
#inputRow {
    position: relative;
    margin-top: 177px;
    margin-left: 197px;
}
.title {
    left: 124px;
    top: -42px;
    width: 950px;
    height: 248px;
    text-align: center;
    padding: 10px;
}
.subtitle {
    left: 140px;
    top: -18px;
    width: 922px;
    height: 150px;
    text-align: center;
    padding: 10px;
}
.bodyText {
    left: 133px;
    top: 66px;
    width: 922px;
    height: 150px;
    text-align: left;
    padding: 10px;
}
textarea {
    border: {
        radius: 7%;
        color: #939292;
    }
}
content {
    width: 750px;
    height: 750px;
    align-content: center;
}
</style>

