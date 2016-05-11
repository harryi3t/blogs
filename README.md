# Using custom badges

Badges are often a convinent utility to track the status of a project. If you want to add a badge showing your last builds status Shippable provides its own api for bagdes. The api always gives default bagde which will say run is shippable in case your run is succesfull.

- Default shippable badge image

This is something that you will always not want. It is also possible to have a custom badge of your choice which will display the text you want. For example: If you want to display badge for specific branch with the branch name and indicate that the build is passing.

- build passing
- master passing
- dev shippable

This is possible by using shields.io. Shields.io provides an api that will generate a badge with the text your choice for a given run. You will need to pass the runid and your text as query parameters.Here is how your url might look like.
https://img.shields.io/shippable/runId/branch.svg?field1=value1&field2=value2&field3=value3

Note: You can get the run if from your runs page on shippable.
Image for runId

Following are the various fields that you can use to get your custom badge.
  - successLabel
  - uccessColor
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
