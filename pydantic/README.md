# Everything about Pydantic

This is the course about Pydantic in Udemy
```
https://nisum.udemy.com/course/pydantic/learn/lecture/41126002#overview
```

**Github link**
```
https://github.com/fbaptiste/pydantic-essentials
```
## 1. Overview

**enums**

**properties/cached properties**

**composition**

**dataclasses**

**model basics**
- required vs optional field 
- nullable fields
- type coersion
- basic validation

**model configuration**
- extra fields
- lax vs strict type coercion
- validating defaults and assignements

**Field Aliases**
- manual specification
- auto-generated aliases

**Specialized Pydantic Types with Validations**
- constrained numbers
- constrained lists
- dates and times
- URL types

**Additional Field configurations**
- Constraints 
- mutable defaults
- default factories

**Serialization and Deserialization**
- ignored fields 
- aliases
- validation and serialization aliases

**Annotated Types**
- Python
- Pydantic
- Leveraging Generics

**Custome validators**
- Before and after validators
- Decorator approach
- Annotated approach
- Combining multiple before and after validators
- Dependent Field Validators
- Sequence Type Validators
- Modifying data via Validators

**Computed Fields**

**Complex models**
- inheritance
- composition

**Practical examples**
- Consuming REST API JSON data
- loading csv data
- validating Python function arguments
- using model code generators
- How fastAPI leverage pydantic



## 2. Basics

**Pydantic model**

**Deserialization**

**Serialization**

**Type Coersion**

**Required vs optional fields**

**Nullable fields**

**Inspecting fields**

**JSON schema generation**

## 3. Model configuration

**Handling Extra fields**

**Strict vs Lax Type Coersion**

**Validating default values**

**Validating assignments**

**Mutability**

**Coercing number to string**

**Standardizing strings**

**Handling Python nums**

## 4. Field Aliasing, Serialization and Deserialization

**Field Aliases and Default values**

**Alias Generator Functions**

**Deserializing by Field Name or Alias**

**Serialization Aliases**

**Validation Aliases**

## 5. Specialized Pydantic Types

**PositiveInt**

**Constrained Lists**

**UUID**

**Date Related Types**

**Network Types**

## 6. Additional Field Features
Field
**Numerial Field Constraints**

**String Constraints**

**Default Factories**

**Additional Field Configurations**
- Frozen
- default 
- exclude

## 7. Annotated Types

**Annotated Types**
With Annotated, you can create reusable constrained types

**Type variables**
Define a generic placeholder that can later be bound to any type.

**String Constraints**
- To lower
- min/max length
- strip_whitespace 
...


