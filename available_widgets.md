Here on Askdata, we provide different types of visualizations such as Charts, Widgets and much more. In this page, we aim to provide a more detailed explanation of Widgets and their usage. 

You can have a preview of what a Widget looks like in the following video:



Every widget type you can use on our platform has it's own configuration, that is mainly because every type of graphical representation needs its own structure of the input data. For that reason, we provide a detailed explanation of each Widget:

<style>
 
html, body {
  height: 100%;
  width: 100%;
}

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#wrapper {
  height: 100%;
  width: 100%;
}

.custom-shadow {
  box-shadow: 0 14px 28px rgba(0, 0, 0, 0.25), 0 10px 10px rgba(0, 0, 0, 0.22);
}

.custom-shadow-sm {
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
}

/* In FontawesomePicker.vue <style scoped lang="scss" /> */
.icon-preview-fade-enter-active, .icon-preview-fade-leave-active {
  transition: opacity 0.25s;
}

.icon-preview-fade-enter, .icon-preview-fade-leave-to {
  opacity: 0;
}

.preview-container {
  width: 100%;
  position: relative;
}

.previewer {
  position: absolute;
  width: 100%;
  min-height: 50px;
  max-height: 500px;
  overflow: auto;
  background: white;
  top: 10px;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: center;
  transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
}

.icon-preview {
  width: 20%;
  padding-top: 20%;
  position: relative;
}
@media (max-width: 800px) {
  .icon-preview {
    width: 33%;
    padding-top: 33%;
  }
}
.icon-preview .icon-wrapper {
  position: absolute;
  height: 80%;
  width: 80%;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  margin: auto;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
  transition: ease-in-out all 0.25s;
}
.icon-preview .icon-wrapper:hover, .icon-preview .icon-wrapper.selected {
  background: #42b883;
  color: #fbfbfb;
}
.icon-preview .icon-wrapper i {
  font-size: 4vw;
}
  
 </style>


<div id="app"><App/></div>



![pic1](https://raw.githubusercontent.com/Edoardoba/test/main/6kpi.png)
