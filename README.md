# 🔊 EchoLink

**Turn your phone into a wireless speaker for your PC.**
Share your computer's audio to any phone browser using a 4-digit code. No app to install, no account to create.

Built with **WebRTC** and **PeerJS**. The whole project is a single HTML file.

---

## ✨ Features

- **Zero setup:** open the page on both devices, no install and no sign-up
- **4-digit pairing code:** the easiest way to link your PC and phone
- **Direct audio streaming:** sound goes straight from your PC to your phone (peer-to-peer)
- **Pause / Resume / Disconnect:** available on both devices and kept in sync
- **Auto-reconnect:** keep the same code alive and rejoin automatically if the connection drops
- **Lock-screen controls:** play and pause buttons on Android (Chrome)
- **Private:** nothing is recorded, saved, or uploaded

---

## 🚀 How to use

### On the computer
1. Open the page in **Chrome** or **Edge**.
2. Start sharing and choose **Entire Screen**.
3. Turn on **Share system audio**, then press **Share**.
4. A 4-digit pairing code appears.

### On the phone
1. Open the same page in any modern browser.
2. Enter the 4-digit code and connect.
3. Sound now plays from your phone. Use the **phone's volume buttons** to adjust it.

> Your computer stays silent while the phone is playing.

---

## 📋 Requirements

| Device | Requirement |
|---|---|
| **Computer** | Chrome or Edge. Full system audio works best on **Windows**; on macOS/Linux the browser may only share one tab's audio. |
| **Phone / tablet** | Any modern browser with sound turned up |
| **Internet** | Needed on both devices (the 4-digit code uses the PeerJS pairing service) |
| **Network** | Same Wi-Fi is recommended (see below) |

---

## 🌐 Network notes

EchoLink uses a public **STUN** server to help the two devices find each other. It does **not** use a TURN relay.

- ✅ **Same Wi-Fi:** works reliably.
- ⚠️ **Different networks:** may work, but can fail, especially when the phone is on mobile data behind carrier-grade NAT, or on strict school/office/guest networks.

To make it work on any network, add a TURN server to the `iceServers` list in the code.

---

## ⚠️ Limitations

- Only **one phone** can connect at a time.
- Small delay of about **50–300 ms**. Fine for music and podcasts, noticeable in videos.
- Bluetooth speakers or earbuds on the phone add extra delay.
- **Sound only:** no video, and no phone microphone sent back to the PC.
- The code stops working when you stop sharing or close the page.
- Changing the PC's volume while sound plays can make the audio too quiet. Use the phone's volume instead.

### When the phone screen turns off

- **Android + Chrome:** sound should keep playing.
- **iPhone:** Apple often stops web audio when the screen locks. This is an iOS limitation.
- Battery saver can also stop playback. Set your browser to **Unrestricted** in battery settings.
- Keep the EchoLink page open in the browser.

### Browser sharing bar

Chrome and Edge always show a bar saying the page is sharing your screen and audio. A web page cannot remove it, but you can press **Hide**. No picture is recorded or sent, only sound.

---

## 🛠️ Troubleshooting

| Problem | Fix |
|---|---|
| Phone can't find the computer | Check the 4 digits and make sure the computer is still sharing |
| No sound | Make sure **Share system audio** was ticked and the computer is playing something |
| Still stuck | Press **Stop sharing**, then start again to get a new code |
| "Pairing service could not load" | Check your internet connection and reload the page |

---

## 🔒 Privacy

- Audio travels **directly from your computer to your phone**.
- The pairing service only helps devices find each other with the code. It never receives your sound.
- Nothing is saved, recorded, or uploaded.
- Press **Stop sharing** when you're done so nobody else can join with the code.

---

## 🧰 Tech stack

- HTML, CSS, JavaScript (single file)
- [WebRTC](https://webrtc.org/) for real-time audio
- [PeerJS](https://peerjs.com/) for pairing and signaling
- Screen Capture API and Media Session API

---

## 👤 Developer

**Rifaat Al Hasan (Ayon)**, Software Engineering student at Daffodil International University

- 📧 [alhasanayon26@gmail.com](mailto:alhasanayon26@gmail.com)
- 🌐 [Portfolio](https://alhasanayon26.github.io/Al-Hasan-Ayon)

---

## 📄 License

MIT. Feel free to change this to whichever license you prefer.
