# Using custom badges

Badges are often a convinent utility to track the status of a project and if you want to add a badge showing your last build's status, Shippable provides its own api for bagdes. The api always gives default badge which will say run is shippable in case your run was successful.

<img src="https://cloud.githubusercontent.com/assets/5207331/15181150/2b59af56-17a3-11e6-9c7f-87cefd972d2a.png" height="100"/>

This is something that you always not want. You may like to have a custom badge of your choice which will display the label and color that you want.
For example: You would like to display a badge for a specific branch with the branch name and its status in the badge itself.

<img src="https://cloud.githubusercontent.com/assets/5207331/15181191/6579542a-17a3-11e6-8818-6132ff28a73b.png"
height="100"/>

<img src="https://cloud.githubusercontent.com/assets/5207331/15181229/a5c83bb8-17a3-11e6-8dbc-faf5e2fbaba3.png"
height="100"/>

This is possible by using shields.io. Shields.io provides an api that will generate a badge with the text of your choice for a given projectId. You will need to pass the projectId and some query parameters to get your own badge.Here is how your url might look like.
```
https://img.shields.io/shippable/:projectId/:branch.svg?field1=value1&field2=value2&field3=value3
```

Image for projectId
> **Note**
> You can get the projectId from your project page on shippable..
> <img src="https://cloud.githubusercontent.com/assets/5207331/15181229/a5c83bb8-17a3-11e6-8dbc-faf5e2fbaba3.png"
height="100"/>

###### Following are the various fields that you can use to get your custom badge.
|    Field  		 	  |                Purpose                   |Default Value|
|---------------------|------------------------------------------|-------------|
|   label		      |       left text in badge                 | run         |
|  	colarA		 	  | left side color in badge  	        | ![#555555][555555]`   |
|   successLabel 	  | label when build is passing     		 | shippable   |
|   successColor 	  | color when build is passing     		 | ![#44CC11][44CC11]   |
|   failLabel		  | label when build is failing     		 | failing     |
|   failColor		  | color when build is failing     		 | ![#DC5F59][DC5F59]   |
|   cancelledLabel	  | label when build is cancelled   		 | cancelled   |
|   cancelledColor	  | color when build is cancelled   		 | ![#6BAFBD][6BAFBD]   |
|   unstableLabel	  | label when build is unstable     		 | unstable    |
|   unstableColor	  | color when build is unstable     		 | ![#CEA61B][CEA61B]   |
|   pendingLabel	  | label when build is pending     		 | pending     |
|   pendingColor	  | color when build is pending     		 | ![#5183A0][5183A0]   |
|   skippedLabel	  | label when build is skipped     		 | skipped     |
|   skippedColor	  | color when build is skipped     		 | ![#F8A97D][F8A97D]   |
|   noBuildLabel	  | label when there is no build    		 | none        |
|   noBuildColor	  | color when there is no build    		 | ![#A1ABAB][A1ABAB]   |
|   inaccessibleLabel | label when Shippable API is inaccessible | inaccessible|
|   inaccessibleColor | color when Shippable API is inaccessible | ![#A1ABAB][A1ABAB]   |


#### Below are some of the examples  

[run-shippable]:https://cloud.githubusercontent.com/assets/5207331/15181150/2b59af56-17a3-11e6-9c7f-87cefd972d2a.png
[build-passing]:https://cloud.githubusercontent.com/assets/5207331/15181191/6579542a-17a3-11e6-8818-6132ff28a73b.png
[prod-shippable]:https://cloud.githubusercontent.com/assets/5207331/15181229/a5c83bb8-17a3-11e6-8dbc-faf5e2fbaba3.png
[prod-shippable-color]:https://cloud.githubusercontent.com/assets/5207331/15181303/235dc1f6-17a4-11e6-8619-307a6190fc7b.png
<!-- http://localhost:8080/shippable/54ee15335ab6cc13528dd1ef.svg?label=production&successLabel=shippable&colorA=%23075E54&successColor=%23128C7E  -->
