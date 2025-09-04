# Testing

This project uses [Molecule](https://molecule.readthedocs.io/) for testing Ansible roles and ansible-lint for code quality.

## Prerequisites

Create a virtual environment and install molecule and dependencies:
```bash
# Create and activate virtual environment
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install molecule ansible-core ansible-lint
```

**Note:** Remember to activate the virtual environment (`source venv/bin/activate`) before running tests in new terminal sessions.

## Running Tests

### Run all tests
```bash
# Lint the Ansible code
ansible-lint

# Run molecule tests
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

- **default**: Tests keybase role structure and task syntax using the delegated driver

The test verifies that:
1. All role files exist and are properly structured
2. The role tasks have valid syntax and can be imported
3. The role runs successfully in check mode

## Continuous Integration

The CI pipeline automatically runs:
- `ansible-lint` - Code quality and best practices validation
- `molecule test` - Role structure and syntax validation

## Local Development

To run the same checks that CI runs:

```bash
# Create and activate virtual environment
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install molecule ansible-core ansible-lint

# Run linting
ansible-lint

# Run molecule tests
molecule test
```

**Note:** Remember to activate the virtual environment (`source venv/bin/activate`) before running tests in new terminal sessions.