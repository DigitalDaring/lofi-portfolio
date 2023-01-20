<script>
    import Nav from '$lib/nav/Nav.svelte';
    import AuthorIcon from '$lib/author-icon/author-icon.svelte';
</script>
<section class="classy-page">
    <section class="intro-stuff">
        <AuthorIcon/>
        <h1>SHIPS IN THE NIGHT</h1>
        <p class="thin-boy">
            This debut novel of author Edmund Bates follows Madeline Carver; a dock worker
            at The Shipping Company.  Working for an import / export business that caters to the supernatural
            isn't always easy, but it does pay well and they don't ask too many questions.
        </p>
        <p class="thin-boy">
            When a particularly expensive delivery goes missing, Madeline gets roped into helping track it down with the help of
            her haunted 1984 Monte Carlo and the ghost that is trapped within.  Maddie combs through the weird and
            unnatural parts of Florida looking for the missing package, but some things may be better left
            lost.
        </p>
    </section>
    <section class="epic-stuff">
        <Nav/>
        <img src="shipping_container_ink.png" id="shipping-container-image"/>
    </section>
</section>
<style lang="scss">

    .classy-page {
      width: 100%;
      height: 100%;
      background-color: rgb(5, 7, 7);
      display: flex;
      flex-direction: row;

      .intro-stuff {
        width: 200px;
        background-color: #FEFDFD;

        h1 {
          font-size: 32px;
          margin: 0;
          padding-left: 12px;
          margin-bottom: 10px
        }

        p {
          font-size: 10px;
          padding: 5px 14px;
          z-index: 999;
          position: relative;
          text-shadow: #fff 1px 0 10px;
          opacity: .6;
        }
      }

      .epic-stuff {
        width: calc(100% - 200px);
        display: grid;
        grid-template-columns: 100%;
        grid-template-rows: 45px 32px auto;
        grid-template-areas: 'header'
                             ' . '
                             'image';
        flex-direction: column;
        background-color: #000;
        background-image: linear-gradient(to left, rgba(0,0,0,0), rgba(54,56,53,1));
      }

      #shipping-container-image {
        width: 854px;
        margin-left: -154px;
        grid-area: image;
      }

    }
</style>