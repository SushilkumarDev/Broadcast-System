<h1 align="center">MiroTalk WebRTC Live Broadcast</h1>

<br />


<p align="center">MiroTalk BRO Live Broadcast allows to broadcast live video, audio and screen stream to all connected users (viewers) and receive messages from them. Can handle unlimited rooms, without time limitations, each having a broadcast and many viewers.</a></p>

---

<p align="center">
    <a href="https://bro.mirotalk.com">Explore MiroTalk BRO</a>
</p>

---

<p align="center">
    <a href="https://bro.mirotalk.com"><img src="./public/assets/images/ui.png"></a>
</p>


---

</details>

<details open>
<summary>Quick Start</summary>

<br/>

Start the app using [nodejs](https://nodejs.org/en/download):

```bash
# Copy .env.template in .env and edit it if needed
$ cp .env.template .env
# Install dependencies
$ npm install
# Run the app
$ npm start
```

Start the app using [docker](https://docs.docker.com/engine/install/) - [docker-compose](https://docs.docker.com/compose/) and optional [official image](https://hub.docker.com/r/mirotalk/bro):

![docker](public/assets/images/docker.png)

```bash
# Copy .env.template in .env and edit it if needed
$ cp .env.template .env
# Copy docker-compose.template.yml in docker-compose.yml and edit it if needed
$ cp docker-compose.template.yml docker-compose.yml
# Get official image from Docker Hub
$ docker pull mirotalk/bro:latest
# Run the image in a container
$ docker-compose up #-d
```

Server up and running

```js
Server is running {
  home: 'http://localhost:3016',
  broadcast: 'http://localhost:3016/broadcast?id=123&name=Broadcaster',
  viewer: 'http://localhost:3016/viewer?id=123&name=Viewer',
  viewerHome: 'http://localhost:3016/home?id=123'
}
```

The app should now be running on your http://localhost:3016, you can choose if join room as a `Broadcaster` or `Viewer`.

The `Broadcaster` stream the audio, video or screen to all connected viewers and can receive messages from them.

The `Viewer` get the audio, video or screen that is streamed from the broadcaster and can send messages to it.

</details>

<details>
<summary>Direct Join</summary>

<br>

You can direct join room as `broadcaster` or `viewer` specifying the room id and your name.

| As            | URL                                                     |
| ------------- | ------------------------------------------------------- |
| `Broadcaster` | http://localhost:3016/broadcast?id=123&name=Broadcaster |
| `Viewer`      | http://localhost:3016/viewer?id=123&name=Viewer         |

| Params | Type   | Description |
| ------ | ------ | ----------- |
| id     | string | Room Id     |
| name   | string | User name   |

</details>

<details>
<summary>Embedding</summary>

<br/>

Embedding MiroTalk Live Broadcast into a service or app using an iframe.

```html
<iframe
    allow="camera; microphone; display-capture; fullscreen; clipboard-read; clipboard-write; web-share; autoplay"
    src="https://bro.mirotalk.com"
    style="height: 100vh; width: 100vw; border: 0px;"
></iframe>
```

</details>

<details>
<summary>Documentations</summary>

<br>

-   [Install your own Stun/Turn](./docs/coturn.md)
-   [Ngrok](./docs/ngrok.md)
-   [How to Self-hosting](./docs/self-hosting.md)
-   [Rest API](./app/api/README.md)

</details>

<details>
<summary>Credits</summary>

<br>

-   Gabriel Tanner [webrtc-broadcast-logic](https://gabrieltanner.org/blog/webrtc-video-broadcast/)

</details>

<details>
<summary>License</summary>

<br/>

[![AGPLv3](public/assets/images/AGPLv3.png)](LICENSE)

MiroTalk BRO is free and open-source under the terms of AGPLv3 (GNU Affero General Public License v3.0). Please `respect the license conditions`, In particular `modifications need to be free as well and made available to the public`. Get a quick overview of the license at [Choose an open source license](https://choosealicense.com/licenses/agpl-3.0/).

To obtain a [MiroTalk BRO license](https://docs.mirotalk.com/license/licensing-options/) with terms different from the AGPLv3, you can conveniently make your [purchase on CodeCanyon](https://codecanyon.net/item/mirotalk-bro-webrtc-p2p-live-broadcast/45887113). This allows you to tailor the licensing conditions to better suit your specific requirements.

</details>

</details>

---
