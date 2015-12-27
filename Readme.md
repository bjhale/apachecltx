APACHECTLX
==========

This is a modified version of the apachectl script that comes with OSX re-implementing status and fullstatus.

Requirements
------------

 * Homebrew
 * Lynx

Installation
------------
```shell
git clone https://github.com/bjhale/apachectlx.git
cd apachectlx
cp apachectlx /usr/local/bin/
```

Usage
-----
Can be used just like apachectl.

For new functionality:
```shell
apachectlx status
apachectlx fullstatus
```

Examples
--------

```shell
iMac:~ user$ apachectlx status
                  Apache Server Status for localhost (via ::1)

   Server Version: Apache/2.4.16 (Unix) PHP/5.6.16
   Server MPM: prefork
   Server Built: Aug 22 2015 16:51:57
     __________________________________________________________________

   Current Time: Sunday, 27-Dec-2015 13:22:19 MST
   Restart Time: Sunday, 27-Dec-2015 10:38:10 MST
   Parent Server Config. Generation: 6
   Parent Server MPM Generation: 5
   Server uptime: 2 hours 44 minutes 8 seconds
   Server load: 1.58 1.63 1.57
   Total accesses: 161 - Total Traffic: 261 kB
   CPU Usage: u.09 s.08 cu0 cs0 - .00173% CPU load
   .0163 requests/sec - 27 B/second - 1660 B/request
   1 requests currently being processed, 7 idle workers

_______W........................................................
................................................................
................................................................
..........................................................

   Scoreboard Key:
   "_" Waiting for Connection, "S" Starting up, "R" Reading Request,
   "W" Sending Reply, "K" Keepalive (read), "D" DNS Lookup,
   "C" Closing connection, "L" Logging, "G" Gracefully finishing,
   "I" Idle cleanup of worker, "." Open slot with no current process
```

```shell
iMac:~ user$ apachectlx fullstatus
                  Apache Server Status for localhost (via ::1)

   Server Version: Apache/2.4.16 (Unix) PHP/5.6.16
   Server MPM: prefork
   Server Built: Aug 22 2015 16:51:57
     __________________________________________________________________

   Current Time: Sunday, 27-Dec-2015 13:23:01 MST
   Restart Time: Sunday, 27-Dec-2015 10:38:10 MST
   Parent Server Config. Generation: 6
   Parent Server MPM Generation: 5
   Server uptime: 2 hours 44 minutes 50 seconds
   Server load: 1.64 1.64 1.57
   Total accesses: 162 - Total Traffic: 266 kB
   CPU Usage: u.09 s.08 cu0 cs0 - .00172% CPU load
   .0164 requests/sec - 27 B/second - 1681 B/request
   1 requests currently being processed, 7 idle workers

____W___........................................................
................................................................
................................................................
..........................................................

   Scoreboard Key:
   "_" Waiting for Connection, "S" Starting up, "R" Reading Request,
   "W" Sending Reply, "K" Keepalive (read), "D" DNS Lookup,
   "C" Closing connection, "L" Logging, "G" Gracefully finishing,
   "I" Idle cleanup of worker, "." Open slot with no current process

   Srv PID Acc M CPU SS Req Conn Child Slot Client VHost Request
   0-5 64669 0/17/17 _ 0.02 1502 0 0.0 0.03 0.03 ::1 localhost:80 GET
   /server-status HTTP/1.0
   1-5 64670 0/20/20 _ 0.02 46 0 0.0 0.03 0.03 ::1 localhost:80 GET
   /server-status HTTP/1.0
   2-5 64671 0/26/26 _ 0.03 1362 0 0.0 0.05 0.05 ::1 localhost:80 GET
   /server-status HTTP/1.0
   3-5 64672 0/24/24 _ 0.02 1616 6 0.0 0.04 0.04 ::1 localhost:80 GET
   /server-status HTTP/1.0
   4-5 64673 0/17/17 W 0.02 0 0 0.0 0.02 0.02 ::1 localhost:80 GET
   /server-status HTTP/1.0
   5-5 64674 0/25/25 _ 0.02 1513 6 0.0 0.04 0.04 ::1 localhost:80 GET
   /server-status HTTP/1.0
   6-5 64675 0/17/17 _ 0.02 525 18 0.0 0.03 0.03 ::1 localhost:80 GET
   /server-status HTTP/1.0
   7-5 64676 0/16/16 _ 0.02 42 0 0.0 0.02 0.02 ::1 localhost:80 GET
   /server-status HTTP/1.0
     __________________________________________________________________

    Srv  Child Server number - generation
    PID  OS process ID
    Acc  Number of accesses this connection / this child / this slot
     M   Mode of operation
    CPU  CPU usage, number of seconds
    SS   Seconds since beginning of most recent request
    Req  Milliseconds required to process most recent request
   Conn  Kilobytes transferred this connection
   Child Megabytes transferred this child
   Slot  Total megabytes transferred this slot
```

FAQ
---

###Can I install this with Homebrew.
Not yet. Maybe in the future.
    