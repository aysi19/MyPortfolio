<script setup>
    
</script>

<template>
  <div class="content-container">
    <div class="txt-container">
      <div class="text-inner">
        <p class="txt-hi">Hi there,</p>
        <p class="txt-josh">I am Josh Lendl Cagara</p>
      </div>
      <br>
      <a href="Resume2.pdf" download class="download-btn">
        Download CV
      </a>
    </div>

    <div class="picture-container">
      <!-- Add image or other content here -->
    </div>
  </div>
</template>

<style>

.content-container{
    position: fixed;
    top: 0;
    left: 285px;
    right: 0;
    bottom: 0;
    background-color: white;
    display: flex;
    width: calc(100% - 285px);
}
.txt-container{
    margin-top: auto;
    margin-bottom: auto;
    left: 285px;
    width: calc(75% - 285px);
    background-color: white;
    display: flex;
    color: black;
    flex-direction: column;
    align-items: center;
}
.txt-hi,.txt-josh{
    display: block;
    font-size: 50px;
}
.download-btn {
    width: 20%;
    display: block; 
    color: black;
    padding: 10px;
    text-align: center;
    font-size: 18px;
    font-weight: bold;
    border: 4px solid black;
    background-color: white;
    cursor: pointer;
    border-radius: 20px;
    transition: ease, 0.7s;
}

.download-btn:hover {
    background-color: black;
    color:white;
    width: 20%;
    border-radius: 20px;
}

input[type="radio"]:checked + .download-btn {
    background-color: black;
    color: white;
    width: 20%;
    border-radius: 20px;
}

</style>