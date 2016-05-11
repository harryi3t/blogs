# Using custom badges

Badges are often a convinent utility to track the status of a project. If you want to add a badge showing your last build's status, Shippable provides its own api for bagdes. The api always gives default badge which will say run is shippable in case your run was successful.

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
