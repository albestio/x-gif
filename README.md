# &lt;x-gif&gt;

_The GIF tag the internet deserves_

## Usage

**&lt;x-gif&gt;** is a web component for flexible GIF playback. Because GIFs are cool, and it's fun to mess around with them. Right now it's only defined as a Polymer element, but wrappers for other popular component frameworks are coming.

```html
<x-gif src="probably_cats.gif"></x-gif>
```

This does the following:

* AJAX fetches the GIF as a binary stream
* Slices the GIF into frames like a total boss
* Stacks the frames one on top of the other
* Starts a `requestAnimationFrame` loop to play back the gif at its natural frame rate

**[Here's a demo! It just might work in your browser!](http://geelen.github.io/x-gif)**

## Options

### Speed

Spins through the frames at its natural rate multiplied by `speed`

```html
<x-gif src="definitely_cats.gif" speed="2.1"></x-gif>
```

### Bpm

Breaks the GIF across 1 or more _beats_ (depending on how long the GIF is), where each beat is 1/`bpm` minutes long.

```html
<x-gif src="something_dumb_from_buzzfeed.gif" bpm="120"></x-gif>
```

### Hard-bpm

Just like `bpm` but locks all GIFs to one _beat_, regardless of how long they were originally.

```html
<x-gif src="something_dumb_from_buzzfeed.gif" hard-bpm="120"></x-gif>
```

### Stopped

```html
<x-gif src="something_rad_off_reddit.gif" stopped></x-gif>
```

Stops the `requestAnimationFrame` loop inside the GIF. You can add or remove the `stopped` attribute and it will stop or start. Obvs.
```

### Sync

```html
<x-gif src="mr_t_works_it.gif" sync></x-gif>
```

Defers playback to an external clock, such as beat data from an audio stream to make rad synchronised GIFs & music. [See an example](http://geelen.github.io/x-gif/demos/audio.html).

**[Check out the rest of the demos](http://geelen.github.io/x-gif)**

## Status

* **Polymer element - DONE!**
* Angular directive - TODO
* React component - TODO
* Ember component - TODO
