<script setup>
</script>

<template>
    <div class="leftnavbar">
        <label for="initial">JLC</label><br>
        <div class="btn-container">
            <input type="radio" id="home" name="menu">
            <label for="home" class="right-nav-btn">Home</label>
            <br>
            <input type="radio" id="about-me" name="menu">
            <label for="about-me" class="right-nav-btn">About Me</label>
            <br>
            <input type="radio" id="projects" name="menu">
            <label for="projects" class="right-nav-btn">Projects</label>
            <br>
            <input type="radio" id="work-exp" name="menu">
            <label for="work-exp" class="right-nav-btn">Work Experience</label>
            <br>
            <input type="radio" id="contact" name="menu">
            <label for="contact" class="right-nav-btn">Contacts</label>
        </div>
    </div>
</template>

<style>
.leftnavbar{
    position: fixed;
    left: 0;
    top: 0;
    display: auto;
    background-color: black;
    height: 960px;
    width: 285px;
    flex-direction: column;
    align-items: flex-start;
    justify-content: left;
}
.btn-container{
    display: flex;
}

.right-nav-btn {
    display: block; /* Makes them stack vertically */
    width: 100%; /* Full width of the navbar */
    background-color: #2c3e50; /* Button color */
    color: white; /* Text color */
    padding: 15px; /* Space inside button */
    text-align: center; /* Center text */
    font-size: 18px; /* Text size */
    font-weight: bold;
    border: none;
    cursor: pointer;
    transition: background 0.3s ease;
}

.right-nav-btn:hover {
    background-color: #34495e; /* Darker shade */
}

/* Selected effect */
input[type="radio"]:checked + .right-nav-btn {
    background-color: #1abc9c; /* Highlighted selection */
}

/* Align the buttons */
.btn-container {
    display: flex;
    flex-direction: column; /* Stack items vertically */
    gap: 10px; /* Add spacing between buttons */
}
input[type="radio"] {
    display: none; /* Completely hides the radio buttons */
}

</style>