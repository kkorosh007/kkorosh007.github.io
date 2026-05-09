# Project Goal

Fooling around and around

# The Madness

I want a serverless p2p using only web stack to achive.

# Am I there yet

Ok so far we have isolated qr libs to create and scan qr codes.

That allows p2p connections using streaming qr codes to transfer sdp offer/answer payloads in chunks.

So p2p sdp connection takes < 3 - 5 secs.

Ideas to make it more usable is to allow coping and pasting using the clipboard so the qr code (or png version)
can be sent large enough to carry the full offer or reply.
Looking at WebShare API to allow pushing such payloads to the users other apps to transmit,
but its flacky and has no reverse method to share a file or text from another app with the site listening
So clipboard seems the only way.

The turn and stun server can be configured to allow pointing to preferd server (only way around CGNAT's)

So the idea is, What? To allow using github as a static store content needed to allow p2p connections between devices, primarily on the same lan, using offline/no signaling server methods.

To allow clipboard usage qr encoding will look at reducing the sdp packet size, although needs testing to
make sure it is safe. Current aim is a single datachannel connection using sfrlx stun and turn candidates so 1 stun and one turn.  I can provide the setup and config, but need a db handler to share user and pass settings so access can be controled. (MORE THOUGHT NEEDED)

Now that I can connect p2p using qr code handshake, will look at remote control of peer media devices
using the datachannel to send constraint requests to the remote peer to change the device settings.  The idea to
use one devices camera as if it was connected to your device, controlling zoom and other constraints.

A client side state management that can survive the browser history being cleared. using SPA to install
a self updating web app that holds the client state within its manifest.json file.

Full AES and public/private key management to allow sharing and verifiy content from peers. Using public keys
to encrypt and private keys to sign each message along with the needed security biolerplate.

Key critiria I am working under. try to have a single payload to download and keep it under 14Kb.  Those 
constraints allows quick initial page load, and everything else is lazy loaded or loaded as needed.

If I can be botherd I need a prep step to allow writting the code in files and merging them, but keeping the 
code in one file is simpler for a 1 person project.

PS.
I hate HTML, CSS and JS. but it gives access to most devices.

# THE UI

well that is a weak point, I grant you.  I simple js evaluator interface allows running the functions by hand
The final ideal is a progresive and dynamic grid of contacts and a slider menu system for interaction.
