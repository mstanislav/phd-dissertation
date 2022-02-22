## Hardware Integrity (HW)

**HW-01:** The device features internal enhancements (e.g., epoxy, glue, shielding) that would visibly indicate potential physical tampering of hardware components.

- **Control Test:** If the device can be physically interacted with (e.g., dump flash chip) by an attacker without obvious physical intrusion, the device has failed this control.

**HW-02:** The device features a design (e.g., glued shell) or enhancements (e.g., tamper-evident stickers) that would indicate potential physical tampering of hardware components.

- **Control Test:** If the device can be opened by an attacker to expose internal components and sealed again without obvious physical intrusion, the device has failed this control.

**HW-03:** The device has a unique identifier (e.g., serial number) that is provided by the vendor during manufacturing that is able to be referenced for core operations (e.g., bootstrapping).

- **Control Test:** If the device does not provide a unique identifier that allows for physical association to a specific unit, the device has failed this control.

**HW-04:** The device has an FCC certification process performed for wireless functionality (e.g., Wi-Fi, Bluetooth) which ensures it is compliant to use within the United States.

- **Control Test:** If the device does not provide (e.g., box, shell) an FCC identifier, and one cannot be found (e.g., FCC search), the device has failed this control.

**HW-05:** The device utilizes a flash memory package that is less easily accessible (e.g., BGA) to an attacker with existing internal device access.

- **Control Test:** If a device utilizes a flash package that is easily accessible to an attacker with existing internal device access (e.g., SOIC), the device has failed the control.

## Local Access (LA)

**LA-01:** The device does not readily expose a UART that can readily provide a physical attacker with an ability to interact with the OS and/or bootloader of the device.

- **Control Test:** If the device exposes (e.g., pads, headers) a UART that could be accessed by an attacker to interact with the OS and/or bootloader, then the device has failed this control.

**LA-02:** The device, featuring a UART, does not provide an ability to interact with the bootloader in a manner that lets an attacker change bootloader without limitation (e.g., password).

- **Control Test:** If the device&#39;s UART provides access to a bootloader without mitigation that can allow for an attacker to manipulate settings, the device has failed this control.
- **Dependency:** LA-01

**LA-03:** The device, featuring a UART, does not provide an ability to login directly to the OS from that interface with credentials, if known or discoverable to the attacker.

- **Control Test:** If the device&#39;s UART provides a login interface that would allow an attacker to provide credentials to gain a shell on the system, the device has failed the control.
- **Dependency:** LA-01

**LA-04:** The device, featuring a UART, does not provide an automatic shell -- with no credentials provided -- that could be used by an attacker to directly interact with the OS.

- **Control Test:** If the device&#39;s UART provides a direct, unauthenticated system shell to an attacker, the device has failed the control.
- **Dependency:** LA-01

**LA-05:** The device, featuring a UART, does not provide output that contains sensitive information (e.g., Wi-Fi settings, cloud service tokens) about the device&#39;s configuration.

- **Control Test:** If the device&#39;s UART shows sensitive data that could be valuable to attacker from merely observing the UART&#39;s output, the device has failed the control.
- **Dependency:** LA-01


## Mobile Security (MS)

**MS-01:** The device&#39;s associated mobile application protects sensitive data (e.g., Wi-Fi settings) in files and databases that are not cleartext (e.g., encrypted database strings).

- **Control Test:** If a device&#39;s mobile application stores sensitive data in a manner that allows an attacker to readily read its contents, the device has failed the control.

**MS-02:** The device&#39;s associated mobile application protects network connection (e.g., APIs) via a method (e.g., certificate pinning) that prevents an attacker from readily intercepting traffic.

- **Control Test:** If a device&#39;s mobile application can have its network connections intercepted on an attacker-controlled device with a proxy configuration, the device has failed the control.

**MS-03:** The device&#39;s associated mobile application provides notification (and/or prevents usage) if that mobile device has indications that it has been &quot;rooted&quot; or &quot;jail broken.&quot;

- **Control Test:** If a device&#39;s mobile application can be rooted or jail broken without the end-user being notified (and/or prevented) prior to its usage, the device has failed the control.

**MS-04:** The device&#39;s associated mobile application provides a cloud service that enforces a well-defined password policy to limit insecure password selection by end-users.

- **Control Test:** If a device&#39;s mobile application does not enforce a well-defined password policy requirement with its related cloud service, the device has failed the control.

**MS-05:** The device&#39;s associated mobile application provides a cloud service that supports a second step of authentication, beyond only a password.

- **Control Test:** If a device&#39;s mobile application does not allow an end-user to configure a second step of authentication with its related cloud service, the device has failed the control.

**MS-06:** The device&#39;s associated mobile application provides a cloud service that requires a second step of authentication, beyond only a password.

- **Control Test:** If a device&#39;s mobile application does not require an end-user to configure a second step of authentication with its related cloud service, the device has failed the control.
- **Dependency:** MS-05

**MS-07:** The device&#39;s associated mobile application uses encrypted traffic (e.g., HTTPS) for API calls or similar network connectivity with any associated cloud services.

- **Control Test:** If a device&#39;s mobile application does not use encrypted transports for APIs or similar network connectivity with cloud services, the device has failed the control.

## Wi-Fi Security (WF)

**WF-01:** The device&#39;s configuration of Wi-Fi for use in an end-user&#39;s network does not allow the usage of Wi-Fi Protected Setup (WPS) due to known security design flaws in the protocol.

- **Control Test:** If a device supports the usage of WPS to configure Wi-Fi for connecting to an end-user&#39;s network, the device has failed the control.

**WF-02:** The device&#39;s configuration of Wi-Fi allows the use of Wi-Fi Protected Access 3 (WPA 3) when the relevant network supports the protocol itself.

- **Control Test:** If a device does not support the use of WPA 3 to connect to an end-user&#39;s network that supports the WPA 3 protocol, the device has failed the control.

**WF-03:** The device&#39;s configuration of Wi-Fi for use in an end-user&#39;s network does not allow a temporary Wi-Fi network to be created on the device, limiting potential attack surface.

- **Control Test:** If a device allows the creation of a temporary Wi-Fi network to connect to an end-user&#39;s network as a supported setup option, the device has failed the control.

**WF-04:** The device, supporting a temporary Wi-Fi network for configuration, requires a password to connect to that temporary network for the setup process to occur.

- **Control Test:** If a device, supporting a temporary Wi-Fi network for configuration, does not require a password to connect to that network, the device has failed the control.
- **Dependency:** WF-03

## Service Security (SS)

**SS-01:** The device does not run a hosted web server that is network accessible (beyond localhost) that may support device management, streaming, or other features.

- **Control Test:** If a device hosts a local web server that is network accessible, the device has failed the control.

**SS-02:** The device, running a local web server that is network accessible, uses only encrypted transports (e.g., HTTPS) to handle all inbound traffic to its functionality.

- **Control Test:** If a device, running a local web server that is network accessible, does not encrypt traffic for its functionality, the device has failed the control.
- **Dependency:** SS-01

**SS-03:** The device, running a local web server that is network accessible, performs an authentication process before commands will be allowed to service endpoints.

- **Control Test:** If a device, running a local web server that is network accessible, does not require authentication before commands are allowed, the device has failed the control.
- **Dependency:** SS-01

**SS-04:** The device is not running a File Transfer Protocol (FTP), Secure File Transfer Protocol (SFTP), or other inbound file transfer service during its normal operation.

- **Control Test:** If a device is running an inbound file transfer service during its normal operation, the device has failed the control.

**SS-05:** The device is not running a Secure Shell (SSH), Telnet, or other inbound remote access service during its normal operation.

- **Control Test:** If a device is running an inbound remote access service during its normal operation, the device has failed the control.

**SS-06:** The device is not running a local streaming service (e.g., RTSP) in its default configuration (i.e. without explicit user permission).

- **Control Test:** If a device is running a local streaming service in its default configuration, the device has failed the control.

**SS-07:** The device, running a local streaming service, encrypts the transmission of all video and/or audio.

- **Control Test:** If a device, running a local streaming service, does not encrypt all video and/or audio, the device has failed the control.
- **Dependency:** SS-06

**SS-08:** The device, running a local streaming service, requires authentication to access video and/or audio.

- **Control Test:** If a device, running a local streaming service, does not require authentication before video and/or audio can be accessed, the device has failed the control.
- **Dependency:** SS-06

**SS-09:** The device implements a host-based firewall (e.g., iptables) to limit ingress and/or egress traffic.

- **Control Test:** If a device does not implement a host-based firewall to limit ingress and/or egress traffic, the device has failed the control.

**SS-10:** The device is configured to prevent automatic IP forwarding from one network interface to another.

- **Control Test:** If a device has IP forwarding enabled, the device has failed the control.

**SS-11:** The device, leveraging MQ Telemetry Transport (MQTT) for its operation, encrypts the transmission of all messages between the device and the external MQTT service.

- **Control Test:** If a device, leveraging MQTT service for its operation, does not encrypt transmissions between the device and the external service, the device has failed the control.

## Hardware Security (HS)

**HS-01:** The device&#39;s hardware supports Secure Boot as part of its shipped components (e.g., SoC).

- **Control Test:** If a device&#39;s hardware does not provide support for Secure Boot functionality, the device has failed the control.

**HS-02:** The device&#39;s hardware, supporting Secure Boot functionality, uses that as part of standard operation.

- **Control Test:** If a device&#39;s hardware, supporting Secure Boot functionality, does not leverage that as part of standard operation, the device has failed the control.
- **Dependency:** HS-01

**HS-03:** The device&#39;s hardware supports cryptographic operations via a provided security engine as part of its shipped components (e.g., SoC).

- **Control Test:** If a device&#39;s hardware does not provide a security engine that supports cryptographic operations, the device has failed the control.

**HS-04:** The device&#39;s hardware supports random number generation operations via a provided security engine as part of its shipped components (e.g., SoC).

- **Control Test:** If a device&#39;s hardware does not provide a security engine that supports random number generation operations, the device has failed the control.

## Firmware Updates (FW)

**FW-01:** The device supports a documented approach for end-users and/or the vendor to update the running firmware on the device.

- **Control Test:** If a device&#39;s firmware is unable to be updated through a documented approach by end-users and/or the vendor, the device has failed the control.

**FW-02:** The device, supporting a documented approach to update firmware, notifies the end-user that a new firmware update is available when using the associated mobile application.

- **Control Test:** If a device, supporting a documented approach to firmware updates, does not notify an end-user when a new firmware update is available, the device has failed the control.
- **Dependency:** FW-01

**FW-03:** The device, supporting a documented approach to update firmware, requires new firmware to be installed before the device can be used by the end-user.

- **Control Test:** If a device, supporting a documented approach to firmware updates, does not require new firmware updates to be installed before use, the device has failed the control.
- **Dependency:** FW-01

**FW-04:** The device, supporting a documented approach to update firmware, allows an end-user to request checking for new firmware updates in the associated mobile application.

- **Control Test:** If a device, supporting a documented approach to firmware updates, does not allow an end-user to check for firmware updates, the device has failed the control.
- **Dependency:** FW-01

**FW-05:** The device, supporting a documented approach to update firmware, transports that firmware via an encrypted transport (e.g., HTTPS), even if the firmware is encrypted itself.

- **Control Test:** If a device, supporting a documented approach to firmware updates, does not transport firmware updates via an encrypted transport, the device has failed the control.
- **Dependency:** FW-01

**FW-06:** The device, supporting a documented approach to update firmware, does not provide a direct method for an end-user to upload their own firmware image.

- **Control Test:** If a device, supporting a documented approach to firmware updates, provides a direct method for an end-user to upload firmware, the device has failed the control.
- **Dependency:** FW-01

**FW-07:** The device, supporting a documented approach to update firmware, performs a validation that transmitted firmware matches an expected cryptographic hash before installation.

- **Control Test:** If a device, supporting a documented approach to firmware updates, installs transmitted firmware without verifying a cryptographic hash, the device has failed the control.
- **Dependency:** FW-01

**FW-08:** The device, supporting a documented approach to update firmware, performs a digital signature verification tied to the vendor for a transmitted firmware image before installation.

- **Control Test:** If a device, supporting a documented approach to firmware updates, installs a transmitted firmware image without verifying a signature, the device has failed the control.
- **Dependency:** FW-01

## End-user Privacy (EP)

**EP-01:** The device provides a documented method to physically reset the system to a factory-default state, suitable for re-configuration by a new owner (or disposal).

- **Control Test:** If a device does not provide a documented, physical method to perform a factory-reset of the system, the device has failed the control.

**EP-02:** The device, when performing a documented method to physically reset the system to a factory-default state, removes all sensitive data (e.g., Wi-Fi configuration) from the device.

- **Control Test:** If a device, when performing a vendor-documented method to physically reset the system, does not delete all sensitive data, the device has failed the control.
- **Dependency:** EP-01

**EP-03:** The device, when supporting external media (e.g., Micro SD) and performing a documented method to physically reset the device to a default state, deletes all files from the media.

- **Control Test:** If a device, performing a documented method to physically reset the system, does not delete all files from external media, the device has failed the control.
- **Dependency:** EP-01

**EP-04:** The device, when supporting external media (e.g., Micro SD), performs a method of obfuscation or encryption that limits casual viewing of recordings stored on the external media.

- **Control Test:** If a device, supporting external media, does not prevent casual viewing of the recordings on that media, the device has failed the control.

**EP-05:** The device provides a physical indication (e.g., illuminated LED) that the camera is currently streaming video to a mobile application or a direct method (e.g., RTSP).

- **Control Test:** If a device does not provide a physical indication that a video stream is occurring when accessed with a supported method, the device has failed the control.

**EP-06:** The device&#39;s filesystem is encrypted-at-rest in a manner that prevents an attacker with physical access to its flash memory from recovering the contents of that device.

- **Control Test:** If a device does not encrypt its filesystem in a manner that prevents an attacker with physical access from recovering its contents, the device has failed the control.

## Binary Hardening (BH)

**BH-01:** The device has implemented at least partial Relocation Read-Only (RELRO), determined by evaluating a relevant system binary as a representitive sample.

- **Control Test:** If a device has not implemented at least partial RELRO, determined by evaluating a relevant system binary, the device has failed the control.

**BH-02:** The device has implemented stack canaries, determined by evaluating a relevant system binary as a representitive sample.

- **Control Test:** If a device has not implemented stack canaries, determined by evaluating a relevant system binary, the device has failed the control.

**BH-03:** The device has implemented a non-executable (NX) memory regions, determined by evaluating a relevant system binary as a representitive sample.

- **Control Test:** If a device has not implemented NX memory regions, determined by evaluating a relevant system binary, the device has failed the control.

**BH-04:** The device has implemented Position Independent Executables (PIE), determined by evaluating a relevant system binary as a representitive sample.

- **Control Test:** If a device has not implemented PIE, determined by evaluating a relevant system binary, the device has failed the control.

**BH-05:** The device has removed debugging symbols, determined by evaluating a relevant system binary as a representitive sample.

- **Control Test:** If a device has not removed debugging symbols, determined by evaluating a relevant system binary, the device has failed the control.

**BH-06:** The device has implemented Fortify Source, determined by evaluating a relevant system binary as a representitive sample.

- **Control Test:** If a device has not implemented Fortify Source, determined by evaluating a relevant system binary, the device has failed the control.

## Linux Hardening (LH)

**LH-01:** The device has implemented control groups (cgroups) for at least some contexts.

- **Control Test:** If the device does not implement cgroups for at least some contexts, the device has failed this control.

**LH-02:** The device has implemented seccomp-bpf in a manner that adds protection to core system services.

- **Control Test:** If the device does not implement seccomp-bpf in a manner that adds protection to core system services, the device has failed the control.

**LH-03:** The device has implemented mandatory access controls (MAC) (e.g., SELinux, AppAromor) in a manner that adds protection to core system services.

- **Control Test:** If the device does not implement MAC in a manner that adds protection to core system services, the device has failed the control.

**LH-04:** The device has appropriately configured discetionary access controls (DAC) in a manner that limits file access to specific system services and users (e.g., not over-using root).

- **Control Test:** If the device does not implement DAC in a manner that limits file access to specific system services and users, the device has failed the control.

**LH-05:** The device generally executes system processes and services in a manner that leverages users with less privilege than root, either directly or via privilege separation.

- **Control Test:** If the device does not generally execute system processes and services in a manner that leverages users with less privilege than root, the device has failed the control.

**LH-06:** The device does not contain OS-level account passwords either in a default or hardcoded form, including blank passwords.

- **Control Test:** If the device contains OS-level account passwords either in a default or hardcoded form, including blank passwords, the device has failed the control.

**LH-07:** The device, if it contains OS-level account passwords either in a default or hardcoded form, store those passwords in a format other than md5crypt or descrypt.

- **Control Test:** If the device, containing OS-level account passwords, stores those passwords with md5crypt or descrypt, the device has failed the control.
- **Dependency:** LH-06

**LH-08:** The device&#39;s installed kernel is built from an actively maintained code train.

- **Control Test:** If the device has a kernel that is built from an unmaintained code train, the device has failed the control.

**LH-09:** The device&#39;s installed kernel modules supporting core functionality are digitally signed.

- **Control Test:** If the device has kernel modules providing core functionality that are not digitally signed, the device has failed the control.

**LH-10:** The device has at least partial enablement for Address Space Layout Randomization (ASLR).

- **Control Test:** If the device does not have at least partial ASLR enabled, the device has failed the control.