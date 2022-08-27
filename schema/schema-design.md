# Schema Design Concerns

# Key Concerns
- Allowing for rolling updates/staged rollout i.e. when a schema changes how does it allow the server side applications to change? Basically you want certain application not to change which writes to not change/ignore
- Applicability of rolling updates not only to data formats but schemas as well as old and new code which write and reads the data
- Data Encoding schemes - Few related concerns -> size, storage, language independence of encoding schemes
## Forward and backward compatibility of Schemas
  - Definition
    - Backward Compatibility - new code can read data that was written by old code
    - Forward Compatibility - older can read data that was was written by new code
## Granularity
## Data formats/Encoding standards
  - Few noteable schemes for encoding and decoing : JSON, XML, Protobuff, Thrift, Avro
  - Encoding/Serialization/marshalling - spped, complexity, size are few aspects to look at
