# reysys-technology/homebrew-tap

This tap currently publishes no casks.

## rscli

The `rscli` casks were removed on 2026-09-07. Every one of them pinned version
1.0.3 or older and pointed at release assets in a repository that is no longer
public, so `brew install` had been failing with a 404 for some time.

rscli 1.0.3 is withdrawn and must not be installed. It disables TLS certificate
verification, it reads `config.yaml` from the working directory, and it cannot
authenticate against the current API. If a machine still has it, remove it and
rotate any client secret it held:

```
brew uninstall --cask rscli
```

For current installation instructions see https://docs.reysys.com/docs/version-1.2.0/installation
