# nginx

<!---
Note: Do NOT edit directly, this file was generated using https://github.com/chainguard-images/readme-generator
-->

[![CI status](https://github.com/chainguard-images/nginx/actions/workflows/release.yaml/badge.svg)](https://github.com/chainguard-images/nginx/actions/workflows/release.yaml)

A minimal nginx base image rebuilt every night from source.

## Get It!

The image is available on `cgr.dev`:

```
docker pull cgr.dev/chainguard/nginx:latest
```

## Supported tags

| Tag | Digest | Arch |
| --- | ------ | ---- |
| `1.22` `1.22.1` `1.22.1-r0` `stable` `stable-20221126` | `sha256:58bea545504f59c72dcafd4f175c96b9b8937290fc7e3505f19ad2f091fe67ab`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:58bea545504f59c72dcafd4f175c96b9b8937290fc7e3505f19ad2f091fe67ab) | `amd64` `arm64` `armv7` |
| `stable-20221121` | `sha256:ab103cb6f31f219f27fd8e258e39890b5bdc83728c4b0c48006817174adb1def`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:ab103cb6f31f219f27fd8e258e39890b5bdc83728c4b0c48006817174adb1def) | `amd64` `arm64` `armv7` |
| `stable-20221122` | `sha256:080eb857f9df02d7e550a531694d7d8d142ce0e0c0457ada48d11b1015214f50`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:080eb857f9df02d7e550a531694d7d8d142ce0e0c0457ada48d11b1015214f50) | `amd64` `arm64` `armv7` |
| `stable-20221123` | `sha256:a5877507195df004f410b73acaf385769948df8e9277606f6cb0da9eae77e7d4`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:a5877507195df004f410b73acaf385769948df8e9277606f6cb0da9eae77e7d4) | `amd64` `arm64` `armv7` |
| `stable-20221124` | `sha256:77b88bc8c23da889b617ef1eaac7d22b6b04f04b96f353efd2749c9d92f35b26`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:77b88bc8c23da889b617ef1eaac7d22b6b04f04b96f353efd2749c9d92f35b26) | `amd64` `arm64` `armv7` |
| `stable-20221125` | `sha256:32ce35c568cf3ccac91dc1834624881b0d528482ea93566230a12424344f372c`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:32ce35c568cf3ccac91dc1834624881b0d528482ea93566230a12424344f372c) | `amd64` `arm64` `armv7` |
| `1` `1.23` `1.23.2` `1.23.2-r0` `latest` `mainline` | `sha256:d730f74c479b834f7bedf388b13eb16b6b52e8b69d9d1a2bcbef15c9c9746f21`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:d730f74c479b834f7bedf388b13eb16b6b52e8b69d9d1a2bcbef15c9c9746f21) | `amd64` `arm64` `armv7` |


## Usage

To try out the image, run:

```
docker run -p 8080:80 cgr.dev/chainguard/nginx
```

If you navigate to `localhost:8080`, you should see the nginx welcome page.

To run an example Hello World app, navigate to the root of this repo and run:

```
docker run -v $(pwd)/examples/hello-world/site-content:/var/lib/nginx/html -p 8080:80 cgr.dev/chainguard/nginx
```

If you navigate to `localhost:8080`, you should see `Hello World from Nginx!`.



## Signing

All Chainguard Images are signed using [Sigstore](https://sigstore.dev)!

<details>
<br/>
To verify the image, download <a href="https://github.com/sigstore/cosign">cosign</a> and run:

```
COSIGN_EXPERIMENTAL=1 cosign verify cgr.dev/chainguard/nginx:latest | jq
```

Output:
```
Verification for cgr.dev/chainguard/nginx:latest --
The following checks were performed on each of these signatures:
  - The cosign claims were validated
  - Existence of the claims in the transparency log was verified offline
  - Any certificates were verified against the Fulcio roots.
[
  {
    "critical": {
      "identity": {
        "docker-reference": "ghcr.io/chainguard-images/nginx"
      },
      "image": {
        "docker-manifest-digest": "sha256:d730f74c479b834f7bedf388b13eb16b6b52e8b69d9d1a2bcbef15c9c9746f21"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "c6466853ee51dc6555624638cee0bd4cb1058a69",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/nginx",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEUCIQC66XLt4SaZWr2tNtT/ouEPRHtqJtDQ5o7r6DHyofYpogIgQD4gt+g8DLpvgZYowF9HLbCzpC6HNrcwqxD9nmbD/Eo=",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiJhMWY5ODBmNzk4MmI3MzQzMTcwNzBhMWE1NjYxODE1OTIxODdlYjJhYjlkOTQxMTAyYWNkYmM5NTI2M2M5YTlhIn19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FVUNJUUQwNmVrdERHeEtQSGJFVXhWakRaNDFMNURMM0JySEFnSGpYa3RLWXM1WjZnSWdYcEVtSFhHTFNkaGM2S1ZHbUtqdVpPcGlxVlM5a29XVld6LzROakxDc3BZPSIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUnhWRU5EUVhwRFowRjNTVUpCWjBsVlJHaEtVMFJoTkhwTVNqbENkM2hQZWs0ck4xRmFOREEyVFRSTmQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFVU1RKTlJFRjVUMVJKZDFkb1kwNU5ha2w0VFZSSk1rMUVRWHBQVkVsM1YycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVZMUTBoQlFVWndTemN6VTFkbGVIcGtUbVJQWms1MldFdHZNRTUxYlVwbWREVlBZbkVLYzFwVVF6YzJRakZ1WWtSd2RXcDJRbGt3Um5OclVVWnpLMVE0UXpKQldub3lNbGwyYW1GSlZuSTBabnB5YW1oNFIwdFBRMEZyT0hkblowcE1UVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlYyUmpObkNqVkRiM05RYlV4aEsydzBiUzlqU2tGWmNHMTJhMmxaZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDFwM1dVUldVakJTUVZGSUwwSkdNSGRYTkZwYVlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d5Tlc1aFZ6VTBUSGsxYm1GWVVtOWtWMGwyWkRJNWVXRXlXbk5pTTJSNlRETktiR0pIVm1oak1sVjFaVmRHZEdKRlFubGFWMXA2Q2t3eWFHeFpWMUo2VERJeGFHRlhOSGRQVVZsTFMzZFpRa0pCUjBSMmVrRkNRVkZSY21GSVVqQmpTRTAyVEhrNU1HSXlkR3hpYVRWb1dUTlNjR0l5TlhvS1RHMWtjR1JIYURGWmJsWjZXbGhLYW1JeU5UQmFWelV3VEcxT2RtSlVRVmRDWjI5eVFtZEZSVUZaVHk5TlFVVkRRa0ZvZWxreWFHeGFTRlp6V2xSQk1ncENaMjl5UW1kRlJVRlpUeTlOUVVWRVFrTm9hazVxVVRKT2FtY3hUVEpXYkU1VVJtdFplbGt4VGxSVk1rMXFVVEpOZW1ocVdsZFZkMWx0VVRCWk1rbDRDazFFVlRSWlZGazFUVUozUjBOcGMwZEJVVkZDWnpjNGQwRlJVVVZFYTA1NVdsZEdNRnBUUWxOYVYzaHNXVmhPYkUxRFZVZERhWE5IUVZGUlFtYzNPSGNLUVZGVlJVWXlUbTlaVjJ4MVdqTldhR050VVhSaFZ6Rm9XakpXZWt3eU5XNWhWelUwVFVJd1IwTnBjMGRCVVZGQ1p6YzRkMEZSV1VWRU0wcHNXbTVOZGdwaFIxWm9Xa2hOZG1KWFJuQmlha05DYVhkWlMwdDNXVUpDUVVoWFpWRkpSVUZuVWpsQ1NITkJaVkZDTTBGT01EbE5SM0pIZUhoRmVWbDRhMlZJU214dUNrNTNTMmxUYkRZME0ycDVkQzgwWlV0amIwRjJTMlUyVDBGQlFVSm9URVpYY3pORlFVRkJVVVJCUldkM1VtZEphRUZLVFRCMFRXVmlOM2h5V2s5VmREVUtSR2NyVERaVlVrWTBVSE53WkdaelQycElLMWw1VGpkcmFYVlZNMEZwUlVFclVISnhOek5EVURCV1dETmFObTlUZGxwTlN6aDJOMmQ1U1VsNFNDdHNLd3BxYkdzelFUQmpSWEZqWTNkRFoxbEpTMjlhU1hwcU1FVkJkMDFFV25kQmQxcEJTWGREV1RSUGExUXhORGwxTm05RE5EZFVhaXQwY0hkbGVETXhaSE56Q21velJFZFBVbXMzZUV3M1dGTjViMDlSU1ZOT1UwUXZOek0xTVdZM1lUWjFVWEZpYjBGcVFXaFpOM1paZEcxQ2VqUXhTMGQzYjBaTWRIQnNPVVJEVERNS1RWTjZla2wzUVZCUVF6UlNZbVpoTWtoRFYzbEVXRVpsY1hJM2NXRTRXVk5uWXpsdFNEaFJQUW90TFMwdExVVk9SQ0JEUlZKVVNVWkpRMEZVUlMwdExTMHRDZz09In19fX0=",
          "integratedTime": 1669422568,
          "logIndex": 7857955,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/nginx/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/nginx",
      "githubWorkflowSha": "c6466853ee51dc6555624638cee0bd4cb1058a69",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3551375896",
      "sha": "c6466853ee51dc6555624638cee0bd4cb1058a69"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [apko](https://github.com/chainguard-dev/apko).

