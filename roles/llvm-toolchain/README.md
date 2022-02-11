# miso-robotics.general.llvm-toolchain

Install the LLVM toolchain from official sources.

## Requirements

None.

## Role Variables

**llvm_version**: Version of LLVM to install.

- `"latest"`
- `"14"`
- `"13"`

**llvm_packages**: List of LLVM packages to install. A version postfix is
added if not using latest.

- `"clang"`
- `"clang-format"`
- `"clang-tidy"`

## Dependencies

None.

## Example Playbook

Set up latest LLVM toolchain sources and install some basic packages:

```yaml
- hosts: servers
  roles:
    - role: misorobotics.general.llvm-toolchain:
      vars:
        llvm_packages:
          - clang
          - clang-format
          - clang-tidy
```

## License

MIT
