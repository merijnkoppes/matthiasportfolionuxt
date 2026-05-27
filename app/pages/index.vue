<template>
  <main class="home-page">
    <div id="row1">
      <h1>Matthias van Houtum</h1>
    </div>

    <NuxtImg
      id="portretfoto"
      src="/img_8137.jpeg"
      alt="een mooie foto van Matthias van houtum"
      loading="eager"
      fetchpriority="high"
      format="webp"
      quality="80"
      sizes="85vw sm:400px md:600px lg:900px"
    />

    <p class="paragraph1 para">
      From a young age, I've been captivated by the human experience of
      perceiving the world around us, how we shape our realities, and the
      narratives we construct. Currently, I'm pursuing my studies in IMT, Image
      and Media Technology at HKU; University of the Arts Utrecht.
    </p>

    <p class="paragraph1">
      In my own visuals, I strive to show the extraordinary within the seemingly
      ordinary and to liberate reality from the invented frameworks we impose on
      it. I draw inspiration from my immediate surroundings, such as nature and
      the urban landscape, the often beautiful erosion of lifeless objects, and
      life beyond the everyday theater of humanity. I currently utilize various
      media such as photography, graphic design, and videography.
    </p>

    <p id="paragraph2">
      You can contact me directly through <br />
      Instagram:
      <a
        href="https://www.instagram.com/matthias.van.houtum/"
        target="_blank"
        rel="noopener noreferrer"
      >
        @houtum.van.matthias
      </a>
    </p>
  </main>
</template>

<style scoped lang="scss">
#row1 {
  width: 100%;
  display: flex;
  justify-content: flex-start;
  align-items: center;
  flex-direction: column;

  & h1 {
    display: flex;
    margin: 20px 0 50px 0;
    font-size: 38px;
    line-height: 44px;
  }
}

#portretfoto {
  display: block;
  width: 900px;
  height: auto;
  margin: 43px auto 16px auto;
}

.paragraph1 {
  text-align: left;
  flex-flow: column;
  margin: 2% 3%;
  font-family:
    Georgia,
    Times,
    Times New Roman,
    serif;
  font-size: 15px;
  line-height: 20px;
}

.para {
  margin-bottom: 1lh;
}

#paragraph2 {
  text-align: center;
  padding-top: 0%;
  padding-left: 0%;
  padding-right: 0;
  margin-top: 78px;
  font-size: 14px;
  line-height: 20px;
}

@media (max-width: 1024px) {
  .home-page {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  #portretfoto {
    width: 600px;
    margin-top: 30px;
  }

  .paragraph1 {
    width: 550px;
  }

  #paragraph2 {
    margin-top: 168px;
  }

  #row1 {
    & h1 {
      font-size: 28px;
    }
  }
}

@media (max-width: 768px) {
  .home-page {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  #portretfoto {
    width: 400px;
    margin-top: 20px;
  }

  .paragraph1 {
    width: 380px;
  }

  #paragraph2 {
    margin-top: 168px;
  }
}

@media (max-width: 480px) {
  .home-page {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  #portretfoto {
    width: 85vw;
    margin-top: 20px;
  }

  .paragraph1 {
    width: 80vw;
    font-size: 13px;
    line-height: normal;
  }

  #paragraph2 {
    margin-top: 120px;
  }

  #row1 {
    & h1 {
      font-size: 23px;
    }
  }
}
</style>
