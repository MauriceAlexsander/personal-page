<template>
<div class="external-links">
    <a href="https://github.com/MauriceAlexsander" target="_blank">
      <img src="@/assets/GitHub-Mark-32px.png" alt="Personal Page in Github"/>
    </a>
    <a href="https://www.linkedin.com/in/mauricezanotelli/" target="_blank">
      <img src="@/assets/linkedin.svg" alt="Personal Page in Github"/>
    </a>
</div>
</template>

<style scoped>
.external-links a {
  padding: 12px;
}

.external-links a img {
  height: 24px; 
  width: 24px; 
  filter: invert(70%);
  transition: 0.2s;
}

.external-links a:nth-child(2) img {
  filter: invert(60%);
}

.external-links a:nth-child(1) img:hover {
  filter: invert(100%);
}

.external-links a:nth-child(2) img:hover {
  filter: invert(90%);
}

</style>
