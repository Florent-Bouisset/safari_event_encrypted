Description:
The event "encrypted" is not emitted from the video element when loading a HLS playlist with encrypted content.
This occurs when attaching mediaKeys to a video element with `videoElement.setMediaKeys(mediaKeys);` before setting
the video src with `videoElement.src = http://example.com/master.m3u8`

The file `event_encrypted_not_received.html` reproduce the issue.
Tne file `event_encrypted_received.html` is here to show that the event "encrypted" is emitted when the mediaKeys are not attached.

System Information:
Safari Version 17.2.1 (19617.1.17.11.12)
MacOS 14.2.1 (23C71)

Reproduction: 
Visit the page `event_encrypted_not_received.html`, observes that there is not log for the "encrypted" event.