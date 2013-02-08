# Auto Save Form script #

*Description:*  The most agonizing thing that can happen while filling out a form is accidently losing the entered contents before having a chance to submit it. This can happen if you inadvertently navigate to another page or close the window, among other things, during the process. Well, Auto Save Form script is here to add a layer of insurance against such a travesty from occurring. A nifty plug and play script, it periodically saves the contents of any form and recalls them if needed, up until when the form is actually submitted. This means if the user accidently leaves or reloads the page or even if the browser crashes (Firefox only feature) before then- the entered form contents will be restored.

The script uses HTML5's DOM storage and JSON to accomplish its mission. As such, it only works in modern browsers, from IE9+, FF3.5+, Safari/Chrome, to Opera 11. However, it degrades perfectly with the rest of the bunch, making this a nice progressive feature you can immediately add to your forms.

## Directions ##

*Step 1:* This script uses the following external files:

+ jQuery 1.6 or above (served via Google CDN)
+ autosaveform.js

*Step 2:* Add the below code to the HEAD section of your page:

	<style>
	
	div.savestatus{ /* Style for the "Saving Form Contents" DIV that is shown at the top of the form */
	width:200px;
	padding:2px 5px;
	border:1px solid gray;
	background:#fff6e5;
	-webkit-box-shadow: 0 0 8px #818181;
	box-shadow: 0 0 8px #818181;
	-moz-border-radius: 5px;
	-webkit-border-radius: 5px;
	border-radius:5px;
	color:red;
	position:absolute;
	top:-10px;
	}
	
	form#feedbackform div{ /*CSS used by demo form*/
	margin-bottom:9px;
	}
	
	</style>
	
	<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.6.2/jquery.min.js"></script>
	<script src="autosaveform.js">
	
	/***********************************************
	* Auto Save Form script (c) Dynamic Drive (www.dynamicdrive.com)
	* This notice MUST stay intact for legal use
	* Visit http://www.dynamicdrive.com/ for this script and 100s more.
	***********************************************/
	
	</script>
	
	<script>
	
	var formsave1=new autosaveform({
		formid: 'feedbackform',
		pause: 1000 //<--no comma following last option!
	})
	
	</script>


*Step 3:* Then, add the below sample markup to your page:

	<form id="feedbackform" method="post">
	
	<div>Name:<br /> <input id="username" type="text" size="35" /></div>
	
	<div>Sex: <input type="radio" name="sex" value="male" />Male <input type="radio" name="sex" value="female" />Female</div>
	
	<div>Hobbies: <input type="checkbox" name="hobby" />Reading <input type="checkbox" name="hobby" />Sports <input type="checkbox" name="hobby" />Movies</div>
	
	<div>Country: <select id="country">
		<option>USA</option>
		<option>Canada</option>
		<option>Other</option>
		</select>
	</div>
	
	<div>State/Province:<br /> <input id="state" type="text" size="20" /></div>
	
	<div>About Yourself:<br /> <textarea id="feedback" style="width:350px;height:150px"></textarea></div>
	
	<input type="submit" />
	
	</form>

## Auto Save Form script set up ##

See script project page for additional details on setup and documentation: <http://www.dynamicdrive.com/dynamicindex16/autosaveform.htm>
