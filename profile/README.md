<p align="center">
  <a href="https://webrtc.rs"><img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/webrtc.rs.png" alt="WebRTC.rs" height="140"></a>
</p>

<h1 align="center">Async-friendly and Sans-IO WebRTC and SFU in Rust</h1>

<p align="center">
  <a href="https://webrtc.rs">🌐 Website</a>
  ·
  <a href="https://webrtc.rs/blog/">📝 Blog</a>
  ·
  <a href="https://sfu.rs">🎥 SFU Demo</a>
  ·
  <a href="https://appr.tc">📞 P2P Demo</a>
  ·
  <a href="https://discord.gg/4Ju8UHdXMs">🎙 Discord</a>
</p>

---

We build the whole WebRTC stack for Rust — from raw protocol bytes (STUN, ICE, DTLS, SRTP, SCTP, RTP/RTCP,
SDP) up to a browser-ready SFU and signaling server. Everything is dual-licensed MIT / Apache-2.0.

Our cores are **Sans-I/O**: pure state machines with no sockets, no threads, and no clock of their own.
The caller owns all I/O. That buys deterministic tests without a network, an async layer that isn't welded
to one runtime, and — as it turns out — a media *server* built from the very same trait.

## Projects

* [**rtc**](https://github.com/webrtc-rs/rtc) — the Sans-I/O WebRTC core: ICE · DTLS · SRTP · SCTP · RTP/RTCP · SDP · interceptors · stats.
* [**webrtc**](https://github.com/webrtc-rs/webrtc) — the async, runtime-agnostic `PeerConnection` API on top of `rtc` (Tokio and smol).
* [**sfu**](https://github.com/webrtc-rs/sfu) — a Selective Forwarding Unit for group calls, live at [sfu.rs](https://sfu.rs).
* [**apprtc**](https://github.com/webrtc-rs/apprtc) — P2P + SFU signaling server and reference web app, live at [appr.tc](https://appr.tc).
* [**sansio**](https://github.com/webrtc-rs/sansio) — the small `Protocol` trait all of the above are written against.

## Work with us

Contributors and pull requests are always welcome, and there is plenty that is well-scoped and open — simulcast, publish/subscribe, TWCC congestion control, and per-hop RTX/NACK in [`sfu`](https://github.com/webrtc-rs/sfu), plus interop and performance work everywhere. Sans-I/O means you can usually test your change without a network. Come say hi on [Discord](https://discord.gg/4Ju8UHdXMs).

Built with 💖 and supported by our [sponsors](https://github.com/sponsors/webrtc-rs).
