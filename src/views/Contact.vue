<template>
  <div class="contact-page py-5">
    <div class="container d-flex justify-content-center py-4">
      <div class="appear-animation items d-flex flex-column align-items-start py-3 px-4">
        <h1 class="font-weight-bold py-4">Contact</h1>
        <h3>Talk to me by send an email to</h3>
        <a class="p-1 my-2" href="mailto:mauricezanotelli@gmail.com">mauricezanotelli@gmail.com</a>
        <p class="py-2">I am more than welcome to answer and talk, normally I am active at 12:00 GMT to 20:00 GTM</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.contact-page {
  height: 100%;
  text-align: start;
}

h1 {
  font-size: 4.5rem;
}

a {
  font-size: 1.5rem;
  background: white;
  border-radius: 6px;
  text-decoration: none;
  color: black;
  transition: .3s;
}

a:hover {
  background: var(--light-green);
}

p {
  font-size: 1.25rem;
  text-align: left;
}

h1 {
  font-size: 4.5rem;
}

@media screen and (max-width: 575px) {
  h1 {
    font-size: 3.5rem;
  }

  h3 {
    font-size: 1.15rem;
  }

  a {
    font-size: 1rem;
  }

  p {
    font-size: 1rem;
  }
}
</style>
