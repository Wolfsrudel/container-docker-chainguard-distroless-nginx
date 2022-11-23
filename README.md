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
| `1` `1.23` `1.23.2` `1.23.2-r0` `latest` `mainline` | `sha256:7c83f12de51aa6fa2366db6314900ab2ae5660604d37b368c6767b71868e1757`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:7c83f12de51aa6fa2366db6314900ab2ae5660604d37b368c6767b71868e1757) | `amd64` `arm64` `armv7` |
| `1.22` `1.22.1` `1.22.1-r0` `stable` `stable-20221123` | `sha256:a5877507195df004f410b73acaf385769948df8e9277606f6cb0da9eae77e7d4`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:a5877507195df004f410b73acaf385769948df8e9277606f6cb0da9eae77e7d4) | `amd64` `arm64` `armv7` |
| `stable-20221121` | `sha256:ab103cb6f31f219f27fd8e258e39890b5bdc83728c4b0c48006817174adb1def`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:ab103cb6f31f219f27fd8e258e39890b5bdc83728c4b0c48006817174adb1def) | `amd64` `arm64` `armv7` |
| `stable-20221122` | `sha256:080eb857f9df02d7e550a531694d7d8d142ce0e0c0457ada48d11b1015214f50`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:080eb857f9df02d7e550a531694d7d8d142ce0e0c0457ada48d11b1015214f50) | `amd64` `arm64` `armv7` |


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
        "docker-manifest-digest": "sha256:7c83f12de51aa6fa2366db6314900ab2ae5660604d37b368c6767b71868e1757"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "90f5a92a0b2d6b29cb50d5b3a753c4b4a6003c1b",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/nginx",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEQCIF9qXu+52/ZInlY2sKPCsuqK6VZStAIIcl+mcXzwc9aZAiAxKSTwA+3Ssx8jEI+fBoHV1kpkHc5S+i62Aqb7YFRN+A==",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiIwNGRjYmNhNGFjMWYwZjQ5YTVlY2Q1MzM3MzI2N2NlOWM1NGRkMWZmMWMxZTdmMTE4Yjk0MDQyYWNmZWZkZjg1In19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FVUNJRkFSeHFDcjh2WkE5Ti9Rdkd0VktzU0RXeStsT01ITXdGbnFVUnBPY2dxbUFpRUE5cGl0c0pnR1IrSyt1RVNvQVR3QXMzd3IwbFFTTWNqL3NFMGx4c2Q1TFpNPSIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUnhSRU5EUVhrMlowRjNTVUpCWjBsVlpIVmtaVk5qYW5GeFNIUm9Ta3ByTXpGTlptNWtPVmQzWkdzd2QwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFVU1hwTlJFRjVUbnBCTlZkb1kwNU5ha2w0VFZSSmVrMUVRWHBPZWtFMVYycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVUyVlhCRlVqWnBaekkyYjFCVFFUTnBVRkl5Y1hvMVNuTnFaakI0UVhWSlVHVkNNVzhLVW04eVlrb3pNMDh4WjIxSWRUZGhZbEJFYlZaUVRIZDNWMjh5Um1Kb1VWUk1MMDAwYVhSSFIyVm9VSEl4UmpKS04zRlBRMEZyTUhkblowcEtUVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlZLTXk4dkNrRkVRWEZJUVVWYWJtSldZazlvYnpSRlIzQldiRFZaZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDFwM1dVUldVakJTUVZGSUwwSkdNSGRYTkZwYVlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d5Tlc1aFZ6VTBUSGsxYm1GWVVtOWtWMGwyWkRJNWVXRXlXbk5pTTJSNlRETktiR0pIVm1oak1sVjFaVmRHZEdKRlFubGFWMXA2Q2t3eWFHeFpWMUo2VERJeGFHRlhOSGRQVVZsTFMzZFpRa0pCUjBSMmVrRkNRVkZSY21GSVVqQmpTRTAyVEhrNU1HSXlkR3hpYVRWb1dUTlNjR0l5TlhvS1RHMWtjR1JIYURGWmJsWjZXbGhLYW1JeU5UQmFWelV3VEcxT2RtSlVRVmRDWjI5eVFtZEZSVUZaVHk5TlFVVkRRa0ZvZWxreWFHeGFTRlp6V2xSQk1ncENaMjl5UW1kRlJVRlpUeTlOUVVWRVFrTm5OVTFIV1RGWlZHdDVXVlJDYVUxdFVUSlpha2sxV1RKSk1VMUhVVEZaYWs1b1RucFZlbGw2VW1sT1IwVXlDazFFUVhwWmVrWnBUVUozUjBOcGMwZEJVVkZDWnpjNGQwRlJVVVZFYTA1NVdsZEdNRnBUUWxOYVYzaHNXVmhPYkUxRFZVZERhWE5IUVZGUlFtYzNPSGNLUVZGVlJVWXlUbTlaVjJ4MVdqTldhR050VVhSaFZ6Rm9XakpXZWt3eU5XNWhWelUwVFVJd1IwTnBjMGRCVVZGQ1p6YzRkMEZSV1VWRU0wcHNXbTVOZGdwaFIxWm9Xa2hOZG1KWFJuQmlha05DYVZGWlMwdDNXVUpDUVVoWFpWRkpSVUZuVWpkQ1NHdEJaSGRDTVVGT01EbE5SM0pIZUhoRmVWbDRhMlZJU214dUNrNTNTMmxUYkRZME0ycDVkQzgwWlV0amIwRjJTMlUyVDBGQlFVSm9TMGhvYjJkM1FVRkJVVVJCUlZsM1VrRkpaMEZNTkVGb09USjZjRzByTlVJeVJHRUtLemN2ZG5Od2FsbGFVWGRuVUd0RmRtdEhOVTlsVW5odWVUbE5RMGxCZFdnMlEwdHhTVFl4VERCcFp6ZDBLMlY2V2toeWNsWllSMVpWVTJ0WVNVVm1XQXBCT1VaMWFsQXhSRTFCYjBkRFEzRkhVMDAwT1VKQlRVUkJNbWRCVFVkVlEwMUNhemxvWlVoaVRsRkZTblZXU1doNGMxaDRUVFZVVUdONGIzaFVWbEpwQ21ORE1VNDFORU42UVV4VlNVUTBTblZWTlZKb1MxTldSbTVDY0dZMWNYVTFjR2RKZUVGTmRtWkNWMkZ6Tm5WWFpXWmpkV1ZCWTBOSFdGbEhjaTlCWXlzS0wwTTFlbGRMVVhrdlFscGtRMWwzUWt3MloxSnNXWEJTYkRoalFuTTFiVFJKWjBWVWRHYzlQUW90TFMwdExVVk9SQ0JEUlZKVVNVWkpRMEZVUlMwdExTMHRDZz09In19fX0=",
          "integratedTime": 1669163240,
          "logIndex": 7652601,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/nginx/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/nginx",
      "githubWorkflowSha": "90f5a92a0b2d6b29cb50d5b3a753c4b4a6003c1b",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3528109240",
      "sha": "90f5a92a0b2d6b29cb50d5b3a753c4b4a6003c1b"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [apko](https://github.com/chainguard-dev/apko).

