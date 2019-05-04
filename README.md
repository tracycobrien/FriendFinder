# FriendFinder
# Friend Finder - Node and Express Servers

### Overview

In this activity, I'll build a compatibility-based "FriendFinder" application -- basically a dating app. This full-stack site will take in results from my surveys, then it will compare the answers with those from other users. The app will then display the name and picture of the user with the best overall match.

I will use Express to handle routing. I deployed the app to Heroku so other users can fill it out.

### Below are the links-

* I have submited both the deployed Heroku link to my homework AND the link to my Github Repository!

*  [Herouku Site ](https://friendfinder757.herokuapp.com/)

* [My Github](https://github.com/tracycobrien/FriendFinder.git)


### Instructions

1. My survey has 10 questions of about your personality and lifestyle choices. You should answer each one on a scale of 1 to 5 based on how much you agree or disagree with a question.

2. My`server.js` file requires the basic npm packages we've used in class: `express` and `path`.

3. My `htmlRoutes.js` file includes two routes:

   * A GET Route to `/survey` displays the survey page.
   * A default, catch-all route leads to `home.html` which displays the home page.

4. My `apiRoutes.js` file contains two routes:

   * A GET route with the url `/api/friends`. This is used to display a JSON of all possible friends.
   * A POST route `/api/friends`. This is used to handle incoming survey results. This route is also used to handle the compatibility logic.

5. I also saved my application's data inside of `app/data/friends.js` as an array of objects. Each of these objects look roughly follow the format below.

```json
{
  "name":"Ahmed",
  "photo":"https://media.licdn.com/mpr/mpr/shrinknp_400_400/p/6/005/064/1bd/3435aa3.jpg",
  "scores":[
      5,
      1,
      4,
      4,
      5,
      1,
      2,
      5,
      4,
      1
    ]
}
```

6. I determined the user's most compatible friends using the following as a guide:

   * I converted each user's results into a simple array of numbers (ex: `[5, 1, 4, 4, 5, 1, 2, 5, 4, 1]`).
   * With that done, I compared the difference between current user's scores against those from other users, question by question. Added up the differences to calculate the `totalDifference`.
     * Example:
       * User 1: `[5, 1, 4, 4, 5, 1, 2, 5, 4, 1]`
       * User 2: `[3, 2, 6, 4, 5, 1, 2, 5, 4, 1]`
       * Total Difference: **2 + 1 + 2 =** **_5_**

   * The closest match will be the user with the least amount of difference.

7. Once I found the current user's most compatible friend, it displays the results as a modal pop-up.
   * The modal should display both the name and picture of the closest match.




