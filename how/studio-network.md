# Studio Network — the Mac becomes the network

[日本語](studio-network.ja.md) · [How it works](README.md)

Studio Network turns the Mac into a Wi-Fi network of its own. No router is needed; cameras and iPhones can join it anywhere.

The network does not reach the internet. It is closed: a camera on it cannot get out.

Devices running Tethr announce themselves to each other and find each other on their own.
Between two devices that have found each other, Tethr opens a single authenticated, encrypted connection.
The camera's state, shooting commands and a preview of each new frame travel through it.
Whichever iPhone takes the shot, the frame reaches every screen.

Limits today: while the network is up, the Mac's Wi-Fi does not join the home network.
The network runs on 2.4 GHz, so cameras that only have 2.4 GHz Wi-Fi can join too.
