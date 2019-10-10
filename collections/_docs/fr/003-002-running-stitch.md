---
title: "Running Stitch"
permalink: /fr/docs/stitches/running-stitch/
excerpt: ""
last_modified_at: 2018-12-14
toc: true
---
## What it is

[![Running Stitch Butterfly](/assets/images/docs/running-stitch.jpg){: width="200x"}](/assets/images/docs/running-stitch.svg){: title="Download SVG File" .align-left download="running-stitch.svg" }

Running stitch produces a series of small stitches following a line or curve.

![Running Stitch Detail](/assets/images/docs/running-stitch-detail.jpg)

## How to Create
Running stitch can be created by setting a **dashed stroke** on a path. Any type of dashes will do the job, and the stroke width is irrelevant.

![Running Stitch Dashes](/assets/images/docs/running-stitch-dashes.jpg){: .align-left style="padding: 5px"}
Select the stroke and go to `Object > Fill and Stroke...` and choose one of the dashed lines in the `Stroke style` tab.

Open [`Extensions > Ink/Stitch  > Params`](/docs/params/#stroke-params) to change parameters to your needs.

**Info:** In order to avoid rounding corners, an extra stitch will be added at the point of any sharp corners.
{: .notice--info style="clear: both;" }

## Sample Files Including Running Stitch
{% include tutorials/tutorial_list key="stitch-type" value="Running Stitch" %}
