---
title: Foundry and Jitsi
category: FoundryVTT Blog
---
FoundryVTT has built in P2P videoconferencing. With more players a centralised server is more beneficial compared to sending all your own information to all peers. A module for using Jitsi is available for FoundryVTT and I've explored it a bit.

# Jitsi
Jitsi is an open source alternative to the likes of zoom, skype and whatnot for video conferencing. Apparently it's in a quite usable state as parts of the US government rely on it. Using it in FoundryVTT would make it so all connected clients communicate with the Jitsi server, send their info and grab what others have sent instead of sending all their info to all participants. With more than two participants this lowers bandwidth consumption.

## FoundryVTT Integration
Enabling the module seems to work by default, using public servers, but from what I have gathered there's a maximum number of participants which is quite low on those server. From my initial testing there can be quite severe lag, I guess it was around 20 seconds at its worst between my laptop and desktop. I can't recall if this was from self hosted or public server tough. Self hosting provides some more benefits than the public servers. One of them being actually having your own video conferencing available. Another would be real time subtitling, I forget the word but since I mainly plan to be using this with swedes it's not as attractive a feature as with English audiences.

## Self hosting Jitsi
Getting Jitsi up on my Debian server was relatively easy. Getting it to behave was another. I'm growing more familiar with nginx and the configs, I was able to get SSL upp thanks to this little adventure but actually getting Jitsi upp with authentication (at least for setting up meetings) seemed to be beyond my powers.
After checking resource usage I realized that actually using Jitsi on that server would not be ideal. I do not see the need to expand resources for something that I think will ultimately not be used.

## Verdict
Jitsi seems nice, I'm glad I stumbled upon that YouTube video mentioning it and took the deep dive into trying to get it set up in foundry. It is not quite as easy to set up as I had hoped but I learned some things at least. I might very well look into using jitsi in the future, not necessarily for TTRPG.

