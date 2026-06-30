# Evidence Schema Draft

Each evidence artifact should include:

```yaml
artifact_id: string
created_at: ISO-8601
source_type: manual | config_export | log | telemetry | operator_observation | policy
vendor: optional string
product_family: optional string
asset_scope: optional asset identifier
access_scope: no_access | anonymous_read | authenticated_read_only | authenticated_export_allowed | admin_read_only
read_only: true
checksum_sha256: string
redaction_status: clean | redacted | unknown
parser_version: optional string
claims_supported:
  - field: string
    value: any
    confidence: known | partially_known | inferred
limitations:
  - string
```

No secret-bearing fields may be persisted.
