# Validation - Addresses must have street number component

- [local-validator.ttl](local-validator.ttl) - Validator using namespaces that the data in the sandbox environment uses
  - Note: some of the namespaces have since changed due to new updates to the Address Model. This validator and the ETL will need to be updated to use the new namespaces when going into the build phase of the project.
- [valid-01.ttl](valid-01.ttl) - Valid address 01
- [valid-02.ttl](valid-02.ttl) - Valid address 02
- [invalid-01.ttl](invalid-01.ttl) - Invalid address 01 - only has 1 address component
- [invalid-02.ttl](invalid-02.ttl) - Invalid address 02 - does not contain at least 1 address component related to street number

Running the tests:

```
pyshacl -s local-validator.ttl invalid-02.ttl
```
