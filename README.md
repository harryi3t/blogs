# Using custom badges

Badges are often a convinent utility to track the status of a project. If you want to add a badge showing your last build's status, Shippable provides its own api for bagdes. The api always gives default badge which will say run is shippable in case your run was successful.

<img src="https://cloud.githubusercontent.com/assets/5207331/15181150/2b59af56-17a3-11e6-9c7f-87cefd972d2a.png" height="100" width="100"/>
- Default shippable badge image

This is something that you won't always want. It is also possible that you would like to have a custom badge of your choice which will display the label and color that you want.
For example: You would like to display a badge for a specific branch with the branch name in the badge itself as shown below.

- build passing
- master passing
- dev shippable

This is possible by using shields.io. Shields.io provides an api that will generate a badge with the text of your choice for a given projectId. You will need to pass the projectId and some query parameters. Here is how your url might look like.
https://img.shields.io/shippable/:projectId/:branch.svg?field1=value1&field2=value2&field3=value3

Note: You can get the projectId from your project page on shippable.
Image for projectId

Following are the various fields that you can use to get your custom badge.
  - successLabel
  - successColor
  - failLabel
  - failColor
  - cancelledLabel
  - cancelledColor
  - unstableLabel
  - unstableColor
  - pendingLabel
  - pendingColor
  - skippedLabel
  - skippedColor
  - noBuildLabel
  - noBuildColor
  - inaccessibleLabel
  - inaccessibleColor

Examples here

[run-shippable]:https://cloud.githubusercontent.com/assets/5207331/15181150/2b59af56-17a3-11e6-9c7f-87cefd972d2a.png
[build-passing]:https://cloud.githubusercontent.com/assets/5207331/15181191/6579542a-17a3-11e6-8818-6132ff28a73b.png
[prod-shippable]:https://cloud.githubusercontent.com/assets/5207331/15181229/a5c83bb8-17a3-11e6-8dbc-faf5e2fbaba3.png
[prod-shippable-color]:https://cloud.githubusercontent.com/assets/5207331/15181303/235dc1f6-17a4-11e6-8619-307a6190fc7b.png
<!-- http://localhost:8080/shippable/54ee15335ab6cc13528dd1ef.svg?label=production&successLabel=shippable&colorA=%23075E54&successColor=%23128C7E  -->
