<template>
  <div class="container">
    <div class="title"><h1>Title</h1></div>
    <div class="screen">
      <img class="testimg" src="../assets/test2.jpg" />
      <br />
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Tristique magna sit
        amet purus gravida quis blandit turpis cursus. In tellus integer feugiat
        scelerisque varius morbi enim nunc. Fermentum dui faucibus in ornare
        quam. Aliquet nibh praesent tristique magna sit amet. Et netus et
        malesuada fames ac turpis. At ultrices mi tempus imperdiet nulla.
        Ullamcorper dignissim cras tincidunt lobortis feugiat. Ut morbi
        tincidunt augue interdum velit euismod in pellentesque. Id aliquet risus
        feugiat in ante metus dictum at. Risus in hendrerit gravida rutrum
        quisque non tellus orci ac. Ornare aenean euismod elementum nisi quis
        eleifend quam. Quis risus sed vulputate odio ut.
      </p>
      <br />
      <p>
        Quis blandit turpis cursus in hac habitasse platea dictumst. Porttitor
        eget dolor morbi non arcu risus quis varius quam. Sed tempus urna et
        pharetra pharetra massa. Enim nec dui nunc mattis enim ut tellus
        elementum. Fringilla ut morbi tincidunt augue interdum velit. Aliquet
        eget sit amet tellus. Nascetur ridiculus mus mauris vitae ultricies leo
        integer. Ultrices tincidunt arcu non sodales. Purus in mollis nunc sed
        id semper risus in hendrerit. Pretium vulputate sapien nec sagittis
        aliquam malesuada bibendum arcu vitae. Phasellus vestibulum lorem sed
        risus ultricies tristique nulla aliquet enim. Lorem mollis aliquam ut
        porttitor leo a diam sollicitudin. Egestas sed tempus urna et pharetra
        pharetra. Tristique magna sit amet purus gravida quis blandit turpis
        cursus. Id aliquet lectus proin nibh nisl condimentum id venenatis.
        Adipiscing enim eu turpis egestas pretium. Scelerisque eleifend donec
        pretium vulputate. Euismod in pellentesque massa placerat.
      </p>
      <br />
      <p>
        Viverra nam libero justo laoreet sit. Purus semper eget duis at tellus
        at. Viverra nam libero justo laoreet. Augue lacus viverra vitae congue
        eu. Vel quam elementum pulvinar etiam non quam. Facilisi nullam vehicula
        ipsum a arcu cursus vitae. Mattis enim ut tellus elementum. Arcu dui
        vivamus arcu felis bibendum ut tristique. At auctor urna nunc id cursus
        metus aliquam. Donec pretium vulputate sapien nec. Morbi non arcu risus
        quis varius quam. Quam viverra orci sagittis eu volutpat odio facilisis
        mauris. Elementum integer enim neque volutpat ac tincidunt vitae semper.
        Dolor sit amet consectetur adipiscing elit ut aliquam purus. Egestas
        maecenas pharetra convallis posuere morbi leo urna molestie. Nunc
        lobortis mattis aliquam faucibus purus in massa tempor nec. Vestibulum
        lectus mauris ultrices eros. Eget velit aliquet sagittis id consectetur
        purus ut. Ipsum faucibus vitae aliquet nec ullamcorper sit amet risus.
        Malesuada pellentesque elit eget gravida cum sociis natoque penatibus
        et.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Screen",
  computed: {
    innerHeight: function() {
      return window.innerHeight;
    },
    outerHeight: function() {
      return window.outerHeight;
    },
    availHeight: function() {
      return window.screen.availHeight;
    },
    innerWidth: function() {
      return window.innerWidth;
    },
    outerWidth: function() {
      return window.outerWidth;
    },
    availWidth: function() {
      return window.screen.availWidth;
    },
  },
  mounted: function() {
    console.log("blah");
  },
};
</script>

<style scoped>
.screen {
  margin: auto;
  width: 95%;
  /* height: 90%; */
  min-height: 90%;
  display: flex;
  flex-direction: column;
}
.container {
  width: 100%;
  min-height: 100%;
  scroll-snap-align: start;
  /* margin-left: 1%; */
  /* margin-right: 1%; */
}
.title {
  height: 10%;
  margin: 0px;
  padding-top: 10px;
  padding-bottom: 5px;
}
.title > h1 {
  margin-block-start: 0px;
  margin-block-end: 0px;
  margin: 0px;
  font-size: 7.5vh;
}
.testimg {
  max-width: 100%;
  max-height: 50vh;
  width: 1200px;
  object-fit: contain;
  margin: auto;
  flex-shrink: 1;
}
p {
  text-align: left;
  width: 1200px;
  max-width: 100%;
  margin: auto;
}
</style>
