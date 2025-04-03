# Endgame

Attempting to make a ZMK firmware module for [the Endgame2024 keyboard by oldman6955](https://github.com/OldMan6955/TheEndgame2024).

## Instructions

To your west.yml, add:

```yaml
manifest:
  remotes:
    [...]
    - name: evantravers
      url-base: https://github.com/evantravers
  projects:
    [...]
    - name: zmk-keyboard-endgame
      remote: evantravers
      revision: main
```

Now you can add to your build.yml:

```yaml
- board: sparkfun_pro_micro_rp2040
  shield: endgame
```

And you can build a keymap in your zmk-config as you would for any keyboard.
