## Remote attestation（RA）

 Remote attestation is a challenge-response protocol between a client (Prover) and a remote host (Verifier) for reporting Prover’s hardware and software configuration (e.g., the internal state of RAM, flash, etc.) to the host. Typically, Verifier initiates the protocol by sending a challenge to a Prover, which needs to measure its own integrity and create a fresh and authentic evidence of being in a trustworthy state. The process of integrity measurement may vary, for instance, it may involve computing an encryption-based MAC or a keyed hash over its memory , or randomly placed verification bits. Such an evidence is then transmitted to Verifier, who is assumed to know all possible reference measurement(s) for Prover that correspond to Prover’s valid (i.e, good or safe) state(s).

![An example of RA protocol ](./images/ra.png)

 Prover is assumed to have a trust anchor, which makes sure that the integrity measurement is taken and reported correctly, even if the platform is compromised. The trust anchor helps to establish protected resources (memory, processor, RAM) exclusively for attestation purposes, and, thus, one can say that it divides the Prover ’s platform into a secure and nonsecure worlds. While the latter holds general-purpose code (application/service specific), the secure world is used to safeguard attestation key(s) in protected memory, store and run an immutable RA code securely and atomically. The two parts of the device communicate through a secure gateway.
 
Based on a way used to establish a trust anchor on a computing platform, RA schemes can be roughly divided into three categories: 
1. software-based,
2. hardware-based, 
3. and hybrid.
 
`Hardware-based solutions` rely on dedicated (optionally, tamper-resistant) hardware components, such as Trusted Platform Module (TPM),Intel SGX or ARM TrustZone to provide a Root-of-Trust (RoT). All services and information provided by RoT can be considered reliable, and thereby secrets like cryptographic keys can be stored
 securely. RA schemes that leverage hardware-based trust an chors provide highest security guarantees among all the categories, but require specific hardware for Prover’s platforms, which may or may not be available in practice.
 
 `Software-based schemes` impose no assumptions on underlying hardware. Consequently, there cannot be any secrets securely stored on Prover. As a workaround, these schemes use side-channel information (e.g., precise timing of execution of certain algorithms) to detect malicious behavior. This makes software-based schemes applicable to, and appealing for, legacy devices. However, they rely on strong as
sumptions, e.g., Prover must be directly connected to Verifier.
This greatly limits their applicability.
 
`Hybrid schemes` blend software and hardware features to achieve RA while aiming to minimize requirements on underlying hardware. They provide much stronger security guarantees than software-based schemes, while requiring only minimal security features in hardware (such as Read Only Memory (ROM) and Memory Protection Unit (MPU) for secure storage), which are readily available on many platforms.


## Hardware-based solutions


## Software-based schemes
* From Interaction to Independence: zkSNARKs for Transparent and Non-Interactive Remote Attestation Shahriar Ebrahimi,  Parisa Hassanizadeh, [Paper](https://github.com/zero-savvy/zk-remote-attestation/blob/master/doc/NDSS24.pdf), NDSS 2024

## Hybrid schemes
