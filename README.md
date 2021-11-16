
<!DOCTYPE html>
<html>
<head>

<title>Cookie Clicker</title>
<!--
Code and graphics copyright Orteil, 2013-2019
Feel free to alter this code to your liking, but please do not re-host it, do not profit from it and do not present it as your own.
-->

<meta name="viewport" content="width=900, initial-scale=1">
<link rel="shortcut icon" href="https://cdn.jsdelivr.net/gh/BinBashBanana/gstore/html5games/cookieclicker/img/favicon.ico" />
<!--<link href="https://fonts.googleapis.com/css?family=Kavoon&subset=latin,latin-ext" rel="stylesheet" type="text/css">-->
<link href='https://fonts.googleapis.com/css?family=Merriweather:900&subset=latin,latin-ext' rel='stylesheet' type='text/css'>
<script src="https://cdn.jsdelivr.net/gh/BinBashBanana/gstore/html5games/cookieclicker/showads.js"></script><!-- this just detects adblockers so we can adjust the layout and play nice -->
<script src="https://cdn.jsdelivr.net/gh/BinBashBanana/gstore/html5games/cookieclicker/base64.js"></script>
<script src="https://cdn.jsdelivr.net/gh/BinBashBanana/gstore/html5games/cookieclicker/main.js?v=2.061"></script>
<link href="https://cdn.jsdelivr.net/gh/BinBashBanana/gstore/html5games/cookieclicker/style.css?v=2.050" rel="stylesheet" type="text/css">
<!--[if IE]>
<style type="text/css">
	#ifIE9{display:block;}
</style>
<![endif]-->

<!--[if lt IE9]><script src="https://cdn.jsdelivr.net/gh/BinBashBanana/gstore/html5games/cookieclicker/excanvas.compiled.js"></script><![endif]-->

</head>
<body>

<div id="wrapper">

	<div id="topBar" style="display:none">
		<div><b>Cookie Clicker</b>&trade; &copy; <a href="http://orteil.dashnet.org" target="_blank" id="topbarOrteil">Orteil</a>, 2019 - <a href="http://dashnet.org" target="_blank" id="topbarDashnet">DashNet</a></div>
		<div><a href="http://twitter.com/orteil42" target="_blank" id="topbarTwitter">twitter</a></div>
		<div><a href="http://orteil42.tumblr.com" target="_blank" id="topbarTumblr">tumblr</a></div>
		<!--<div><a href="http://forum.dashnet.org" target="_blank">Official forum</a></div>-->
		<div style="position:relative;"><div style="width:22px;height:32px;background:url(https://cdn.jsdelivr.net/gh/BinBashBanana/gstore/html5games/cookieclicker/img/discord.png);position:absolute;left:0px;top:0px;pointer-events:none;"></div><a href="https://discordapp.com/invite/cookie" target="_blank" style="padding-left:16px;" id="topbarDiscord">Discord</a></div>
		<div style="position:relative;"><div style="width:25px;height:32px;background:url(https://cdn.jsdelivr.net/gh/BinBashBanana/gstore/html5games/cookieclicker/img/weeHoodie.png);position:absolute;left:-2px;top:0px;pointer-events:none;"></div><a class="blueLink" href="http://www.redbubble.com/people/dashnet" target="_blank" style="padding-left:12px;" id="topbarMerch">Merch!</a></div>
		<div style="position:relative;"><div style="width:22px;height:32px;background:url(https://cdn.jsdelivr.net/gh/BinBashBanana/gstore/html5games/cookieclicker/img/patreon.png);position:absolute;left:0px;top:0px;pointer-events:none;"></div><a class="orangeLink" href="https://www.patreon.com/dashnet" target="_blank" style="padding-left:16px;" id="topbarPatreon">Patreon</a></div>
		<div style="position:relative;display:none;font-weight:bold;" id="heralds"><div style="position:absolute;top:-4px;width:31px;height:39px;background:url(img/heraldFlag.png);left:50%;margin-left:-15px;pointer-events:none;"></div><div id="heraldsAmount" style="position:relative;z-index:10;text-shadow:0px 1px 0px #000,0px 0px 6px #ff00e4;color:#fff;">-</div></div>
		<div><a class="lightblueLink" style="font-weight:bold;" href="https://play.google.com/store/apps/details?id=org.dashnet.cookieclicker" target="_blank" id="topbarMobileCC">Cookie Clicker for Android</a></div>
		<div><a href="http://orteil.dashnet.org/randomgen/" target="_blank" id="topbarRandomgen">RandomGen</a></div>
		<div><a href="http://orteil.dashnet.org/igm/" target="_blank" id="topbarIGM">Idle Game Maker</a></div>
		<div id="links" class="hoverer">
			Other versions
			<div class="hoverable">
			<a href="../" target="_blank" id="linkVersionLive">Live version</a>
			<a href="beta" target="_blank" id="linkVersionBeta">Try the beta!</a>
			<a href="http://orteil.dashnet.org/cookieclicker/v10466" target="_blank" id="linkVersionOld">v. 1.0466</a>
			<a href="http://orteil.dashnet.org/experiments/cookie/" target="_blank">Classic</a>
			</div>
		</div>
	</div>

	<div id="game">
		<div id="javascriptError">
			<div id="loader">
				<div class="spinnyBig"></div>
				<div class="spinnySmall"></div>
				<div id="loading" class="title">Loading...</div>
				<div id="failedToLoad" class="title">This is taking longer than expected.<br>
				<div style="font-size:65%;line-height:120%;">Slow connection? If not, please make sure your javascript is enabled, then refresh.<br>
				If problems persist, this might be on our side - wait a few minutes, then hit ctrl+f5!</div></div>
				<div id="ifIE9" class="title" style="font-size:100%;line-height:120%;">Your browser may not be recent enough to run Cookie Clicker.<br>You might want to update, or switch to a more modern browser such as Chrome or Firefox.</div>
				<!--<div class="title">Oops, looks like we've got a problem.</div>
				<div>Please bear with us while we fix it.<br>Your save is safe, don't worry!</div>-->
			</div>
		</div>

		<canvas id="backgroundCanvas"></canvas>
		
		<div id="goldenCookie" class="goldenCookie"></div>
		<div id="seasonPopup" class="seasonPopup"></div>
		<div id="shimmers"></div>
		<div id="alert"></div>
		<div id="particles"></div>
		<div id="sparkles" class="sparkles"></div>
		<div id="notes"></div>
		<div id="darken"></div>
		<div id="toggleBox" class="framed prompt"></div>
		<div id="promptAnchor"><div id="prompt" class="framed"><div id="promptContent"></div><div class="close" onclick="PlaySound('snd/tick.mp3');Game.ClosePrompt();">x</div></div></div>
		<div id="versionNumber" class="title"></div>
		<div id="ascend">
			<div id="ascendBG"></div>
			<div id="ascendZoomable"><div id="ascendContent"><div id="ascendUpgrades" style="position:absolute;"></div></div></div>
			<div id="ascendOverlay"></div>
		</div>
		
		<div id="debug"><div id="devConsole" class="framed"></div><div id="debugLog"></div></div>
		
		<div id="sectionLeft" class="inset">
			<canvas id="backgroundLeftCanvas" style="z-index:5;"></canvas>
			<div class="blackFiller"></div>
			<div class="blackGradient"></div>
			<div id="sectionLeftInfo"></div>
			<div id="cookies" class="title"></div>
			<div id="bakeryNameAnchor"><div id="bakeryName" class="title"></div></div>
			<div id="specialPopup" class="framed prompt offScreen"></div>
			<div id="buffs" class="crateBox"></div>
			<div id="cookieAnchor">
				<div id="bigCookie"></div>
				<div id="cookieNumbers"></div>
			</div>
			<div id="sectionLeftExtra"></div>
		</div>

		<div class="separatorLeft"></div>
		<div class="separatorRight"></div>

		<div id="sectionMiddle" class="inset">
			<div id="comments" class="inset title">
				<div id="prefsButton" class="button">Options</div>
				<div id="statsButton" class="button">Stats</div>
				<div id="logButton" class="button"><div id="checkForUpdate">New update!</div>Info</div>
				<div id="legacyButton" class="button">Legacy<div id="ascendMeterContainer" class="smallFramed meterContainer"><div id="ascendMeter" class="meter filling"></div></div><div class="roundedPanel" id="ascendNumber"></div><div id="ascendTooltip" class="framed"></div></div>
				<div id="commentsTextBelow" class="commentsText"></div>
				<div id="commentsText" class="commentsText"></div>
				<div class="separatorBottom"></div>
			</div>
			<div id="centerArea">
				<div id="buildingsTitle" class="inset title zoneTitle">Buildings</div>
				<div id="buildingsMaster"></div>
				<div id="rows"></div>
				<div id="menu"></div>
				<!--
				<div id="donateBox">
					<form target="_blank" action="https://www.paypal.com/cgi-bin/webscr" method="post" id="donate" style="margin:0px 16px;">
					<input type="hidden" name="cmd" value="_s-xclick">
					<input type="hidden" name="hosted_button_id" value="BBN2WL3TC6QH4">
					<input type="image" src="https://www.paypalobjects.com/en_GB/i/btn/btn_donate_LG.gif" border="0" name="submit" alt="PayPal — The safer, easier way to pay online.">
					<img alt="" border="0" src="https://www.paypalobjects.com/nl_NL/i/scr/pixel.gif" width="1" height="1">
					</form>
					<small>Help us keep developing the game!</small>
				</div>
				-->
			</div>
		</div>

		<div id="sectionRight" class="inset">
			<div id="store">
				<div id="storeTitle" class="inset title zoneTitle">Store</div>
				<div id="toggleUpgrades" class="storeSection upgradeBox"></div>
				<div id="techUpgrades" class="storeSection upgradeBox"></div>
				<div id="vaultUpgrades" class="storeSection upgradeBox"></div>
				<div id="upgrades" class="storeSection upgradeBox"></div>
				<div id="products" class="storeSection"></div>
			</div>
			
		</div>
		
		<div id="focusButtons">
			<div id="focusLeft" class="title">Cookie</div>
			<div id="focusMiddle" class="title" style="font-size:80%;padding-top:18px;padding-bottom:14px;">Buildings</div>
			<div id="focusRight" class="title">Store</div>
			<div id="focusMenu" class="title">Menu</div>
		</div>
		<div id="compactOverlay" class="title">
			<div id="compactCommentsText" class="commentsText"></div>
			<div id="compactCookies"></div>
			<div class="separatorBottom"></div>
		</div>
		
		<div id="tooltipAnchor"><div id="tooltip" class="framed" onMouseOut="Game.tooltip.hide();"></div></div>

	</div>

</div>

</body>
</html>
