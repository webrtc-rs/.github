<p align="center">
  <a href="https://webrtc.rs"><img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/webrtc.rs.png" alt="WebRTC.rs" height="140"></a>
</p>

<h1 align="center">Async-friendly and Sans-I/O WebRTC and SFU in Rust</h1>

<p align="center">
  <a href="https://webrtc.rs">🌐 Website</a>
  ·
  <a href="https://webrtc.rs/blog/">📝 Blog</a>
  ·
  <a href="https://appr.tc">🎥 P2P/SFU Demo</a>
  ·
  <a href="https://discord.gg/4Ju8UHdXMs">🎙 Discord</a>
</p>

---

We build the full WebRTC network/protocol ecosystem in Rust — from low-level RTC protocols up to a browser-ready SFU, signaling server, and streaming ingest/egress. Everything is dual-licensed MIT / Apache-2.0.

Our cores are **Sans-I/O**: pure state machines with no sockets, no threads, and no clock of their own. The caller owns all I/O. That buys deterministic tests without a network, an async layer that isn't welded to one runtime, and — as it turns out — a media *server* built from the very same trait.

## Projects

* [**sansio**](https://github.com/webrtc-rs/sansio) — the small `sansio::Protocol` trait everything else is written against.
* [**rtc**](https://github.com/webrtc-rs/rtc) — the Sans-I/O WebRTC core: ICE · STUN · TURN · mDNS · DTLS · SCTP · DataChannel · SRTP · RTP/RTCP · SDP.
* [**sfu**](https://github.com/webrtc-rs/sfu) — a Sans-I/O SFU (Selective Forwarding Unit) media server for group calls on top of `rtc`.
* [**webrtc**](https://github.com/webrtc-rs/webrtc) — the async, runtime-agnostic `PeerConnection` API on top of `rtc`.
* [**apprtc**](https://github.com/webrtc-rs/apprtc) — P2P/SFU signaling server and reference web app with automatic P2P→SFU upgrade, live at [appr.tc](https://appr.tc).

Everything is published on crates.io:

<p align="center">
    <img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/check.png">AppRTC<a href="https://crates.io/crates/apprtc"><img src="https://img.shields.io/crates/v/apprtc.svg"></a>
    <img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/check.png">AppWeb<a href="https://crates.io/crates/appweb"><img src="https://img.shields.io/crates/v/appweb.svg"></a>
    <img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/check.png">Signaling<a href="https://crates.io/crates/signaling"><img src="https://img.shields.io/crates/v/signaling.svg"></a>
    <br><br>
    <img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/check.png">WebRTC<a href="https://crates.io/crates/webrtc"><img src="https://img.shields.io/crates/v/webrtc.svg"></a>
    <img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/check.png">RTC<a href="https://crates.io/crates/rtc"><img src="https://img.shields.io/crates/v/rtc.svg"></a>
    <img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/check.png">SFU<a href="https://crates.io/crates/sfu"><img src="https://img.shields.io/crates/v/sfu.svg"></a>
    <br>
    <img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/check.png">Media<a href="https://crates.io/crates/rtc-media"><img src="https://img.shields.io/crates/v/rtc-media.svg"></a>
    <img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/check.png">Interceptor<a href="https://crates.io/crates/rtc-interceptor"><img src="https://img.shields.io/crates/v/rtc-interceptor.svg"></a>
    <img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/check.png">DataChannel<a href="https://crates.io/crates/rtc-datachannel"><img src="https://img.shields.io/crates/v/rtc-datachannel.svg"></a>
    <br>
    <img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/check.png">RTP<a href="https://crates.io/crates/rtc-rtp"><img src="https://img.shields.io/crates/v/rtc-rtp.svg"></a>
    <img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/check.png">RTCP<a href="https://crates.io/crates/rtc-rtcp"><img src="https://img.shields.io/crates/v/rtc-rtcp.svg"></a>
    <img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/check.png">SRTP<a href="https://crates.io/crates/rtc-srtp"><img src="https://img.shields.io/crates/v/rtc-srtp.svg"></a>
    <img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/check.png">SCTP<a href="https://crates.io/crates/rtc-sctp"><img src="https://img.shields.io/crates/v/rtc-sctp.svg"></a>
    <br>
    <img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/check.png">DTLS<a href="https://crates.io/crates/rtc-dtls"><img src="https://img.shields.io/crates/v/rtc-dtls.svg"></a>
    <br>
    <img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/check.png">mDNS<a href="https://crates.io/crates/rtc-mdns"><img src="https://img.shields.io/crates/v/rtc-mdns.svg"></a>
    <img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/check.png">STUN<a href="https://crates.io/crates/rtc-stun"><img src="https://img.shields.io/crates/v/rtc-stun.svg"></a>
    <img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/check.png">TURN<a href="https://crates.io/crates/rtc-turn"><img src="https://img.shields.io/crates/v/rtc-turn.svg"></a>
    <img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/check.png">ICE<a href="https://crates.io/crates/rtc-ice"><img src="https://img.shields.io/crates/v/rtc-ice.svg"></a>
    <br>
    <img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/check.png">SDP<a href="https://crates.io/crates/rtc-sdp"><img src="https://img.shields.io/crates/v/rtc-sdp.svg"></a>
    <img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/check.png">Shared<a href="https://crates.io/crates/rtc-shared"><img src="https://img.shields.io/crates/v/rtc-shared.svg"></a>
    <img src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/check.png">SansIO<a href="https://crates.io/crates/sansio"><img src="https://img.shields.io/crates/v/sansio.svg"></a>
</p>

Each webrtc-rs project is developed and released as an independent Rust crate or application. To keep development fast, projects that depend on unreleased changes use Git submodules instead of waiting for every internal crate to be published to crates.io. The nested source layout used by AppRTC is:

```text
apprtc/
├── apprtc/                                       # AppRTC executable crate
├── appweb/                                       # AppRTC web/API crate
├── signaling/                                    # AppRTC signaling crate
├── signaling-proto/                              # AppRTC signaling-proto crate
└── [sfu]/                                        # SFU repository, AppRTC submodule
      └── [webrtc]/                               # async WebRTC repository, SFU submodule
              └── [rtc]/                          # Sans-I/O RTC repository, WebRTC submodule
                    ├── rtc-datachannel           # DataChannel crate
                    ├── rtc-dtls                  # DTLS crate
                    ├── rtc-ice                   # ICE crate
                    ├── rtc-interceptor           # Interceptor crate
                    ├── rtc-interceptor-derive    # Interceptor Derive crate
                    ├── rtc-mdns                  # mDNS crate
                    ├── rtc-media                 # Media crate
                    ├── rtc-rtcp                  # RTCP crate
                    ├── rtc-rtp                   # RTP crate
                    ├── rtc-sctp                  # SCTP crate
                    ├── rtc-sdp                   # SDP crate
                    ├── rtc-shared                # Shared crate
                    ├── rtc-srtp                  # SRTP crate
                    ├── rtc-stun                  # STUN crate
                    └── rtc-turn                  # TURN crate
```

This lets AppRTC build and test against the exact in-development SFU, async WebRTC, and RTC revisions while preserving independent repositories, versioning, releases, and crates.io publication. Published consumers continue to use the corresponding crates.io versions; the submodule layout is a development workflow for cross-repository changes and integration testing.


## Work with us

Contributors and pull requests are always welcome, and there is plenty that is well-scoped and open — simulcast, publish/subscribe, and congestion control in [`sfu`](https://github.com/webrtc-rs/sfu), plus interop and performance work everywhere. Sans-I/O means you can usually test your change without a network. Come say hi on [Discord](https://discord.gg/4Ju8UHdXMs).

---

<p align="center">
    Built with 💖 and supported by our sponsors:
    <br><br>
    <a href="https://github.com/sponsors/webrtc-rs"><img width="16" height="16" alt="GitHub Sponsors" src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/github-sponsors.svg" />&nbsp;github.com/sponsors/webrtc-rs</a> 
    &nbsp;·&nbsp;
    <a href="https://opencollective.com/webrtc-rs"><img width="16" height="16" alt="Open Collective" src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/open-collective.svg" />&nbsp;opencollective.com/webrtc-rs</a>
    &nbsp;·&nbsp;
    <a href="https://patreon.com/WebRTCrs"><img width="16" height="16" alt="Patreon" src="https://raw.githubusercontent.com/webrtc-rs/webrtc-rs.github.io/master/res/patreon.svg" />&nbsp;patreon.com/WebRTCrs</a>
</p>
