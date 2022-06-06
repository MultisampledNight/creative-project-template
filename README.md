# Template for creative non-code projects

I use Blender. Actually I use Blender quite often. And not only Blender, but
also GIMP, Inkscape and LMMS, making random Vim colorschemes, too. It turns out
that even though all those are "creative" applications, my project structure for
each one is different. So here I define one possible structure for use in
non-code projects, to finally bring consistency into my own projects.

## Terms

- "Revisions" increase anytime a rebuild/redesign happens, or so large changes
	happen that the original design or work becomes irrelevant. They _never_
	reset and should be consistent _everywhere._ They're in the format `rXXX`, so
	`r001` for the first (and really first, there's no "zeroth") revision.
- "Versions" increase anytime the artist thinks the current state of the artwork
  should be preserved. They should be consistent in their category, and higher
	versions should come after lower ones chronologically. They're in the format
	`vXXX` with `v001` being the first version.

## Structure

- `exports`
	Contains all exports to a game engine, other people or whatever you want
	to show the outer world outside of your "environment". Actual contents are
	first contained by revision + version number folders, like `r001-v001`. The
	version number is independent from the main source file versioning and
	increases only on new exports, the revision, however, should stay in sync with
	the source. Ideally every export folder also contains notes on what the export
	is supposed to do and which version in `source` it corresponds to.

- `notes`
	Everything you want to keep track of for later on, or just write down
	thoughts. Can reach from short todo lists to long character documents.

- `resources`
	Put everything, really everything you find about your project here. Whether
	it's just a picture of your cat if you want to make an extraterrestial animal,
	detailed concept art created by your lovely concept artists or just audio
	samples, it all belongs here. Basically `notes` but extended to
	non-textual/reference content.

- `render`
	Keep your `source` folder clean and put any conversions from that folder here.
	A "render" can be anything as a real costly render of a 3D model, a
	rasterization of an SVG to a PNG, or your converted audio.

- `source`
	The actual source files you're working on. In Blender `.blend` files, in
	Inkscape `.svg` files, or whatever the equivalent for your software is. All
	files in this folder should follow the scheme
	`subject-rXXX-vXXX-details.extension`, where `subject` describes the thing
	you're working on in general, `rXXX` is the revision, `vXXX` is the version,
	`details` describes what this version has (or at the point of creation, what
	it _should_ have in future) and `extension` the filetype extension. Also, if
	you have two closely related models and the other one "appears" during
	development of the first one, take your time to make two subfolders and move
	all previous stuff into them.


## General thoughts

- Git or other versioning systems may be used atop of the `rXXX-vXXX` scheme or
	even inplace, just _communicate when that's the case._
- Projects and workflows can greatly differ. Adjust and adapt as _you_ see fit.
- Notes are very useful. When you're not sure what to tackle next, write down
	what you still need to do, details about it, and everything you have in mind
	in this very moment.
- Use `.zip` files for compressing exports. Don't expect everyone to have `tar`
	installed just because your system has it.


<!--
	vim: tw=80
-->
