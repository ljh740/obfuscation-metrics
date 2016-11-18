# Processes and Metrics for Assessing Obfuscation Effectiveness

The Mobile Application Security Verification Standard (MASVS) is a standard for mobile app security. It is meant to be used by mobile software architects and developers seeking to develop secure mobile applications and as a basis for mobile app security testing methodologies. The MASVS lists requirements for both security controls and software protection mechanisms, and defines four verification levels that can be applied to achieve different grades of security and resiliency.

Level 4 of the MASVS requires the use of hardware-based isolation features, such as SEE or TEE. However, as specialized hardware is not always available, it allows for strong software protection and obfuscation as a substitute. The software protection requirements are listed in MASVS V8 - "Resiliency Against Reverse Engineering":

- **V8.16: Verify that sensitive computations take place in a trusted environment that is isolated from the mobile operating system. Hardware-based SE or TEE should be used whenever available.**

- **V8.17: If hardware-based isolation is unavailable, verify that a strong form of obfuscation has been applied to isolate sensitive data and computations, and verify the robustness of the obfuscation.**

Obfuscation is a controversial topic however, and there is currently no industry standard defining *strong* obfuscation. The goal of this project is to find workable solutions to this problem. It aims to achieve the following:

* List obfuscation methods that are considered *good enough* to stand in for dedicated crypto hardware.

* For each obfuscation method, determine a list of minimum requirements to be fulfilled, such as:

	* White-box must be resilient against DFA

* For each obfuscation method, determine measurable properties such as:

	* Minimum algorithmic complexity of virtual machine interpreter
	* Minimum size/complexity of lookup tables in white-box crypto

* Outline a *practical* verification process that can be used by mobile appsec experts in planning and white-box testing.

## Threat Model

Before we attempt to define requirements and metrics, we need to know what we are actually defending against. By obfuscating code and data, we aim to increase the effort adversaries need to invest to achieve certain goals. The following table states a threat model that looks at the obfuscated app from the attacker's perspective.

|Adversary's goal|Example|Counter-measure|
|---|---|---|
|Todo|todo|todo|

## Metrics
- [Kolmogorov Complexity](https://github.com/b-mueller/obfuscation-metrics/blob/master/02a_kolmogorov_complexity.md)
- [Normalized Compression Distance](https://github.com/b-mueller/obfuscation-metrics/blob/master/02b_normalized_compression_distance.md)

## Practical Obfuscation Effectiveness

## Transformations

### Control flow obfuscation

### Data obfuscation

### Virtualization

### White-box cryptography

## Sample Programs

- [OATH-TOTP](https://github.com/b-mueller/obfuscation-metrics/tree/master/testprograms/oath-totp)
