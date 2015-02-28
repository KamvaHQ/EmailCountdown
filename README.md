#EmailCountdown
==============


**What does this do?**

Creates a countdown image counting down to a specific time/date for use in email campaigns.

##How does it work?

This generates an image based on the following variables:

```php
  $image = imagecreatefrompng('images/countdown.png');
	$font = array(
		'size'=>81, // Font size, in pts usually.
		'angle'=>0, // Angle of the text
		'x-offset'=>45, // The larger the number the further the distance from the left hand side, 0 to align to the left.
		'y-offset'=>98, // The vertical alignment, trial and error between 20 and 60.
		'file'=>'./BRoya.ttf', // Font path
		'color'=>imagecolorallocate($image, 254, 152, 6), // RGB Colour of the text
	);
```


##How to use it?
You can add an image to your newsletter with ?time= query. for example, example.com/gif.php?time=tomorrow will generate a live gif countdown to tomorrow. time query could be any [strtotime](http://php.net/manual/en/function.strtotime.php) value.
![Time to next monday](http://niloofarestakhri.com/lab/gif.php?time=next%20monday)