# Macro Pad 23
This is the ZMK config for the Macro Pad 23. It is a 23-switch macropad compatible with Xiao-based boards.

## Building locally

1. Install the local zephyr and ZMK toolchain as described in the [ZMK docs](https://zmk.dev/docs/development/local-toolchain/setup/native).
4. Clone the repo:
    ```
    https://github.com/Smartich0ke/macropad-23
    ```
3. Step into the zmk app directory installed in step 1:
    ```
    cd zmk/app
    ```
5. Run `west build` as follows, making sure to replace the `ZMK_CONFIG` and `ZMK_EXTRA_MODULES` path with the path to where you cloned this repo. For more info on this see [Building With External Modules](https://zmk.dev/docs/development/local-toolchain/build-flash#building-with-external-modules).
    ```
    west build -b seeeduino_xiao_ble \
    -- -DSHIELD=macropad_23sw \
    -DZMK_CONFIG="/path/to/macropad-23" \
    -DZMK_EXTRA_MODULES="/path/to/macropad-23"
    ```
6. The compiled uf2 will be located at `zmk/app/build/zephyr/zmk.uf2`.