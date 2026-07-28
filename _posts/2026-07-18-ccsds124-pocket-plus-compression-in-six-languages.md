---
title: "CCSDS 124.0-B-1: POCKET+ Compression in Six Languages"
excerpt: "Flight-proven on OPS-SAT-1, standardized by CCSDS, and now open-sourced in C, C++, Python, Go, Rust, and Java."
header:
  og_image: /assets/images/posts/2026-07-18/ccsds124-og.png
  overlay_image: /assets/images/posts/2020-08-30/Space_laboratory_sees_snowy_Svalbard.png
  caption: "[One of the first photos captured by OPS-SAT-1: snowy Svalbard](https://www.esa.int/ESA_Multimedia/Images/2020/08/Space_laboratory_sees_snowy_Svalbard)"
categories:
  - research
tags:
  - ccsds
  - opssat
  - research
  - compression
---

Hej folks! I developed and released open-source implementations of [CCSDS 124.0-B-1](https://ccsds.org/Pubs/124x0b1.pdf), the lossless compression standard for satellite housekeeping telemetry. They are MIT-licensed and available in six languages: C, C++, Python, Go, Rust, and Java. Check them out at [Tanagra Space](https://tanagraspace.com/ccsds124/).

### What is CCSDS 124.0-B-1?

Satellites continuously downlink housekeeping telemetry: fixed-length packets of parameters (e.g. temperatures, voltages, and status flags) that barely change from one packet to the next. The standard exploits that redundancy with nothing more than bitwise operations (OR, XOR, and AND), which makes it a good fit for constrained flight processors with real-time demands. It is based on POCKET+, an algorithm designed by the European Space Agency. I wrote about presenting our OPS-SAT-1 implementation at SmallSat 2022 in [an earlier post](/opssat/opssat-leop-commissioning-and-pocket+/).

### From OPS-SAT-1 to Standard

I implemented an earlier version in embedded C for the satellite's Nanomind 3200 flight computer when I was a spacecraft operations engineer with the European Space Agency's OPS-SAT-1 mission. We also ran it on the spacecraft's payload computer. Validating the algorithm and making it flight-proven was quite the adventure that led to its standardization by the Consultative Committee for Space Data Systems (CCSDS):

> Evans, D., Labrèche, G., Marszk, D., Bammens, S., Hernández-Cabronero, M., Zelenevskiy, V., Shiradhonkar, V., Starcik, M., & Henkel, M. (2022). Implementing the New CCSDS Housekeeping Data Compression Standard 124.0-B-1 (based on POCKET+) on OPS-SAT-1. *Proceedings of the 36th Annual Small Satellite Conference*. [https://digitalcommons.usu.edu/smallsat/2022/all2022/133/](https://digitalcommons.usu.edu/smallsat/2022/all2022/133/)

Releasing these implementations as open source for everyone is a fitting wrap-up to that adventure.

### Validation

Every implementation produces byte-identical output to the ESA reference implementation, passes the UAB/CNES cross-validation suite of 24,900 test vectors, and matches the other five languages bit for bit.

The C implementation is of particular interest for flight software because it is [MISRA-C:2012 compliant](https://github.com/tanagraspace/ccsds124/tree/main/implementations/c#misra-c2012-compliance). MISRA C is the de facto coding standard for safety-critical embedded systems, so the library steers clear of the undefined and error-prone corners of the C language. It is also embedded-friendly by design: C99 standard library only, no dependencies, and static allocation throughout, so no malloc and no free. There are no memory leaks: the test-vector, malformed-input, and robustness suites all pass [Valgrind](https://valgrind.org/) checks.

### Links

- [Project Page.](https://tanagraspace.com/ccsds124/)
- [GitHub Repository.](https://github.com/tanagraspace/ccsds124)
- [CCSDS 124.0-B-1 Standard.](https://ccsds.org/Pubs/124x0b1.pdf)
- [SmallSat 2022 Paper.](https://digitalcommons.usu.edu/smallsat/2022/all2022/133/)
