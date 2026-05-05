## Requirements

```bash
nix shell nixpkgs#just nixpkgs#jq github:pinpox/pgp2ssh github:serokell/deploy-rs
```

## CLI Guide

### General

Start the common development environment:
```bash
just dev
```

### Configuration Management

Update the `sing-box` configurations:
```bash
just update-configs
```

Convert a PEM certificate to a JSON-escaped string (useful for embedding in sing-box config):
```bash
jq -Rs '.' cert.crt
```

### System & Deployment

Rebuild the local system configuration:
```bash
just rebuild-sys
```

Deploy the configuration to the NixOS server:
```bash
just deploy-server
```

## References

- [dev_flake](https://github.com/magic0whi/dev_flake)
- [sing-box-subscribe](https://github.com/Toperlock/sing-box-subscribe)
- [nix-darwin](https://github.com/nix-darwin/nix-darwin)
- [just](https://github.com/casey/just)
- [deploy-rs](https://github.com/serokell/deploy-rs)

## Acknowledgements

I gratefully acknowledge chezmoi's powerful templating and field-level encryption capabilities, which make it possible to securely manage and publicize these configurations.

- [KeePassXC](https://keepassxc.org/)
- [chezmoi](https://www.chezmoi.io/)
