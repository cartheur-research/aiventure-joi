## aiventure-joi

The david robot in a fun and engaging package. Clarity and purpose is the method and means. What about it?

* 1.30m tall, robust Robotis motors, high-strength plastic for weight and loss of _fear factor_
* Microphone, speakers, camera
* Three accelerometers for redudant walking stabilization
* AeonAI presence standard
	- Voice communication as conversation
	- Voice command as instructions
* Ideal controller standard
	- Self-learning
	- Self-programming
	- Self-adapting to dynamic events
* Animation training standard
	- No programing required
	- Learns by show
	- Refines animation automatically

### Operations

A test of the rebuild and assurance hardware is prepared for the intensive programming and training exericises ahead:

* AeonAI presence
* Ideal controller
	- Standing and walking
* Animation training
	- Data storage and entropy

![ops-check-2025](/images/ops-check.png)
_A shot from the perspective of joi_

### Printing

Collected in areas of the [form](/form/README.md).

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

Also create a file with the code at:

`/home/.config/alsa/asoundrc`

### Asynchronous behavior

Missing from the arm32 codebase, but in the huggable stack. DONE

### Bash shell generalization

Also missing. Will need huggable code. DONE

### Simulating positions

Start with [this](https://docs.poppy-project.org/en/installation/install-vrep.html). But have found this is a waste of time.

### About

![369](/images/joi-369.png)