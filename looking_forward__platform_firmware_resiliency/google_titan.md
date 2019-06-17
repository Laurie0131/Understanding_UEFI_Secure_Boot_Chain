## Google Titan {#google-titan}

Google developed [Titan](https://cloud.google.com/blog/products/gcp/titan-in-depth-security-in-plaintext) as a hardware root-of-trust solution for [Google Cloud Platform](https://cloud.google.com/) (GCP). Aside from basic secure boot, Titan implements remediation and first-instruction integrity. These features are like functions found in Intel Boot Guard and Project Cerberus.

_“Trust can be re-established through remediation in the event that bugs in Titan firmware are found and patched, and first-instruction integrity allows the platform to identify the earliest code that runs on each machine’s startup cycle.”_

_-- “[Titan in depth: Security in plaintext](https://cloud.google.com/blog/products/gcp/titan-in-depth-security-in-plaintext)” (cloud.google.com)_

Figure 4-10 shows the Titan System Integration diagram. Figure 4-11 shows the Titan Verified Boot flow.

![](media/image24.png)

Figure 4-10: Titan System Integration (source: “[Titan silicon root of trust for Google Cloud](https://keystone-enclave.org/workshop-website-2018/slides/Scott_Google_Titan.pdf)”)

![](media/image25.png)

Figure 4-11: Titan Verified Boot(source: “[Titan silicon root of trust for Google Cloud](https://keystone-enclave.org/workshop-website-2018/slides/Scott_Google_Titan.pdf)”)