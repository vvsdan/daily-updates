### daily-updates

This repo/README file is meant to serve as a journey for documenting work I do daily, problems solved, tasks completed, or challenges faced in my learning. 

# 1 Jan 2024 

In the comfy store project, there was a NaN error being produced when adding items to the cart. In the web application, the error appeared in the Navbar Cart icon which was to indicate the number of items in the cart. The same error carried over for other dynamic values such as in the checkout page, when calculating the shipping totals (everything produced NaN except the static shipping price). 
Initially, I thought this error was in the store.js file OR the cartSlice.js file where state values were stored, or being incremented, edited, etc. 
Solution: In App.jsx the path for "Orders" was incorrect
<img src='https://dj-project-previews.s3.amazonaws.com/updates/Screenshot+2024-01-02+121816.png'>
-------------------------------------------------------------------------------
# 2 Jan 2024
