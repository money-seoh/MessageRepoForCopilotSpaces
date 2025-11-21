# Message Format Specification

## UserEntity Message Structure

### Syntax
```
UserEntity(Operation(<OP>),OperDate(<FIELDS>))
```

### Operations
- `ADD`: Create new user
- `UPDATE`: Update existing record of user entity

### Mandatory Fields
- `FirstName(value)` - User's first name
- `LastName(value)` - User's last name  
- `UserName(value)` - Unique username

### Optional Fields
- `Address(street, city, country)` - User's address (comma-separated)
- `Address(,,)` - User's address (optional comma-separated values)

### Examples

**Mandatory only:**
```
UserEntity(Operation(ADD),OperDate(FirstName(John),LastName(Doe),UserName(johndoe1)))
```

**With optional address:**
```
UserEntity(Operation(ADD),OperDate(FirstName(John),LastName(Doe),UserName(johndoe2),Address(SampleAddress, ExampleCity, Country)))
```

### Validation Rules
1. UserName must be unique
2. All mandatory fields required for ADD operation
3. Address must have exactly 3 comma-separated values
4. No nested parentheses within field values