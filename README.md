# Revideo-Colab-Standalones
Standalone Colab notebooks for creating videos with [Revideo](https://re.video/). This repo is a collection of experiments using their provided [API](https://docs.re.video/category/api-reference), designed to be easily accessible and usable by anyone, anywhere, through Colab.

## Overview
![template.gif](/outputs/template.gif)

This Colab template lets you easily explore and use Revideo. It's an open-source library for programmatically creating videos, pretty fun to work with!

## Quickstart

### Step 1: Setup

No setup needed! Everything is included in this [notebook](https://github.com/AmanPriyanshu/Revideo-Colab/blob/main/Re_Video_Complete_Colab_Run.ipynb).

### Step 2: Run

Go through the notebook and run each cell. This lets you interactively load Revideo templates, modify parameters, and render videos right in your browser.

### Step 3: Customize

There's a bunch of things to customize and try out. Check out their [Revideo Documentation](https://docs.re.video/)

## Note

One main thing: when running on Colab, ensure that the `renderVideo` function in your project's `src/render.ts` file includes the `--no-sandbox` argument in the `puppeteer` configuration. Here's an example of how it should look:

```javascript
import { renderVideo } from '@revideo/renderer';

renderVideo(
  './path/to/your/config.ts',
  { color: 'white', range: [1, 10] },
  { puppeteer: { args: ['--no-sandbox'] } }
);
```

This argument is necessary for Puppeteer to work properly in the Colab environment.

## Contributing

Want to contribute to more standalone Colab projects or templates? Raise an issue here! I'd love to expand this project through standalone contributions.

## Credits

Revideo is an amazing open-source project that I'm experimenting with!

- [Website](https://re.video/)
- [GitHub](https://github.com/redotvideo/revideo)
