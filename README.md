# Sentiment per message

Sentiment analysis docker image for simplified setup. This docker image is used for sentiment analysis per message.

> https://doc.livehelperchat.com/docs/bot/sentiment-analysis-per-message

# Install

Pull images

```shell
git clone https://github.com/LiveHelperChat/sentiment-per-message && cd sentiment-per-message
docker-compose -f docker-compose.yml pull
wget https://livehelperchat.com/var/deep_sentence.tgz
tar zxfv deep_sentence.tgz
rm -f deep_sentence.tgz
```

Run one time

```
docker-compose -f docker-compose.yml up
```

Run as a service

```
docker-compose -f docker-compose.yml up -d
```

Testing

```shell
curl -X 'POST' \
  'http://127.0.0.1:5058/model' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "sentences": [
    "I'\''m sad"
  ]
}'
```

You cal also point your browser to test directly

> http://127.0.0.1:5058/docs