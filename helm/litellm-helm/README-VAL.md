# Key Management Examples (Internal)

Example requests for managing LiteLLM proxy keys against an internal deployment.

```bash
curl -X POST https://ai.cloud-doctor.eu/key/update \
  -H "Authorization: Bearer XXX" \
  -H "Content-Type: application/json" \
  -d '{
    "key": "sk-YYY",
    "duration": "0d",        # expire it immediately
    "models": []             # or revoke model access
  }'

  # List all keys (inspect what's active)
curl https://ai.cloud-doctor.eu/key/list \
  -H "Authorization: Bearer wgrUQYqz3s8u7nH$"

# Get info on a specific key
curl -X POST https://ai.cloud-doctor.eu/key/info \
  -H "Authorization: Bearer XXX" \
  -H "Content-Type: application/json" \
  -d '{"keys": ["sk-YYY"]}'

  curl -L -X POST 'https://ai.cloud-doctor.eu/key/service-account/generate' \
-H 'Authorization: Bearer XXX' \
-H 'Content-Type: application/json' \
-d '{
 "team_id": "87495bfe-55ec-4742-9ab5-4efa837034e3"
}'

```
