<img src="https://user-cdn.hackclub-assets.com/019d11fd-2806-7e75-bf75-9d22aabcde4a/Arrow-Banner-Light.png" alt="Arrow Browser Banner" width="850">

Arrow is my first foray into the fascinating world of web browser engineering! I originally wanted to make one from scratch (yup, including the rendering and JavaScript engines) but quickly realised that was a *very* dumb idea (unless you're prepared to undertake one of computing's hardest challenges like the people over at [Ladybird](https://github.com/LadybirdBrowser/ladybird/)).

I therefore pivoted to modifying the source code of Chromium, but the [ungoogled-chromium-macos](https://github.com/ungoogled-software/ungoogled-chromium-macos) fork to make things a bit more interesting! The way this works is — I tweak the UI to look like how I want it to (which usually means ~plagiarising~ borrowing interfaces from browsers I think are cool like [Arc](https://arc.net/) and [Zen](https://github.com/zen-browser/desktop)) and create a series of patches, which anyone building the source code from scratch can apply. This approach was inspired by the wonderful people behind the [Helium Browser](https://github.com/imputnet/helium)!

> [!WARNING]
> Arrow, atleast in its current form, is not a viable replacement for your daily browser. It is unstable and follows bad code practices, mainly because this was my first time working on a project of this scale. If you're looking for serious ungoogled-chromium browser, Helium is far better and has an active developer community working on it!

### A little note on design 

I chose Chromium because it is the most stable browser: Blink and V8 (the rendering and JavaScript engines) power not just Google Chrome but also Opera, Edge, Brave and a bunch of other browsers. In the future I'd like to experiment with Mozilla Firefox (and maybe even Safari).

## Current progress
*(last updated: March 23rd, 2026)*

<img src="https://cdn.hackclub.com/019d1ad9-1e1f-7228-b558-29e59d27c32d/arrow-desktop-mockup.png" width=600>

## Building

Same instructions as [ungoogled-chromium-macos](https://github.com/ungoogled-software/ungoogled-chromium-macos?tab=readme-ov-file#building)! You can clone either that repository (in which case, you'll have to copy over Arrow's patches folder `/patches/arrow`), or this one and follow the instructions from ungoogled's README. This will require installing tools like Python3 (also `PySocks` and `httplib2`), Metal Toolchain, Ninja, NodeJS, etc. Keep in mind the initial build can take several hours depending on how fast your data drive is.

Please also note building Chromium from scratch is a huge endeavour and will require a lot of storage (and a fast SSD for rebuilds). Make sure you have those to save yourself a lot of trouble later.

## Credits

1. **The Chromium Authors** (thank you also for writing well-documented code which made modifying the source much easier) 
2. **Ungoogled-Chromium**
3. In no particular order, the creators of: **Arc**, **Helium** and **Zen** for the UI inspiration!
