# Testing

This project uses Ansible's built-in syntax checking and linting for testing.

## Prerequisites

Install ansible-core and ansible-lint:
```bash
pip install ansible-core ansible-lint
```

## Running Tests

### Run all tests
```bash
# Lint the Ansible code
ansible-lint

# Check playbook syntax
ansible-playbook --syntax-check playbook.yml
```

### Continuous Integration

The CI pipeline runs:
1. **Ansible Lint** - Checks code quality and best practices
2. **Syntax Check** - Validates playbook syntax

## Test Coverage

The tests verify that:
1. All Ansible code follows best practices (via ansible-lint)
2. Playbook syntax is valid (via syntax check)
3. Role structure is correct

## Local Development

To run the same checks that CI runs:

```bash
# Install dependencies
pip install ansible-core ansible-lint

# Run linting
ansible-lint

# Check syntax
ansible-playbook --syntax-check playbook.yml
```