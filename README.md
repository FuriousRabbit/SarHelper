SarHelper
=========

I typically use sar on all of my servers and find I sometimes have to grep through
the man pages to find a certain switch I need information about. I wrote this program
to quickly go through select areas of interest and highlight potential problems.

In the future I paln on integrating SarHelper with atop to quickly locate processes that
may be causing system irregularities.

Usage Example
=========
<code>
./SarHelper /var/log/sa/sa06 07:00:00 19:00:00
</code>

This would parse the sar log <code>/var/log/sa/sa06</code> starting at <code>7AM</code> and ending at <code>7PM</code>

Example Output
=========

CPU Idle Percent         Load Averages
__________________       ___________________________
01:00:01 PM  99.07       01:00:01 PM  0.00 0.00 0.00
01:10:01 PM  99.07       01:10:01 PM  0.00 0.00 0.00
01:20:01 PM  <code>76.08</code>       01:20:01 PM  0.00 0.02 0.00
01:30:01 PM  99.07       01:30:01 PM  <code>1.01 0.67 0.33</code>
01:40:01 PM  99.06       01:40:01 PM  0.00 0.00 0.00

