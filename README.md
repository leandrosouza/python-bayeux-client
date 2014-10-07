python-bayeux-client
====================

A simple python bayeux client that connects to a server using the Bayeux protocol 
and allows for users to receive data published by the server.

Usage
=====
<pre><code>
from bayeux.bayeux_client import BayeuxClient
def cb(data):
  print(data)
bc = BayeuxClient('http://localhost:8080/cometd')
bc.register('channel/foo/bar', cb)
bc.start()
</code></pre>

Dependencies
============
Twisted (http://twistedmatrix.com/trac/)<br>
zope.interface (https://pypi.python.org/pypi/zope.interface#download)<br>
