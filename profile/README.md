<p align="center">
  <a href="https://webrtc.rs"><img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/webrtc.rs.png" alt="WebRTC.rs" height="140"></a>
</p>

<h1 align="center">Async-friendly and Sans-I/O WebRTC and SFU in Rust</h1>

<p align="center">
  <a href="https://webrtc.rs">🌐 Website</a>
  ·
  <a href="https://webrtc.rs/blog/">📝 Blog</a>
  ·
  <a href="https://appr.tc">📞 P2P Demo</a>
  ·
  <a href="https://sfu.rs">🎥 SFU Demo</a>
  ·
  <a href="https://discord.gg/4Ju8UHdXMs">🎙 Discord</a>
</p>

---

We build the whole WebRTC stack for Rust — from RTC protocols up to a browser-ready SFU, signaling server, and streaming ingest/egress. Everything is dual-licensed MIT / Apache-2.0.

Our cores are **sans-I/O**: pure state machines with no sockets, no threads, and no clock of their own. The caller owns all I/O. That buys deterministic tests without a network, an async layer that isn't welded to one runtime, and — as it turns out — a media *server* built from the very same trait.

## Projects

* [**sansio**](https://github.com/webrtc-rs/sansio) — the small `sansio::Protocol` trait everything else is written against.
* [**rtc**](https://github.com/webrtc-rs/rtc) — the sans-I/O WebRTC core: STUN · ICE · DTLS · SCTP · DataChannel · SRTP · RTP/RTCP · SDP · Interceptors.
* [**webrtc**](https://github.com/webrtc-rs/webrtc) — the async, runtime-agnostic `PeerConnection` API on top of `rtc`.
* [**sfu**](https://github.com/webrtc-rs/sfu) — a Selective Forwarding Unit for group calls on top of `rtc`, live at [sfu.rs](https://sfu.rs).
* [**apprtc**](https://github.com/webrtc-rs/apprtc) — signaling server and reference web app; P2P is live at [appr.tc](https://appr.tc), SFU signaling (🚧 *planned*) is next.
* [**whip**](https://github.com/webrtc-rs/whip) — WebRTC-HTTP Ingestion Protocol, for pushing streams *into* the stack. 🚧 *planned*
* [**whep**](https://github.com/webrtc-rs/whep) — WebRTC-HTTP Egress Protocol, for pulling streams *out* of it. 🚧 *planned*

## Work with us

Contributors and pull requests are always welcome, and there is plenty that is well-scoped and open. Sans-I/O means you can usually test your change without a network.

Built with 💖 and supported by our [sponsors](https://github.com/sponsors/webrtc-rs).
