# Molecule Testing

This project uses [Molecule](https://molecule.readthedocs.io/) for testing Ansible roles.

## Prerequisites

1. Install molecule and dependencies:
```bash
pip install molecule[docker] molecule-docker ansible-lint
```

2. Install required Ansible collections:
```bash
ansible-galaxy collection install -r molecule/requirements.yml
```

3. Ensure Docker is running on your system

## Running Tests

### Run all tests
```bash
molecule test
```

### Run individual steps
```bash
# Check syntax only
molecule syntax

# Create test environment
molecule create

# Run the role
molecule converge

# Verify installation
molecule verify

# Clean up
molecule destroy
```

## Test Scenarios

- **default**: Tests keybase installation on Ubuntu 20.04 Docker container

The test verifies that:
1. The keybase role runs successfully
2. The keybase command is available after installation