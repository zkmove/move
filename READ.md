# Move VM with Witness Generation

This is a fork of the Move VM with support for execution witness generation.
When running a Move entry function, the VM can record a structured
trace of all executed bytecode operations and serialize it as JSON.

## Install

```bash
cargo install --git https://github.com/zkmove/move move-cli
```

## Usage

Use the `--witness` (or `-w`) flag with `move run` to generate a witness file:

```bash
move sandbox run <module> <function> --witness
```

The witness will be saved as a timestamped JSON file under the `witnesses/` directory.
