<section id="layout">
    <img src="left-splotch.png" id="left-splotch"/>
    <section id="content">
        <slot></slot>
    </section>
    <img src="right-splotch.png" id="right-splotch"/>
</section>

<style lang="scss">
  #layout {
    display: grid;
    grid-template-columns: 128px 800px 128px;
    grid-template-rows: 100px 625px 100px;
    grid-template-areas: '.           .       .'
                         'leftsplotch content rightsplotch'
                         '.           .       rightsplotch';
    width: 1056px;
    margin: 0 auto;
    font-family: sans-serif;

    #left-splotch {
      width: 128px;
      grid-area: leftsplotch;
    }

    #right-splotch {
      width: 128px;
      grid-area: rightsplotch;
    }

    #content {
      grid-area: content;
      box-shadow: rgba(0, 0, 0, .8) 8px 18px 32px;
    }
  }
</style>
