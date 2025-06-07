<script setup>
</script>

<template>
    <div class="leftnavbar">
        <div class="btn-container">
            <input type="radio" id="home" name="menu">
            <label for="home" class="left-nav-btn">Home</label>
            <br>
            <input type="radio" id="about-me" name="menu">
            <label for="about-me" class="left-nav-btn">About Me</label>
            <br>
            <input type="radio" id="projects" name="menu">
            <label for="projects" class="left-nav-btn">Education</label>
            <br>
            <input type="radio" id="work-exp" name="menu">
            <label for="work-exp" class="left-nav-btn">Experience</label>
            <br>
            <input type="radio" id="contact" name="menu">
            <label for="contact" class="left-nav-btn">Contact Me</label>
        </div>
    </div>

</template>

<style>
.leftnavbar{
    position: fixed;
    left: 0;
    top: 0;
    bottom: 0;
    display: auto;
    background-color: black;
    height: auto;
    width: 285px;
    flex-direction: column;
    align-items: center;
    justify-content: flex;
}

.btn-container{
    justify-content: center;
    display: flex;
    align-items: center;
    height: 100vh;  
}

.left-nav-btn {
    width: 50%;
    display: block; 
    color: white;
    padding: 15px;
    text-align: center;
    font-size: 18px;
    font-weight: bold;
    border: none;
    cursor: pointer;
    border-radius: 20px;
    transition: ease, 0.7s;
}

.left-nav-btn:hover {
    background-color: white;
    color:black;
    width: 50%;
    border-radius: 20px;
}

input[type="radio"]:checked + .left-nav-btn {
    background-color: white;
    color: black;
    width: 50%;
    border-radius: 20px;
}

.btn-container {
    display: flex;
    flex-direction: column;
    gap: 10px;
}
input[type="radio"] {
    display: none;
}

</style>