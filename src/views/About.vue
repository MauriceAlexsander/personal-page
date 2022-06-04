<template>
  <div class="container about">
    <div class="appear-animation about-content d-flex flex-column align-items-start py-5 px-4">
      <h1 class="py-4">About me.</h1>
      <p>Hi, I'm a <strong>self-taught</strong> brazilian web developer, and I loves what I do.</p>
      <p>I've always been passionate about solving <strong>problems</strong>, so nothing more natural than do it for living.</p>
      <p>I like to think inside and outside the box to find <strong>simple</strong> and <strong>elegant</strong> solutions</p>
      <p>My goal is to make a <strong>difference</strong>, I always give my 100%.</p>

      <h3 class="pt-5 py-4">What I do when I am not programming?</h3>
      <p>Spend time with my friends or by myself.</p>
      <p>I really like NFL, Formula 1 and more recently started to watch, MotoGP.</p>
    </div>
  </div>
</template>

<style scoped>
.about {
  padding: 0 72px;
}

.about-content {
  text-align: start;
}

strong {
  background: white;
  color: black;
  padding: 2px;
  border-radius: 4px;
  transition: .3s;
}

strong:hover {
  background: var(--light-green);
}

@media screen and (max-width: 991px){
  .about {
    padding: 0 24px;
  }
}

@media screen and (max-width: 768px){
  .about {
    padding: 0px;
  }
}

</style>
