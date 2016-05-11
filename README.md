# Using custom badges

Badges are often a convinent utility to track the status of a project and if you want to add a badge showing your last build's status, Shippable provides its own api for bagdes. The api always gives default badge which will say run is shippable in case your run was successful.

<img src="https://cloud.githubusercontent.com/assets/5207331/15181150/2b59af56-17a3-11e6-9c7f-87cefd972d2a.png" height="100"/>

This is something that you always not want. You may like to have a custom badge of your choice which will display the label and color that you want.
For example: You would like to display a badge for a specific branch with the branch name and its status in the badge itself.

<img src="https://cloud.githubusercontent.com/assets/5207331/15181191/6579542a-17a3-11e6-8818-6132ff28a73b.png"
height="100"/>

<img src="https://cloud.githubusercontent.com/assets/5207331/15181229/a5c83bb8-17a3-11e6-8dbc-faf5e2fbaba3.png"
height="100"/>

This is possible by using shields.io. Shields.io provides an api that will generate a badge with the text of your choice for a given projectId. You will need to pass the projectId and some query parameters to get your own badge. Here is how your url might look like.
https://img.shields.io/shippable/:projectId/:branch.svg?field1=value1&field2=value2&field3=value3

Note: You can get the projectId from your project page on shippable.
Image for projectId


### Scenarios
| No |                                    Requirement                            |
|-----|-----------------------------------------------------------------------|
| 1   |     successLabel | 
| 2   |     successColor |
| 3   |     failLabel    |
| 4   |     failColor    | 
| 5   |     cancelledLabel |
| 6   |     cancelledColor |
| 7   |     unstableLabel | 
| 8   |     unstableColor |
| 9   |     pendingLabel |
| 10   |    pendingColor | 
| 11  |     skippedLabel |
| 12  |     skippedColor |
| 13  |     noBuildLabel | 
| 14  |     noBuildColor |
| 15  |     inaccessibleLabel |
| 16|       inaccessibleColor | 


#### Below are some of the examples  

[run-shippable]:https://cloud.githubusercontent.com/assets/5207331/15181150/2b59af56-17a3-11e6-9c7f-87cefd972d2a.png
[build-passing]:https://cloud.githubusercontent.com/assets/5207331/15181191/6579542a-17a3-11e6-8818-6132ff28a73b.png
[prod-shippable]:https://cloud.githubusercontent.com/assets/5207331/15181229/a5c83bb8-17a3-11e6-8dbc-faf5e2fbaba3.png
[prod-shippable-color]:https://cloud.githubusercontent.com/assets/5207331/15181303/235dc1f6-17a4-11e6-8619-307a6190fc7b.png
<!-- http://localhost:8080/shippable/54ee15335ab6cc13528dd1ef.svg?label=production&successLabel=shippable&colorA=%23075E54&successColor=%23128C7E  -->
