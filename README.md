## aiventure-joi

The david robot in a fun and engaging package. Clarity and purpose is the method and means.

### USB sound card

When using the miniature black-case USB sound card, create a file:

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

This was already in-place, the problem was that `aplay` was only for `root`, so:

`sudo usermod --append --groups audio cartheur`

And a reboot solved the issue.

### Asynchronous behavior

Missing from the arm32 codebase, but in the huggable stack.

### Bash shell generalization

Also missing. Will need huggable code.
