# Software Requirements

## qat_hw Requirements
Successful operation of QAT Hardware acceleration requires a software tool chain
that supports OpenSSL\* 1.1.1 or OpenSSL\* 3.0 or BoringSSL\* and Intel&reg; QuickAssist
Technology Driver for Linux or Intel&reg;  QuickAssist Technology
Driver for FreeBSD. This release was validated on the following:

* Operating system: CentOS* 8.4, Ubuntu\* 20.04.2 LTS & FreeBSD\* 12.3
* Intel&reg; QuickAssist Technology Driver for Linux\* HW Version 2.0 - **QAT20.L.1.0.10-00005**
* Intel&reg; QuickAssist Technology Driver for Linux\* HW Version 1.7 & 1.8 - **QAT.L.4.20.0-00001**
* Intel&reg; QuickAssist Technology Driver for FreeBSD\* HW Version 1.7 - **QAT.B.3.12.0-00004**
* OpenSSL\* 1.1.1t & 3.0.8
* BoringSSL\* commit - [987dff1][1]
* BabaSSL - 8.3.2

## qat_sw Requirements
Successful operation of the Intel&reg; QAT Software acceleration requires a
software tool chain that supports OpenSSL\* 1.1.1 or OpenSSL\* 3.0 and Intel&reg;
Crypto Multi-buffer library(for Asymmetric PKE) cloned from the [ipp-crypto][2] repo.
The crypto_mb library needs to be installed using the instructions from the
[Crypto Multi-buffer Library][3] Readme.

For QAT SW AES-GCM acceleration, prequisite is to have Intel&reg;
Multi-Buffer crypto for IPsec Library cloned from the [intel-ipsec-mb][4]
repo and installed using the instructions from the intel-ipsec-mb README.
The Intel&reg; QAT Engine supports QAT SW AES-GCM from OpenSSL\* 1.1.1d.

This release was validated on the following:

* Operating system: Ubuntu\* 20.04.2 LTS
* Intel&reg; Crypto Multi-buffer library from the [ipp-crypto][2] release
  version **IPP Crypto 2021.7.1**
* Intel&reg; Multi-Buffer crypto for IPsec Library release version **v1.3**
* OpenSSL\* 1.1.1t & 3.0.8
* BoringSSL\* commit - [987dff1][1]
* BabaSSL - 8.3.2

--------------------------------------------------------------------------------

Note : OpenSSL\* Version 1.1.1 will be EOL from Sep'23 for general use hence
QAT Engine(qat_hw & qat_sw) is also planning to drop the support for OpenSSL\*
1.1.1 after the OpenSSL\* 1.1.1 EOL.

--------------------------------------------------------------------------------

[1]:https://github.com/google/boringssl/commit/987dff1a9fa953a8c7dffa369d78caae02b8d9ab
[2]:https://github.com/intel/ipp-crypto
[3]:https://github.com/intel/ipp-crypto/tree/develop/sources/ippcp/crypto_mb
[4]:https://github.com/intel/intel-ipsec-mb
