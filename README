PirateScope
-----------

A simple oscilloscope client for the Bus Pirate universal serial
interface.  (Visit http://dangerousprototypes.com/docs/Bus_Pirate for
more information.)


System Requirements
-------------------

Operating System:
- PirateScope has been tested under Debian GNU/Linux and OS X Snow
  Leopard.

Software:
- Python 2.x (http://www.python.org/)
- wxPython (http://www.wxpython.org/)
- numpy (http://www.numpy.org/)

Hardware:
- Bus Pirate with firmware v5.9 or later


Installation
------------

Under Debian, the software dependencies can be met simply by
installing the necessary packages using apt.

Under OS X the process is slightly more involved, but Github
user @granitepenguin has generously provided detailed
instructions, which are contained within the file INSTALL.OSX.
Alternatively, as nicely pointed out by @esalgado, one can use
MacPorts to simplify the process. (This is also described in
INSTALL.OSX.)


Usage notes
-----------

PirateScope has several modes of operation,  the default being the
continuous sampling mode without synchronisation.  This is a good
starting point, as it allows you to see whether any signal is being
received. The sampling rate and the total number of samples displayed
in the window can each be adjusted at any time using the controls on
the right-hand side of the "Sampling" panel.

Once you're getting a clear signal, it may be sensible to select one
of the triggering radio buttons at the bottom-right of the screen.
These only begin capture and display of samples when the input voltage
level crosses the "trigger" voltage level.  This voltage level can be
adjusted by shifting the vertical slider to the right of the graph.
(The current trigger level can be shown on the graph by selecting the
relevant option from the View menu.)  The "Offset" spin control allows
you to adjust the time offset of the displayed data relative to the
trigger time, so that signal immediately prior or some time after the
triggering event can be observed.

For capturing rare events, it may be sensible to use the triggering
mode in combination with the "Single shot" sampling mode.  It is also
possible to perform single shot sampling without triggering, although
this is less useful.

Selecting the "Spectrum" checkbox replaces the time domain output with
a frequency domain graph of the same signal.  This is the magnitude of
a Fourier transform of the most recent window of the captured signal.
(This is continuously updated as more data is acquired, but only the
most recent window of data is ever used to compute the spectrum.) The
maximum frequency is set by the Nyquist frequency, which is half the
current sampling rate.

The most recent displayed sampled voltages can be written to disk
using the File->Save Sample.  This creates an ASCII file containing
two columns, with the first being the sample times and the second
being the corresponding voltage measurements. The first row of the
file is a header which allows the data file to be easily read into R
data analysis environment (http://www.r-project.org).

The currently-displayed graph can also be written to disk as an image
in a variety of formats (including BMP, JPEG and PNG) using
File->Save Graph.
