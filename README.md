SarHelper
=========

I typically use sar on all of my servers and find I sometimes have to grep through
the man pages to find a certain switch I need information about. I wrote this program
to quickly go through select areas of interest and highlight potential problem areas.

In the future I paln on integrating SarHelper with atop to quickly locate processes that
may be causing system irregularities.

Usage Example
=========
<code>
./SarHelper /var/log/sa/sa06 07:00:00 19:00:00
</code>

This would parse the sar log <code>/var/log/sa/sa06</code> starting at 7AM and ending at 7PM
