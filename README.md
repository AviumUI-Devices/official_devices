# AviumUI Official Device and Maintainer Policy

This document defines the baseline technical requirements, maintainer responsibilities,
and review principles for AviumUI official devices, in order to ensure stability,
security, and long-term maintainability of the project.

---

## 1. Scope

This policy applies to **all AviumUI official devices and their maintainers**.

---

## 2. Maintainer Requirements

### 2.1 Physical Device Ownership and Responsibility

- Maintainers must physically own and actively use the device they maintain  
- Blind or untested builds are not allowed for official releases  
- If maintaining multiple devices with minimal hardware differences, at least one
  of them must be physically owned and actively maintained  

---

### 2.2 Basic Technical Competency

Maintainers are **not required to develop complex features**, but must demonstrate:

- Basic code reading ability  
- Basic problem investigation and self-debugging skills  

Maintainers should be able to independently locate and understand existing code,
configurations, or documentation within the project repositories, and apply
necessary updates accordingly, rather than relying entirely on step-by-step guidance.

---

### 2.3 Prior Maintenance Experience

- Before applying for official status, the device should be maintained unofficially
  for a reasonable period of time  
- Submitting a single build and immediately applying for official status will not
  be considered sufficient maintenance experience  

---

## 3. Contributions and Commit Practices

### 3.1 Contribution Scope

Maintainer contributions may span multiple areas, including but not limited to:

- Device tree repositories  
- Common device trees  
- Kernel repositories  
- Other platform-related components  

> Contributions in device-specific repositories alone are not the sole metric
> for evaluating maintenance capability.

---

### 3.2 Commit Authorship and Attribution

- All commits submitted to official repositories must accurately reflect the actual
  authorship of the code  
- If the submitter is not the original author, proper authorship must be clearly
  stated in the commit message  

Any form of misleading, impersonated, or concealed authorship is not permitted.

---

## 4. Official Repository Hosting

- Once a device is approved as an AviumUI official device, its corresponding device
  tree repository **must be hosted under the AviumUI GitHub organization**  

---

## 5. Official Device Technical Requirements

### 5.1 Security and System Integrity

- Official devices must not use `RemovePackages` or similar mechanisms to remove or
  alter core system components  
- Official release builds must enforce **SELinux Enforcing**  
- Bypassing or ignoring SELinux security rules (such as using
  `IGNORE_SELINUX_NEVERALLOWS`) is not allowed  

---

### 5.2 Build Requirements

- Official release builds must be on **`user` build type**  
- Official releases must generate standard **target-files** build artifacts  

---

### 5.3 Root and Privileged Solutions

- Official release builds **must not ship with** KernelSU, Magisk, or any other
  root or privilege-escalation solutions pre-integrated  
- The decision to obtain root access must be left entirely to the end user  

---

## 6. Official Communication Language

- Commit messages, code comments, and technical discussions related to official
  devices and repositories must be conducted in English  

---

## 7. Review Authority and Project Discretion

- Official device reviews and maintenance are conducted based on this policy and
  the maintainer’s demonstrated ability to sustain the device  
- The project reserves the right to adjust the official status of any device at
  any stage  
- The project also reserves final discretion over maintainer applications and
  official device approval  

---

## 8. Miscellaneous

- This policy may be updated as the project evolves
