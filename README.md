# Speedcubing Score Leaderboard
The aim of this little project is to provide a convenient way to project the live results of a speedcubing competition onto a screen.
The entering of the scores is done through a file called `scores.json`. The only requirement of the app is that is must be placed on any web server.
# `scores.json` Syntax
The syntax of the file is self-explanatory once you open it. Here are some of the more complex properties, which may require explanation:
* `showNow` and `showNowText`: if `showNow` is set to `true`, `showNowText` is displayed instead of the scores table; you can use any sort of HTML in `showNowText`
* `Qplaces` and `Qcolors`: `Qplaces` determines the place the contesants need to reach to be above a qualification line. `Qcolors` specifies the colors of those lines. To disable the lines, set `Qplaces` to `[]`
* `bestColor` and `bestTextColor`: they determine the background color and text color of the best score in a round
* `isFinalRound`: if it's `true`, the minimum and maximum scores are discarded when calculating the sum
* `leaveOnlyFirst`: leave only the first N scores when saving the sorted `scores.json` (to save, press the `I` key)
# Auto-refresh
The webpage automatically scrolls down by 100 pixels every 5 seconds. Once it reaches the bottom, it goes back to the top and the data is automatically refreshed. You can force a refresh by pressing the `F` key.
