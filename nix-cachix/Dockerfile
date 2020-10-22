FROM nixos/nix

RUN nix-channel --add \
  https://nixos.org/channels/nixpkgs-unstable nixpkgs && \
  nix-channel --update

RUN \
  nix-env -iA cachix -f https://cachix.org/api/v1/install && \
  nix-env -i bash google-cloud-sdk git && \
  nix-collect-garbage -d

ENTRYPOINT "bash"
