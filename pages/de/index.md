---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth: header_001.jpg
widget1:
  title: "Natur 4.0 im Überblick"
  url: '/de/ueber/zusammenfassung'
  image: widget_header_003.jpg
  text: 'Flächendeckendes Naturschutzmonitoring durch vernetzte Sensorik als Grundlage für einen nachhaltigen Artenschutz und die Sicherung von Ökosystemfunktionen.'
widget2:
  title: "Das Team von Natur 4.0"
  url: '/de/ueber/team'
  text: 'Vernetztes Naturschutzmonitoring erfordert ein vernetztes Team im Querschnittsverbund aus Wissenschaft, Praxis und Bildung.'
  image: widget_team.jpg
widget3:
  title: "Kontakt"
  url: '/de/praxis/fragen'
  image: widget_questions.jpg
  text: 'Waldspaziergang mit Roboter? Hier finden Sie Antworten auf allgemeine Fragen und Kontaktinformationen.'
#
# Use the call for action to show a button on the frontpage
#
# To make internal links, just use a permalink like this
# url: /getting-started/
#
# To style the button in different colors, use no value
# to use the main color or success, alert or secondary.
# To change colors see sass/_01_settings_colors.scss
#
# callforaction:
#  url: https://tinyletter.com/feeling-responsive
#  text: Inform me about new updates and features ›
#  style: alert
permalink: /index.html
#
# This is a nasty hack to make the navigation highlight
# this page as active in the topbar navigation
#
homepage: true
---

<p id="twitter-target"><button onclick="setShowTwitter()">Ich bin damit einverstanden, dass mir Inhalte von Twitter angezeigt werden.</button></p>

<script type="text/javascript">

function setShowTwitter() {
  docCookies.setItem("show-twitter", "true");
  showTwitter();
}

function showTwitter() {
  var tag_a = document.createElement("a");
  tag_a.className = "twitter-timeline";
  tag_a.href = "https://twitter.com/Nature40Lab?ref_src=twsrc%5Etfw";
  tag_a.innerHTML = "Tweets";
  var tag_script = document.createElement("script");
  tag_script.async = true;
  tag_script.src = "https://platform.twitter.com/widgets.js";
  tag_script.charset = "utf-8";

  tag_target = document.getElementById("twitter-target");
  tag_target.innerHTML = "";
  tag_target.appendChild(tag_a);
  tag_target.appendChild(tag_script);
}

function init() {
  var cooky = docCookies.getItem("show-twitter");
  if(cooky === 'true') {
    showTwitter();
  }
}

document.addEventListener('DOMContentLoaded', function() {init();}, false);

</script>



<div id="videoModal" class="reveal-modal large" data-reveal="">
  <div class="flex-video widescreen vimeo" style="display: block;">
    <iframe width="1280" height="720" src="https://www.youtube.com/embed/3b5zCFSmVvU" frameborder="0" allowfullscreen></iframe>
  </div>
  <a class="close-reveal-modal">&#215;</a>
</div>
