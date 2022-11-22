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
| `1` `1.23` `1.23.2` `1.23.2-r0` `latest` `mainline` | `sha256:d45f84da2db52c2f330b75df7f01bbcfe44acab4a381a826e38901c72b73338c`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:d45f84da2db52c2f330b75df7f01bbcfe44acab4a381a826e38901c72b73338c) | `amd64` `arm64` `armv7` |
| `1.22` `1.22.1` `1.22.1-r0` `stable` `stable-20221122` | `sha256:080eb857f9df02d7e550a531694d7d8d142ce0e0c0457ada48d11b1015214f50`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:080eb857f9df02d7e550a531694d7d8d142ce0e0c0457ada48d11b1015214f50) | `amd64` `arm64` `armv7` |
| `stable-20221121` | `sha256:ab103cb6f31f219f27fd8e258e39890b5bdc83728c4b0c48006817174adb1def`<br/>[View entry in Rekor](https://rekor.tlog.dev/?hash=sha256:ab103cb6f31f219f27fd8e258e39890b5bdc83728c4b0c48006817174adb1def) | `amd64` `arm64` `armv7` |


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
        "docker-manifest-digest": "sha256:d45f84da2db52c2f330b75df7f01bbcfe44acab4a381a826e38901c72b73338c"
      },
      "type": "cosign container image signature"
    },
    "optional": {
      "1.3.6.1.4.1.57264.1.1": "https://token.actions.githubusercontent.com",
      "1.3.6.1.4.1.57264.1.2": "schedule",
      "1.3.6.1.4.1.57264.1.3": "b9ae3a093e6c8e6daee6d22d75d8ff57afae59e6",
      "1.3.6.1.4.1.57264.1.4": "Create Release",
      "1.3.6.1.4.1.57264.1.5": "chainguard-images/nginx",
      "1.3.6.1.4.1.57264.1.6": "refs/heads/main",
      "Bundle": {
        "SignedEntryTimestamp": "MEUCIQCFgEayHzigPDViNulavp/ZHufKedF6HavjkBzOL5sOvgIgDA+xBB9zdC54+W87H3UpQZ1AV93et5M7lNh2A4DNFdM=",
        "Payload": {
          "body": "eyJhcGlWZXJzaW9uIjoiMC4wLjEiLCJraW5kIjoiaGFzaGVkcmVrb3JkIiwic3BlYyI6eyJkYXRhIjp7Imhhc2giOnsiYWxnb3JpdGhtIjoic2hhMjU2IiwidmFsdWUiOiJhYmFkNzMzNjQzM2M5YjIzYTQwMWMxN2FlZDZkN2U4NDAyMmJiMjBmMjg0ZjdmNDE1ZTlkMjkxMjlmMzdiZGFmIn19LCJzaWduYXR1cmUiOnsiY29udGVudCI6Ik1FWUNJUURxeWRmWURHY2tKeW5QdWI3TG1jNVJvUStBMmFGL3ZwMXY3ajRuRDdteStRSWhBTlo4WC9XWW5Ncyttd1BDRkFZY21OQ0VvdEYrV0k0dktMYTZhYUtxQkhTZiIsInB1YmxpY0tleSI6eyJjb250ZW50IjoiTFMwdExTMUNSVWRKVGlCRFJWSlVTVVpKUTBGVVJTMHRMUzB0Q2sxSlNVUnhha05EUVhwRFowRjNTVUpCWjBsVlF5dGFaMGxHSzJwT1NsQlJVbWhqYkUxbk9VdDRXV1Y2VEhSQmQwTm5XVWxMYjFwSmVtb3dSVUYzVFhjS1RucEZWazFDVFVkQk1WVkZRMmhOVFdNeWJHNWpNMUoyWTIxVmRWcEhWakpOVWpSM1NFRlpSRlpSVVVSRmVGWjZZVmRrZW1SSE9YbGFVekZ3WW01U2JBcGpiVEZzV2tkc2FHUkhWWGRJYUdOT1RXcEplRTFVU1hsTlJFRjVUbnBOTVZkb1kwNU5ha2w0VFZSSmVVMUVRWHBPZWsweFYycEJRVTFHYTNkRmQxbElDa3R2V2tsNmFqQkRRVkZaU1V0dldrbDZhakJFUVZGalJGRm5RVVZFV0V4d1QxUnRLMjVzTmpFclowOTRSRWw2TjBKTmNEaDVjRXM1YzFWNmVraFlRMk1LUW01dmNIcHpNMEZvU1dnek1GVnlVbXRaTTBWMlIwNTVjWEpIWkdaVFdYQkpjREZTYmpad09TdHdTWHBpTlhCSE0zRlBRMEZyT0hkblowcE1UVUUwUndwQk1WVmtSSGRGUWk5M1VVVkJkMGxJWjBSQlZFSm5UbFpJVTFWRlJFUkJTMEpuWjNKQ1owVkdRbEZqUkVGNlFXUkNaMDVXU0ZFMFJVWm5VVlU1WWtWUENrTlpiVTVMTWs0M1NXeDFiM1JPUTNObGNITnphVFZuZDBoM1dVUldVakJxUWtKbmQwWnZRVlV6T1ZCd2VqRlphMFZhWWpWeFRtcHdTMFpYYVhocE5Ga0tXa1E0ZDFwM1dVUldVakJTUVZGSUwwSkdNSGRYTkZwYVlVaFNNR05JVFRaTWVUbHVZVmhTYjJSWFNYVlpNamwwVERKT2IxbFhiSFZhTTFab1kyMVJkQXBoVnpGb1dqSldla3d5Tlc1aFZ6VTBUSGsxYm1GWVVtOWtWMGwyWkRJNWVXRXlXbk5pTTJSNlRETktiR0pIVm1oak1sVjFaVmRHZEdKRlFubGFWMXA2Q2t3eWFHeFpWMUo2VERJeGFHRlhOSGRQVVZsTFMzZFpRa0pCUjBSMmVrRkNRVkZSY21GSVVqQmpTRTAyVEhrNU1HSXlkR3hpYVRWb1dUTlNjR0l5TlhvS1RHMWtjR1JIYURGWmJsWjZXbGhLYW1JeU5UQmFWelV3VEcxT2RtSlVRVmRDWjI5eVFtZEZSVUZaVHk5TlFVVkRRa0ZvZWxreWFHeGFTRlp6V2xSQk1ncENaMjl5UW1kRlJVRlpUeTlOUVVWRVFrTm9hVTlYUm14Tk1rVjNUMVJPYkU1dFRUUmFWRnByV1ZkV2JFNXRVWGxOYlZFelRsZFJORnB0V1RGT01rWnRDbGxYVlRGUFYxVXlUVUozUjBOcGMwZEJVVkZDWnpjNGQwRlJVVVZFYTA1NVdsZEdNRnBUUWxOYVYzaHNXVmhPYkUxRFZVZERhWE5IUVZGUlFtYzNPSGNLUVZGVlJVWXlUbTlaVjJ4MVdqTldhR050VVhSaFZ6Rm9XakpXZWt3eU5XNWhWelUwVFVJd1IwTnBjMGRCVVZGQ1p6YzRkMEZSV1VWRU0wcHNXbTVOZGdwaFIxWm9Xa2hOZG1KWFJuQmlha05DYVhkWlMwdDNXVUpDUVVoWFpWRkpSVUZuVWpsQ1NITkJaVkZDTTBGT01EbE5SM0pIZUhoRmVWbDRhMlZJU214dUNrNTNTMmxUYkRZME0ycDVkQzgwWlV0amIwRjJTMlUyVDBGQlFVSm9TbmszY1dGRlFVRkJVVVJCUldkM1VtZEphRUZRVWtRNWVGUk5hRGhzVEdSSU1GRUtUV2N5UTNack1IVjRVVFV6Y0Zaa2NtRlRUa0ZTUkdSTGVYZEJSa0ZwUlVGdWFrUmlOMnhIUm5Zd04yWXpTbGRLTmxRdmFYWkRVMHhzYjB4UlNuUXdhUXBxZGtSdVJIbEpaRWhTYjNkRFoxbEpTMjlhU1hwcU1FVkJkMDFFWVVGQmQxcFJTWGhCVG1Fck9FZFNMMVF6Tkd4dVFWcDNTMWR1YVVwUVJHNUxObko0Q21ndkswdGtVR3BETW1sQ2VVTTRlRlZ1V1Vzd1ZETTJXa1o1Wms5dVIyTkhNa05CVERCUlNYZGpPRGx6VldoV2FqVkJkVm92VkZKU2RXRldlRlZUTTBvS05VRmxRVk5oU2pCUlYybEJiVlpNV1M5clNYQkZObmgyUWpSTFl5czNRV3A1WTNBd1VYRlpXZ290TFMwdExVVk9SQ0JEUlZKVVNVWkpRMEZVUlMwdExTMHRDZz09In19fX0=",
          "integratedTime": 1669076863,
          "logIndex": 7577174,
          "logID": "c0d23d6ad406973f9559f3ba2d1ca01f84147d8ffc5b8445c224f98b9591801d"
        }
      },
      "Issuer": "https://token.actions.githubusercontent.com",
      "Subject": "https://github.com/chainguard-images/nginx/.github/workflows/release.yaml@refs/heads/main",
      "githubWorkflowName": "Create Release",
      "githubWorkflowRef": "refs/heads/main",
      "githubWorkflowRepository": "chainguard-images/nginx",
      "githubWorkflowSha": "b9ae3a093e6c8e6daee6d22d75d8ff57afae59e6",
      "githubWorkflowTrigger": "schedule",
      "run_attempt": "1",
      "run_id": "3519177141",
      "sha": "b9ae3a093e6c8e6daee6d22d75d8ff57afae59e6"
    }
  }
]
```

You can verify that the image was built in Github Actions in this repository from the `Issuer` and `Subject` fields.
</details>

## Build

This image is built with [apko](https://github.com/chainguard-dev/apko).

