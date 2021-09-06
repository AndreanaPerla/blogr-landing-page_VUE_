<template>
  <div class="desingForFuture-container">
    <h1>Designed for the future</h1>
    <div class="designForFuture-sectionUp">
      <div class="sectionUp-text">
        <h4>Introducing an extensible editor</h4>
        <p>
          Blogr features an exceedingly intuitive interface which lets you focus
          on one thing: creating content. The editor supports management of
          multiple blogs and allows easy manipulation of embeds such as images,
          videos, and Markdown. Extensibility with plugins and themes provide
          easy ways to add functionality or change the looks of a blog.
        </p>
        <h4>Robust content management</h4>
        <p>
          Flexible content management enables users to easily move through
          posts. Increase the usability of your blog by adding customized
          categories, sections, format, or flow. With this functionality, you're
          in full control.
        </p>
      </div>
      <div class="sectionUp-img">
        <img
          src="../images/illustration-editor-desktop.svg"
          alt="illustration-editor"
        />
      </div>
    </div>
    <StateOfArt />
    <div class="designForFuture-sectionDown">
      <div class="sectionDown-img">
        <img
          src="../images/illustration-laptop-desktop.svg"
          alt="illustration-laptop"
        />
      </div>
      <div class="sectionDown-text">
        <h4>Free, open, simple</h4>
        <p>
          Blogr is a free and open source application backed by a large
          community of helpful developers. It supports features such as code
          syntax highlighting, RSS feeds, social media integration, third-party
          commenting tools, and works seamlessly with Google Analytics. The
          architecture is clean and is relatively easy to learn
        </p>
        <h4>Powerful tooling</h4>
        <p>
          Batteries included. We built a simple and straightforward CLI tool
          that makes customization and deplyment a breeze, but capable of
          producing even the most complicated sites.
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import StateOfArt from "./StateOfArt.vue";

export default {
  name: "DesignForFuture",
  components: {
    StateOfArt,
  },
};
</script>

<style scoped>
.desingForFuture-container {
  padding-top: 10%;
  padding-bottom: 9%;
  position: relative;
  overflow-x: hidden;
}

.desingForFuture-container h1,
.desingForFuture-container h4 {
  color: hsl(208, 49%, 24%);
  letter-spacing: 0.025rem;
}

.desingForFuture-container p {
  color: hsl(207, 13%, 34%);
  letter-spacing: 0.025rem;
}

.desingForFuture-container h1 {
  text-align: center;
  padding-bottom: 6.5%;
  font-weight: bold;
  font-size: 2.5vw;
}

.designForFuture-sectionUp {
  display: flex;
  padding-left: 10.5%;
  padding-bottom: 11%;
}

.designForFuture-sectionDown {
  display: flex;
  justify-content: flex-end;
  padding-right: 10.5%;
  padding-top: 22.5%;
}

.sectionUp-text,
.sectionDown-text {
  width: 44.5%;
}

.sectionUp-text h4,
.sectionDown-text h4 {
  font-size: 2vw;
  padding-bottom: 5.25%;
}

.sectionUp-text p,
.sectionDown-text p {
  line-height: 1.75rem;
  padding-bottom: 14%;
}

.sectionUp-img {
  position: absolute;
  top: 2.5%;
  right: -19%;
}

.sectionDown-img {
  position: absolute;
  bottom: 5%;
  left: -18.5%;
}

.sectionUp-img img,
.sectionDown-img img {
  width: 64vw;
}

@media (max-width: 800px) {
  .desingForFuture-container h1 {
    font-size: 3vw;
  }

  .designForFuture-sectionUp {
    display: flex;
    flex-direction: column-reverse;
    align-items: center;
    padding-left: 0;
    padding-bottom: 22%;
  }

  .designForFuture-sectionDown {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: unset;
    padding-right: 0;
    padding-top: 11%;
  }

  .sectionUp-text h4,
  .sectionDown-text h4 {
    font-size: 2.5vw;
    padding-bottom: 3%;
  }

  .sectionUp-img {
    position: relative;
    top: 0;
    right: 0;
    padding-bottom: 7%;
  }

  .sectionDown-img {
    position: relative;
    bottom: 0;
    left: 0;
    padding-bottom: 7%;
  }

  .sectionUp-text,
  .sectionDown-text {
    width: 80%;
    text-align: center;
  }

  .sectionUp-text p,
  .sectionDown-text p {
    padding-bottom: 7%;
  }
}

@media (max-width: 480px) {
  .desingForFuture-container h1 {
    font-size: 5vw;
  }

  .sectionUp-img img,
  .sectionDown-img img {
    width: 90vw;
  }

  .designForFuture-sectionUp {
    padding-bottom: 35%;
  }

  .sectionUp-text h4,
  .sectionDown-text h4 {
    font-size: 4vw;
  }
}
</style>
