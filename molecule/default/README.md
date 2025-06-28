# Molecule Testing

This directory contains Molecule configuration for testing the ansible-fio role.

## Test Platforms

- Debian 12 (Bookworm)
- Ubuntu 20.04 (Focal)
- Ubuntu 22.04 (Jammy)
- Ubuntu 24.04 (Noble)
- Fedora 42 (Latest)
- Rocky Linux 9
- AlmaLinux 9
- Enterprise Linux 10

## Running Tests

### Prerequisites

```bash
pip install molecule[docker] docker ansible
```

### Run Tests

```bash
# Run full test suite
molecule test

# Test individual steps
molecule create
molecule converge
molecule verify
molecule destroy
```

## Test Structure

- `molecule.yml`: Main configuration
- `converge.yml`: Playbook that applies the role
- `verify.yml`: Verification tests that ensure FIO is working