tcx-annotator
=============

A script to overlay video with gps data

Given a video of a bike ride and telemetry data as tcx file, the script combines the two in a video that contains the original video with telemetry data overlay

The original file is splitted in frames using ffmpeg, for each frame the frame and the synchronized trackpoint are passed to a php that produce an svg file.
The svg file contains the original frame and the telemetry data ( gauges, elevation, etc ) based on trackpoint data.
The svg file is rendered to a jpeg using a renderer ( convert, phantomjs, batik )
Finally, the output movie is done by merging the rendered jpeg



