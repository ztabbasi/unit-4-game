# Name of project

Crystal Game: A number between 19 and 120 is picked.  Upto user to pick one of the four crystals with hidden values to match the number picked.  User to continue picking number until  he matches the picked number.  User loses if his counter is above the picked number.  

# Link to the site

[Crystal Game](https://ztabbasi.github.io/unit-4-game/)

# Images

![Picture]

# Technologies used

HTML
CSS
Javascript
Jquery


# code snippets

Test which crystal was clicked and add based on the crystal's hidden value and check if still below total
 
    var crystalValue = ($(this).attr("data-crystalvalue"));
    crystalValue = parseInt(crystalValue);
    // We then add the crystalValue to the user's "counter" which is a global variable.
    // Every click, from every crystal adds to the global counter.
    counter += crystalValue;

    // All of the same game win-lose logic applies. So the rest remains unchanged.
    //alert("New score: " + counter);
    $("#score").text(counter);
       
    if (counter === targetNumber) {
      wins++;
      $("#wins").text(wins);
      counter=0;
      resetGame();
    }

    else if (counter >= targetNumber) {
      losses++;
      $("#losses").text(losses);
      counter=0;
      resetGame();
    }

# Author 
Zia Abbasi

# License
Standard MIT License
