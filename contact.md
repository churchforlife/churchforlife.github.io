---
layout: default
title: Contact
navId: 60
---

## Contact Us

<div id="contactContainer">
	<ul class="contactList">
		<li><h3>Services</h3></li>
		<li><div class="contactItem"><div><i class="fa fa-clock-o contact-icons" aria-hidden="false"></i></div><div><p>Sundays, 10:00am</p></div></div></li>
		<li><div class="contactItem"><div><i class="fa fa-map-signs contact-icons" aria-hidden="false"></i></div><div><p>19 Kilvington Drive, Emerald, VIC</p></div></div></li>
	</ul>

	<ul class="contactList">
		<li><h3>Pastor Mal Doswell</h3></li>
		<li><div class="contactItem"><div><i class="fa fa-phone contact-icons" aria-hidden="false"></i></div><div><p>0425 777 462</p></div></div></li>
		<li><div class="contactItem"><div><i class="fa fa-envelope contact-icons" aria-hidden="false"></i></div><div><p>psmaldoswell@churchforlife.com.au</p></div></div></li>
	</ul>

	<ul class="contactList">
		<li><h3>Church Office</h3></li>
		<li><div class="contactItem"><div><i class="fa fa-phone contact-icons" aria-hidden="false"></i></div><div><p>PHONE NUMBER</p></div></div></li>
		<li><div class="contactItem"><div><i class="fa fa-envelope contact-icons" aria-hidden="false"></i></div><div><p>Church For Life PO Box 307, Emerald, Victoria, 3782</p></div></div></li>
		<li><div class="contactItem"><div><i class="fa fa-envelope contact-icons" aria-hidden="false"></i></div><div><p>inquiries@churchforlife.com.au</p></div></div></li>
	</ul>
</div> <!-- /contactContainer -->


### Location

<div id="map-canvas"></div>

<script src="https://maps.googleapis.com/maps/api/js?v=3.exp"></script>

<script>
	var markers = {{ site.data.location | jsonify }};
	function initializeMap() {
		var bounds = new google.maps.LatLngBounds(),
			mapOptions = {
				mapTypeId: 'roadmap',
				styles: [{"featureType":"water","elementType":"geometry","stylers":[{"visibility":"on"},{"color":"#aee2e0"}]},{"featureType":"landscape","elementType":"geometry.fill","stylers":[{"color":"#abce83"}]},{"featureType":"poi","elementType":"geometry.fill","stylers":[{"color":"#769E72"}]},{"featureType":"poi","elementType":"labels.text.fill","stylers":[{"color":"#083705"}]},{"featureType":"poi","elementType":"labels.text.stroke","stylers":[{"color":"#ffffff"}]},{"featureType":"poi.park","elementType":"geometry","stylers":[{"visibility":"on"},{"color":"#8dab68"}]},{"featureType":"road","elementType":"geometry.fill","stylers":[{"visibility":"on"}]},{"featureType":"road","elementType":"labels.text.fill","stylers":[{"color":"#083705"}]},{"featureType":"road","elementType":"labels.text.stroke","stylers":[{"color":"#ffffff"}]},{"featureType":"road","elementType":"labels.icon","stylers":[{"visibility":"off"}]},{"featureType":"road.local","elementType":"geometry","stylers":[{"color":"#dddddd"}]},{"featureType":"road.arterial","elementType":"geometry","stylers":[{"color":"#aaaaaa"}]},{"featureType":"road.highway","elementType":"geometry","stylers":[{"color":"#888888"}]},{"featureType":"transit","stylers":[{"visibility":"on"}]},{"featureType":"administrative","elementType":"geometry.stroke","stylers":[{"visibility":"on"},{"color":"#87ae79"}]},{"featureType":"administrative","elementType":"geometry.fill","stylers":[{"color":"#7f2200"},{"visibility":"off"}]},{"featureType":"administrative","elementType":"labels.text.stroke","stylers":[{"color":"#ffffff"},{"visibility":"on"},{"weight":4.1}]},{"featureType":"administrative","elementType":"labels.text.fill","stylers":[{"color":"#495421"}]},{"featureType":"administrative.neighborhood","elementType":"labels","stylers":[{"visibility":"off"}]}]
			};
		// Display a map on the page
		var map = new google.maps.Map(document.getElementById("map-canvas"), mapOptions);
		map.setTilt(45);

		var position = new google.maps.LatLng(markers[0].latitude, markers[0].longitude);
		bounds.extend(position);

		marker = new google.maps.Marker({
			position: position,
			map: map,
			title: markers[0].title
		});

		// Automatically center the map fitting all markers on the screen
		map.fitBounds(bounds);
		// Override map zoom level once fitBounds function runs (Make sure it only runs once)
		var boundsListener = google.maps.event.addListener((map), 'bounds_changed', function(event) {
			this.setZoom(17);
			google.maps.event.removeListener(boundsListener);
		});
	}
	google.maps.event.addDomListener(window, 'load', initializeMap);
</script>
