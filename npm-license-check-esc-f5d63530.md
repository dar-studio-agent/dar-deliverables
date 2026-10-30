# npm license check

Source for every row: the public npm registry record at `registry.npmjs.org/<name>`. The latest version is the value of `dist-tags.latest`; the license is that version's `license` field; publish time is the `time` field for that same version, in UTC.

| package | latest version | license | publish time (UTC) |
|---|---|---|---|
| react | 19.3.1 | MIT | 2026-10-14T16:47:15.290Z |
| vue | 3.5.44 | MIT | 2026-10-13T07:45:32.806Z |
| lodash | 4.18.1 | MIT | 2026-04-01T21:01:20.458Z |
| axios | 1.21.0 | MIT | 2026-10-27T07:18:54.313Z |
| typescript | 7.0.2 | Apache-2.0 | 2026-07-08T15:55:18.431Z |
| svelte | 5.57.3 | MIT | 2026-10-26T18:16:20.865Z |

## Proof and raw registry excerpts

Every fragment below is copied character-for-character from the identified registry response, without reformatting, reordering, or removing keys inside the fragment. Separate contiguous fragments are used for `dist-tags`, the latest version object, and `time`.

### react

- Request: host `registry.npmjs.org`, path `/react`
- Full request URL: `https://registry.npmjs.org/react`
- Retrieved at (UTC): `2026-10-30T16:28:13.421811+00:00`

Raw contiguous fragment from `dist-tags` (unchanged):

```text
"dist-tags":{"beta":"19.0.0-beta-26f2496093-20240514","rc":"19.0.0-rc.1","next":"19.3.0-canary-d5736f09-20260507","latest":"19.3.1",
```

Raw contiguous fragment from the latest version object through its `license` field (unchanged):

```text
"19.3.1":{"name":"react","version":"19.3.1","keywords":["react"],"license":"MIT"
```

Raw contiguous fragment from the top-level `time` object (unchanged):

```text
"19.3.1":"2026-10-14T16:47:15.290Z"
```

### vue

- Request: host `registry.npmjs.org`, path `/vue`
- Full request URL: `https://registry.npmjs.org/vue`
- Retrieved at (UTC): `2026-10-30T16:28:15.799898+00:00`

Raw contiguous fragment from `dist-tags` (unchanged):

```text
"dist-tags":{"csp":"1.0.28-csp","v2-latest":"2.7.16","legacy":"2.7.16","alpha":"3.6.0-alpha.7","beta":"3.6.0-beta.17","latest":"3.5.44",
```

Raw contiguous fragment from the latest version object through its `license` field (unchanged):

```text
"3.5.44":{"name":"vue","version":"3.5.44","keywords":["vue"],"author":"Evan You","license":"MIT"
```

Raw contiguous fragment from the top-level `time` object (unchanged):

```text
"3.5.44":"2026-10-13T07:45:32.806Z"
```

### lodash

- Request: host `registry.npmjs.org`, path `/lodash`
- Full request URL: `https://registry.npmjs.org/lodash`
- Retrieved at (UTC): `2026-10-30T16:28:16.828223+00:00`

Raw contiguous fragment from `dist-tags` (unchanged):

```text
"dist-tags":{"latest":"4.18.1"}
```

Raw contiguous fragment from the latest version object through its `license` field (unchanged):

```text
"4.18.1":{"name":"lodash","version":"4.18.1","keywords":["modules","stdlib","util"],"author":{"name":"John-David Dalton","email":"john.david.dalton@gmail.com"},"license":"MIT"
```

Raw contiguous fragment from the top-level `time` object (unchanged):

```text
"4.18.1":"2026-04-01T21:01:20.458Z"
```

### axios

- Request: host `registry.npmjs.org`, path `/axios`
- Full request URL: `https://registry.npmjs.org/axios`
- Retrieved at (UTC): `2026-10-30T16:28:17.193397+00:00`

Raw contiguous fragment from `dist-tags` (unchanged):

```text
"dist-tags":{"next":"1.7.0-beta.2","old-version":"0.30.0","latest":"1.21.0",
```

Raw contiguous fragment from the latest version object through its `license` field (unchanged):

```text
"1.21.0":{"_id":"axios@1.21.0","bugs":{"url":"https://github.com/axios/axios/issues"},"dist":{"shasum":"30c363a2652d9649e8b4d2645b34c64ca541ff67","tarball":"https://registry.npmjs.org/axios/-/axios-1.21.0.tgz","integrity":"sha512-YCzXMB53Q9PZBsh7yN7wtapit4WepwcHS2fP8QhGsBxSz5YtgYobV7GGlWlAJi+RxfU77GQTQi2DSLUma42EYA==","fileCount":92,"unpackedSize":2215223,"attestations":{"url":"https://registry.npmjs.org/-/npm/v1/attestations/axios@1.21.0","provenance":{"predicateType":"https://slsa.dev/provenance/v1"}},"signatures":[{"keyid":"SHA256:DhQ8wR5APBvFHLF/+Tc+AYvPOdTpcIDqOhxsBHRwC7U","sig":"MEYCIQCYGPIXGWaJAgIlj3d2JSSnVkZ3y3UncUly+PcT47ncdAIhAPjlxghyUJkXHNNFHIqHOkm/QuTZNKl5YfwjPRjRtWpU"}]},"main":"./dist/node/axios.cjs","name":"axios","type":"module","types":"index.d.ts","unpkg":"dist/axios.min.js","author":{"name":"Matt Zabriskie"},"module":"./index.js","browser":{"./dist/node/axios.cjs":"./dist/browser/axios.cjs","./lib/adapters/http.js":"./lib/helpers/null.js","./lib/platform/node/index.js":"./lib/platform/browser/index.js","./lib/platform/node/classes/Buffer.js":"./lib/helpers/null.js","./lib/platform/node/classes/FormData.js":"./lib/helpers/null.js"},"exports":{".":{"bun":{"default":"./index.js","require":"./dist/node/axios.cjs"},"types":{"default":"./index.d.ts","require":"./index.d.cts"},"browser":{"default":"./index.js","require":"./dist/browser/axios.cjs"},"default":{"default":"./index.js","require":"./dist/node/axios.cjs"},"react-native":{"default":"./dist/esm/axios.js","require":"./dist/browser/axios.cjs"}},"./unsafe/*":"./lib/*","./package.json":"./package.json","./unsafe/utils.js":"./lib/utils.js","./dist/node/axios.cjs":"./dist/node/axios.cjs","./lib/adapters/xhr.js":"./lib/adapters/xhr.js","./lib/adapters/http.js":"./lib/adapters/http.js","./unsafe/core/settle.js":"./lib/core/settle.js","./dist/browser/axios.cjs":"./dist/browser/axios.cjs","./unsafe/adapters/xhr.js":"./lib/adapters/xhr.js","./unsafe/adapters/http.js":"./lib/adapters/http.js","./unsafe/helpers/buildURL.js":"./lib/helpers/buildURL.js","./unsafe/core/buildFullPath.js":"./lib/core/buildFullPath.js","./unsafe/helpers/combineURLs.js":"./lib/helpers/combineURLs.js","./unsafe/helpers/isAbsoluteURL.js":"./lib/helpers/isAbsoluteURL.js"},"gitHead":"aa54a5e1e0e50cd1a2561b854ae5490ff589d065","license":"MIT"
```

Raw contiguous fragment from the top-level `time` object (unchanged):

```text
"1.21.0":"2026-10-27T07:18:54.313Z"
```

### typescript

- Request: host `registry.npmjs.org`, path `/typescript`
- Full request URL: `https://registry.npmjs.org/typescript`
- Retrieved at (UTC): `2026-10-30T16:28:17.718170+00:00`

Raw contiguous fragment from `dist-tags` (unchanged):

```text
"dist-tags":{"dev":"3.9.4","tag-for-publishing-older-releases":"4.1.6","insiders":"4.6.2-insiders.20220225","rc":"7.0.1-rc","latest":"7.0.2",
```

Raw contiguous fragment from the latest version object through its `license` field (unchanged):

```text
"7.0.2":{"name":"typescript","version":"7.0.2","keywords":["TypeScript","Microsoft","compiler","language","javascript"],"author":{"name":"Microsoft Corp."},"license":"Apache-2.0"
```

Raw contiguous fragment from the top-level `time` object (unchanged):

```text
"7.0.2":"2026-07-08T15:55:18.431Z"
```

### svelte

- Request: host `registry.npmjs.org`, path `/svelte`
- Full request URL: `https://registry.npmjs.org/svelte`
- Retrieved at (UTC): `2026-10-30T16:28:22.438913+00:00`

Raw contiguous fragment from `dist-tags` (unchanged):

```text
"dist-tags":{"next":"5.0.0-next.272","latest":"5.57.3"}
```

Raw contiguous fragment from the latest version object through its `license` field (unchanged):

```text
"5.57.3":{"_id":"svelte@5.57.3","bugs":{"url":"https://github.com/sveltejs/svelte/issues"},"dist":{"shasum":"68cf74c2247a66d80af045ce07a20f8e04ace655","tarball":"https://registry.npmjs.org/svelte/-/svelte-5.57.3.tgz","fileCount":388,"integrity":"sha512-5mAftM3SoDV9X0zdF386F9p2pv8iKOwi/KfBS1XnBAkVCKFzVOLHUoa8iGWAt4buoicLmyWVRpuuD5wplXOQsg==","signatures":[{"sig":"MEYCIQDPPsWVpwEQuOBl2LdqycWO/SmRGDKGwEBgrtlL+NPqgQIhAJJAZxOkh1uTk5F0weszNY+yYMm5pwG+S6Tmj5Hu7nS/","keyid":"SHA256:DhQ8wR5APBvFHLF/+Tc+AYvPOdTpcIDqOhxsBHRwC7U"},{"keyid":"SHA256:DhQ8wR5APBvFHLF/+Tc+AYvPOdTpcIDqOhxsBHRwC7U","sig":"MEUCIQDoaVNwUsYl7FKY9t+quXDLSW8EU40vZifffSncd7TCoQIgFdcuPAYkhNlE0tNBVnUzq37ht60TY4ojSkrzxTV3GK0="}],"attestations":{"url":"https://registry.npmjs.org/-/npm/v1/attestations/svelte@5.57.3","provenance":{"predicateType":"https://slsa.dev/provenance/v1"}},"unpackedSize":2947315},"main":"src/index-client.js","name":"svelte","type":"module","_from":"file:svelte-5.57.3.tgz","types":"./types/index.d.ts","module":"src/index-client.js","engines":{"node":">=18"},"exports":{".":{"types":"./types/index.d.ts","worker":"./src/index-server.js","browser":"./src/index-client.js","default":"./src/index-server.js"},"./store":{"types":"./types/index.d.ts","worker":"./src/store/index-server.js","browser":"./src/store/index-client.js","default":"./src/store/index-server.js"},"./action":{"types":"./types/index.d.ts"},"./easing":{"types":"./types/index.d.ts","default":"./src/easing/index.js"},"./events":{"types":"./types/index.d.ts","default":"./src/events/index.js"},"./legacy":{"types":"./types/index.d.ts","worker":"./src/legacy/legacy-server.js","browser":"./src/legacy/legacy-client.js","default":"./src/legacy/legacy-server.js"},"./motion":{"types":"./types/index.d.ts","default":"./src/motion/index.js"},"./server":{"types":"./types/index.d.ts","default":"./src/server/index.js"},"./animate":{"types":"./types/index.d.ts","default":"./src/animate/index.js"},"./compiler":{"types":"./types/index.d.ts","default":"./src/compiler/index.js","require":"./compiler/index.js"},"./elements":{"types":"./elements.d.ts"},"./internal":{"default":"./src/internal/index.js"},"./reactivity":{"types":"./types/index.d.ts","worker":"./src/reactivity/index-server.js","browser":"./src/reactivity/index-client.js","default":"./src/reactivity/index-server.js"},"./transition":{"types":"./types/index.d.ts","default":"./src/transition/index.js"},"./attachments":{"types":"./types/index.d.ts","default":"./src/attachments/index.js"},"./package.json":"./package.json","./internal/client":{"default":"./src/internal/client/index.js"},"./internal/server":{"default":"./src/internal/server/index.js"},"./reactivity/window":{"types":"./types/index.d.ts","default":"./src/reactivity/window/index.js"},"./internal/flags/async":{"default":"./src/internal/flags/async.js"},"./internal/flags/legacy":{"default":"./src/internal/flags/legacy.js"},"./internal/flags/tracing":{"default":"./src/internal/flags/tracing.js"},"./internal/disclose-version":{"default":"./src/internal/disclose-version.js"}},"imports":{"#client":"./src/internal/client/types.d.ts","#server":"./src/internal/server/types.d.ts","#shared":"./src/internal/shared/types.d.ts","#compiler":{"types":"./src/compiler/private.d.ts","default":"./src/compiler/index.js"},"#client/constants":"./src/internal/client/constants.js","#compiler/builders":"./src/compiler/utils/builders.js"},"license":"MIT"
```

Raw contiguous fragment from the top-level `time` object (unchanged):

```text
"5.57.3":"2026-10-26T18:16:20.865Z"
```
