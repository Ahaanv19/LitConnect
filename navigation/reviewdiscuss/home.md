---
layout: post 
title: Moderator's Picks
search_exclude: true
permalink: /voteforthegoat/home
menu: nav/vote_for_the_goat.html
---

<style>
    body {
        font-family: 'Poppins', sans-serif;
        background-color: #000;
        color: #e0e0e0;
        padding: 20px;
    }

    h2, h3 {
        color: #00d4ff;
        margin-bottom: 10px;
    }

    p {
        margin-bottom: 15px;
    }

    .group-theme {
        background: #ff69b4;
        color: #e0e0e0;
        padding: 15px;
        border-radius: 10px;
        margin-bottom: 20px;
        box-shadow: 0 4px 8px 0 rgba(0, 212, 255, 0.2), 0 6px 20px 0 rgba(0, 212, 255, 0.19);
        border: 1px solid #00d4ff;
    }

    .group-theme h3 {
        margin-top: 0;
    }
</style>

## Welcome to Moderator's Picks!

In this Zone, view the book off the week, with the moderators honest review and 5 star raiting, and then enjoy disscussing with other readers, in the discussion chat, your thoughts and opionions on the moderators review, and have conversations with others about your own feelings. 

### Group Themes and Activities

<div class="group-theme">
    <strong>Sneek Peek</strong>  
    This weeks Book is..... THE HUNGER GAMES!! Check out the Moderators Review!
</div>

<script>
    // Function to fetch preferences from the backend
    function loadPreferences() {
        fetch('http://localhost:8887/api/preferences')
        .then(response => response.json())
        .then(data => {
            // Update the page with the preferences
            const menuElement = document.getElementById('menu');
            const textElement = document.getElementById('text');

            if (menuElement) {
            menuElement.innerText = `Menu: ${data.menu}`;
            }

            if (textElement) {
            textElement.innerText = `Text: ${data.text}`;
            }

            // Apply text color to <p> elements
            let pColors = document.querySelectorAll('p');
            pColors.forEach(p => {
            p.style.color = data.text;
            });

            // Change menu text color
            let menuItems = document.querySelectorAll('.menu-item');
            menuItems.forEach(item => {
            item.style.color = data.menu;  // Apply menu color to each item
            });

            let ulItems = document.querySelectorAll('.ul-item');
            ulItems.forEach(item => {
            item.style.color = data.text
            });

            let liItems = document.querySelectorAll('li');
            liItems.forEach(item => {
            item.style.color = data.text
            });

        })
        .catch(error => {
            console.error('Error fetching preferences:', error);
        });
    }

    // Load preferences when the page is loaded
    window.onload = loadPreferences;
</script>