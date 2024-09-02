
# FIDO2 Authentication

## Demonstration

The following screencast demonstrates authentaction to [webauthn.io](https://webauthn.io/) using [FIDO Bridge](../components/fido-bridge/index.md), [Bridge Controller](../components/bridge-controller/index.md) and [FIDO2 standard](https://fidoalliance.org/fido2/).

<figure class="video_container">
  <video controls="true" allowfullscreen="true">
    <source src="../../assets/videos/fido-webauthnio.mp4" type="video/mp4">
  </video>
</figure>

## Minimal Requirements

1. [FIDO Bridge](../components/fido-bridge/index.md)
2. [Bridge Controller](../components/bridge-controller/index.md)
2. [MeeSign Server](https://meesign.crocs.fi.muni.cz/)
3. [MeeSign Clients](https://meesign.crocs.fi.muni.cz/)

## Tutorial

1. Launch [Bridge Controller](../components/bridge-controller/index.md).
2. Select the FIDO interface from the interface menu, and enable and configure it.
3. Once the configuration is applied, the application attaches a virtual FIDO2-compatible device that is available to all applications. You can detach the device by disabling the interface in the [Bridge Controller](../components/bridge-controller/index.md) menu.

!!! warning "Warning"
    Bridge controller requires passwordless sudo configuration to attach the USB/IP virtual device. This will be solved in the future by writing proper udev rules.
