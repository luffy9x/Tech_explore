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


## 8. Custom Validators
- Before validators : “clean up or normalize” data.
- After validators : “enforce business logic”
### After validators
It alway run from first to last :
- after_validator_1()
- after_validator_2()
- after_validator_3()

### Before validators
It alway run from last to first:
- before_validator_3()
- before_validator_2()
- before_validator_1()

### Combining before and after validators

### Custom Validators using Annotated Types

## Dependent Field Validators
- In Pydantic v2, they’re done with @model_validator.
- They let you enforce rules where one field depends on another.
- Example: end_date must be after start_date, or password_confirm must match password.

## 9. Properties and Computed Fields
**Properties**
- It's a function where you can access like an attribute and the calculation in the function is made on-the-fly
**Cached_properties**
- It's like Properties but it has the cached feature, you don't have to recaculate again. But you need to make sure that all the attribute which gonna be used in the calculation, is "frozen".
- You can not "set" the property, only "get"

**Computed Fields**

- A computed field in Pydantic is a special kind of field that is calculated from other fields but is also treated like a real field when you export or serialize your model (.model_dump(), .model_dump_json()). It’s basically a property that shows up in .dict()/.json()
- You can do 'alias' with "computed Fields"

## 10. Custom Serializers using Annotated Types

In Pydantic v2, you can control how fields are serialized (exported via .model_dump() or .model_dump_json()) by attaching a serializer function using **Annotated** + **PlainSerializer**. This lets you separate input validation from output representation.

Why use this?
- Security → mask passwords, tokens, sensitive fields.
- Formatting → pretty-print dates, decimals, enums, money.
- Separation of concerns → input validation vs. output serialization are independent.

## 11. Complex models

### Model Compositions

### Model inheritance

## 12. Pydantic Applications

### Consuming a REST API

### Ingesting a CSV file

### Validating Function Arguments
@validate_call

### Model code generators

In Pydantic v2, model code generators are tools that help automatically generate Pydantic models from other data formats or schemas, such as:
- OpenAPI (Swagger) specs
- JSON Schema
- SQL databases
- Type annotations (for type checking)
- External tools like datamodel-code-generator
