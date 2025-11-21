# Message Repository for Copilot Spaces

## Overview
This repository contains message templates and specifications for the UserEntity messaging system. It's designed to work with GitHub Copilot Spaces to parse, validate, and generate structured messages.

## Repository Structure

- **Messages/**: Template files for different message types
- **Schemas/**: JSON schema definitions for validation
- **.github/**: Copilot Space configuration and instructions
- **message-spec.md**: Human-readable message format documentation
- **Examples/**: Sample generated messages

## Usage with Copilot Space

### Quick Start
1. Open this repository in GitHub Copilot Space
2. Ask: "Create new user message having address"
3. Copilot will read templates and generate a valid message

### Sample Prompts
- "Create new user message having address"
- "Generate ADD operation for user Jane Smith with address"
- "Create user message without optional fields"
- "Generate 3 user messages with different addresses"

## Message Format

### UserEntity ADD Operation
```
UserEntity(Operation(ADD),OperDate(FirstName(value),LastName(value),UserName(value),Address(street, city, country)))
```
- **Address** is an optional field.

See `message-spec.md` for complete specification.

## Extending This Repository

### Adding New Entities
1. Create folder in `Messages/`
2. Add template files
3. Update `copilot-instructions.md`

### Adding Operations
1. Update schema with new operation type
2. Add template examples
3. Document in `message-spec.md`
