A basic ircbot that receives webhook posts (currently from gitlab and github)
about git pushes, and utters them in an IRC channel.

Based on the example of https://github.com/StalkR/goircbot with a added
webhook plugin.

If an IRC server is using a self-signed certificate, or another cert not rooted
in a cert from the system's cert store, you can add it like so:

  cat >certs.pem /etc/ssl/certs/ca-certificates.crt irc-server-cert.pem
  sparv -cacerts certs.pem

Currently this is a global cert store is used by Sparv for all IRC servers.
