# newrelic_agent_up

## New Relic Agentをコンテナで起動してみる

コマンド

```bash
# echo "license_key: ${NR_LICENSE_KEY}" > newrelic-infra.yml
echo "enable_process_metrics: true" > newrelic-infra.yml
```

```
export NRIA_LICENSE_KEY=`cat env.param`
echo "license_key: $NRIA_LICENSE_KEY" >> newrelic-infra.yml
```

```bash
docker build -t newrelic-infra . --no-cache
```

```bash
docker run \
  --detach \
  --name newrelic-infra \
  newrelic-infra
```
