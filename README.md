# Untangle SSL Inspector Ignore Rules to allow cetain Apps and Services to function.
Be sure to place these rules high on the list in order for them to work properly.

The best way I have found to isolate what domains to use in the rule is to have two tabs opened, one on `Reports -> Web Filter -> All Web Events` and the other on `Reports -> SSL Inspector -> All Sessions` and to add the hostname of the device in question to the filter. Then close and open the app/service/website in question and refresh those tabs to see what domains are getting requested. Then build your rule out from there, adding and removing to determine the bare minimum until the service starts to work.

## Facebook & Messenger App
|Type||Value|
|--|--|--|
|SNI Hostname|is|`*.fbcdn.net,edge-mqtt.facebook.com,rupload.facebook.com,graph.facebook.com,lookaside.facebook.com,m.facebook.com`|
|Certificate Subject|is|`*Facebook*`

## Google Chrome OS / Devices
|Type||Value|
|--|--|--|
|SNI Hostname|is|`*.1e100.net,accounts.google.com,accounts.youtube.com,clients1.google.com,clients2.google.com,clients3.google.com,clients4.google.com,clients2.googleusercontent.com,cros-omahaproxy.appspot.com,dl.google.com,dl-ssl.google.com,*.gvt1.com,gweb-gettingstartedguide.appspot.com,m.google.com,omahaproxy.appspot.com,pack.google.com,policies.google.com,safebrowsing-cache.google.com,safebrowsing.google.com,tools.google.com,chrome.google.com,mtalk.google.com,connectivitycheck.android.com,play.google.com,android.com,google-analytics.com,googleusercontent.com,*.gstatic.com,*.ggpht.com android.clients.google.com,*.gvt2.com,*.gvt3.com,*.googleapis.com,pki.google.com,clients5.google.com,clients6.google.com`|
|Certificate Subject|is|`*Google*`

## Instagram
|Type||Value|
|--|--|--|
|SNI Hostname|is|`*.cdninstagram.com,i.instagram.com`|

## Nest
|Type||Value|
|--|--|--|
|SNI Hostname|is|`*.nest.com`|

## OwletCam
|Type||Value|
|--|--|--|
|SNI Hostname|is|`*.firebaseio.com`|


