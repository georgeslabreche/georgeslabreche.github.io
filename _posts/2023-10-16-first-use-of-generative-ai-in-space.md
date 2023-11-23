---
title: "First Use of Generative AI in Space!"
excerpt: "We achieved the pioneering first application of Generative AI in space on September 29, 2023."
categories:
  - opssat
tags:
  - research
  - artificial intelligence
---

🤖 Generative AI... IN SPACE! 🌌 As the OPS-SAT-1 spacecraft's onboard camera 📷 surpasses its expected lifetime 👵🏼 it faces increased risk of picture degradation. So we came up with an innovative neural network solution!

We trained a Wasserstein GANs (WGANs) model to reconstruct degraded images directly onboard the spacecraft's edge computer payload 🛰️.

**On September 29, 2023, we achieved the pioneering first application of Generative AI in space**. 🎉

<div style="text-align:center;">
  <table align="center">
    <tr>
      <td><img src="/assets/images/posts/2023-10-16/First_Generative_AI_in_Space_1695963889066.jpeg" alt="Original Image 1" width="224"/></td>
      <td><img src="/assets/images/posts/2023-10-16/First_Generative_AI_in_Space_1695963889066.noised.jpeg" alt="Noised Image 1" width="224"/></td>
      <td><img src="/assets/images/posts/2023-10-16/First_Generative_AI_in_Space_1695963889066.denoised.jpeg" alt="Denoised Image 1" width="224"/></td>
    </tr>
    <tr>
      <td><figcaption>Original.</figcaption></td>
      <td><figcaption>Noised.</figcaption></td>
      <td><figcaption>Denoised.</figcaption></td>
    </tr>
  </table>
</div>

🎯 **Result:** Two images restored with impressive structural similarity indices (SSIM) of 0.89 & 0.92! Almost identical to the originals! 👏

✅ **Validation:** OPS-SAT-1 has an onboard CNN image classifier that failed to correctly identify the degraded images. However, post-denoising, the accuracy was restored and classification was a success. That's right — we leveraged existing onboard AI to verify the performance of our onboard AI! 🤯 #AIception.

🧠 **Bonus Observation:** Some reconstructed images were better recognized by the image classifier than their originals. This challenges the idea that higher resolution is always better, suggesting that sometimes simplifying data can boost accuracy!

🔜 **Next:** Keep an eye out for a forthcoming peer-reviewed IEEE publication that will be presented at AeroConf in March 2024. Meanwhile, do browse [the GitHub repo](https://github.com/georgeslabreche/opssat-onboard-image-denoiser).

<div style="text-align:center;">
  <table align="center">
    <tr>
      <td><img src="/assets/images/posts/2023-10-16/First_Generative_AI_in_Space_1695964476824.jpeg" alt="Original Image 2" width="224"/></td>
      <td><img src="/assets/images/posts/2023-10-16/First_Generative_AI_in_Space_1695964476824.noised.jpeg" alt="Noised Image 2" width="224"/></td>
      <td><img src="/assets/images/posts/2023-10-16/First_Generative_AI_in_Space_1695964476824.denoised.jpeg" alt="Denoised Image 2" width="224"/></td>
    </tr>
    <tr>
      <td><figcaption>Original.</figcaption></td>
      <td><figcaption>Noised.</figcaption></td>
      <td><figcaption>Denoised.</figcaption></td>
    </tr>
  </table>
</div>

Congratulations to my fellow co-researchers Cesar Guzman and Sam Bammens for their collaboration on this project. Stellar job, team! 🌟

*A version of this post was [first published on LinkedIn](https://www.linkedin.com/posts/georgeslabreche_aiception-aeroconf-europeanspaceagency-activity-7120045792790237184-TN2n/).*