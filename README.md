# token-list
DeFi Token List Service

## Run Locally
1. Run `yarn install`
2. Install Redis
3. Run `redis-server`
4. Run `yarn start`

## Deploy Google Cloud Function

gcloud functions deploy token-image \
--gen2 \
--region=us-central1 \
--runtime=nodejs16 \
--source=. \
--entry-point=tokenImage \
--trigger-http \
--vpc-connector=projects/nomadic-rig-389719/locations/us-central1/connectors/token-image \
--set-env-vars=REDISHOST=10.196.57.251,REDISPORT=6379