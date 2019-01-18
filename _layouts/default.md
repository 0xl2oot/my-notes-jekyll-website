<!DOCTYPE html>
<html lang="{{ page.lang | default: site.lang | default: "en" }}">

  {%- include head.html -%}

  <body>

    {%- include header.html -%}

    <main class="page-content" aria-label="Content">
      <div class="wrapper">
        {{ content }}
      </div>
    </main>

    {%- include footer.html -%}

  </body>

</html>

<style>
.wrapper {
  max-width: -webkit-calc(1200px - (30px * 2));
  max-width: calc(1200px - (30px * 2));
  margin-right: auto;
  margin-left: auto;
  padding-right: 30px;
  padding-left: 30px;
  }
  @media screen and (max-width: 1200px) {
    .wrapper {
      max-width: -webkit-calc(1200px - (30px));
      max-width: calc(1200px - (30px));
      padding-right: 15px;
      padding-left: 15px; } }
</style>