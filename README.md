## aiventure-joi

The david robot in a fun and engaging package. Clarity and purpose is the method and means.

### USB sound card

When using the USB sound card, create a file:

`sudo nano /etc/asound.conf`

With the following code:
```
pcm.!default {
	type plug
	slave {
		pcm "hw:1,0"
	}
}

ctl.!default {
	type hw
	card 1
}
```
Then run the first time:

`aplay -v speech.wav`
