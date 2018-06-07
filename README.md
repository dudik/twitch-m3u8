# twitch-m3u8
Node.js package that gets the .m3u8 URL of a Twitch stream or VOD

## Install
```
npm install twitch-m3u8
```
## Usage
```
const twitch = require('twitch-m3u8')('clientID');

// returns JSON object containing available qualities of a livestream
twitch.getStream('streamer')
.then(data => console.log(data))
.catch(err => console.error(err));

// returns JSON object containing available qualities of a VOD
twitch.getVod('vodID')
.then(data => console.log(data))
.catch(err => console.error(err));

// returns raw .m3u8 data containing available qualities of a livestream
twitch.getStream('streamer', true)
.then(data => console.log(data))
.catch(err => console.error(err));

// returns raw .m3u8 data containing available qualities of a VOD
twitch.getVod('vodID', true)
.then(data => console.log(data))
.catch(err => console.error(err));
```
