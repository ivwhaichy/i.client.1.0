# Third-Party Notices

The i.client Android distribution is licensed under GPL-3.0-or-later.
Copyright notices in third-party source files remain unchanged.

- sing-box 1.14.4, copyright nekohasekai: GPL-3.0-or-later, with an additional
  restriction against using its name or implying association without consent.
  Upstream: https://github.com/SagerNet/sing-box/tree/v1.14.4
- vk-turn-proxy 1.8.3, revision e8a96967dc66f3dbd631596ea6a8b9fe03f9be69:
  GPL-3.0. Upstream: https://github.com/cacggghp/vk-turn-proxy
  Android patches and complete modified source accompany each release.
- AndroidX, Jetpack Compose and WorkManager: Apache-2.0. Android apksig is used
  only in instrumentation tests as of 1.3.2 (Apache-2.0).
- Kotlin: Apache-2.0. Gradle: Apache-2.0.
- Go standard library: BSD-style license; the Go toolchain is not embedded.

The corresponding-source archive contains upstream license texts and vendored
Go dependency sources with their notices. Maven dependencies are pinned in the
Gradle files. The APK also carries the TURN helper's patched source and license.
Source JARs of the resolved Maven dependencies, including the test-only apksig,
are provided in the
additional i.client-jvm-sources-VERSION.zip release asset, with their coordinates.
Production downloads are handed to the browser; Android verifies installation
and the installed package's signing identity. Test fixtures still use apksig
to check signature/digest rejection behavior.

i.client is independent of VK, GitHub, OpenVPN and the sing-box project. No
affiliation or endorsement by those projects is claimed. Product and protocol
names identify interoperability only.
