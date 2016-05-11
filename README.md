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

[2]:https://cloud.githubusercontent.com/assets/5207331/14247587/c1458ae6-fa8c-11e5-8324-f8507c144b32.png
[3]:https://cloud.githubusercontent.com/assets/5207331/14247750/ebdc027a-fa8d-11e5-8323-1819b47f2848.png
[4]:https://github.com/badges/shields/blob/master/server.js#L392
[5]:https://cloud.githubusercontent.com/assets/5207331/15105888/008a8320-15e3-11e6-9eb4-5911e4c67c2b.png
[6]:https://cloud.githubusercontent.com/assets/5207331/15106842/852c6e6c-15e9-11e6-8232-06e465b55383.png
[7]:https://cloud.githubusercontent.com/assets/5207331/15137396/43944b78-16a7-11e6-8284-e2d17900f001.png
[8]:https://github.com/Shippable/heap/issues/63#issuecomment-218074042
[9]:https://cloud.githubusercontent.com/assets/5207331/15137876/da359918-16a9-11e6-8bc7-ca9aceb9cc8a.png
[44CC11]:https://cloud.githubusercontent.com/assets/5207331/15141458/ae3a99da-16bd-11e6-9132-bb46875d3fe7.png
[555555]:https://cloud.githubusercontent.com/assets/5207331/15141509/f8db5d12-16bd-11e6-8e84-8498ef69a596.png
[DC5F59]:https://cloud.githubusercontent.com/assets/5207331/15141552/3741edf0-16be-11e6-8922-9ae46d633f75.png
[6BAFBD]:https://cloud.githubusercontent.com/assets/5207331/15141560/4014c042-16be-11e6-8374-b62914126ba4.png
[CEA61B]:https://cloud.githubusercontent.com/assets/5207331/15141568/48feaec0-16be-11e6-84fb-b48a66a783d6.png
[5183A0]:https://cloud.githubusercontent.com/assets/5207331/15141575/4f9862f8-16be-11e6-83a8-aa9b0ec4f392.png
[F8A97D]:https://cloud.githubusercontent.com/assets/5207331/15141580/56aa568c-16be-11e6-84f5-0ea50f374fa0.png
[A1ABAB]:https://cloud.githubusercontent.com/assets/5207331/15141586/5bc93dc2-16be-11e6-8d53-ea3c434cb58b.png
