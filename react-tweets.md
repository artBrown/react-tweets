#####170310 http://stackoverflow.com/questions/38405514/webpack-babel-loading-error-uncaught-syntaxerror-unexpected-token-import
npm install --save-dev webpack babel-loader babel-core babel-cli babel-preset-es2015

####qbox
https://8df8e4e2.qb0x.com:31984/app/kibana#/management/kibana/index/?_g=()

curl -X PUT "https://8df8e4e2.qb0x.com:9200/company" -d '{
  "settings": {
    "index": {
      "number_of_shards": 1,
      "number_of_replicas": 1
    },
    "analysis": {
      "analyzer": {
        "analyzer-name": {
          "type": "custom",
          "tokenizer": "keyword",
          "filter": "lowercase"
        }
      }
    },
    "mappings": {
      "employeeinfo": {
        "properties": {
          "age": {
            "type": "long"
          },
          "experienceInYears": {
            "type": "long"
          },
          "name": {
            "type": "string",
            "analyzer": "analyzer-name"
          }
        }
      }
    }
  }
}'

curl -XPUT 'http://9dae02428d83f160000.qbox.io:80/_river/my_twitter_river/_meta' -d '{
  "type" : "twitter", 
    "twitter" : {
        "oauth" : {
            "consumer_key" : "TJLSrcKh0fcTsGaPmObuoJlvr",
            "consumer_secret" : "VWnhqDaF87tMz17zujbIplHO9TXvAwP8E9LQ9QEoPCrszYdQQm",
            "access_token" : "760453306112024576-grrqLJgJHbPsTUEBK128M1mmCjlOdOL",
            "access_token_secret" : "qUtfrVzvXCW1jYQhhx0V7hwaLYOaCPxXtEGUhdafSnJJO"
        },
        "filter" : {
            "tracks" : "marvel,comics",
            "language" : "en"
        }
    },
    "index" : {
        "index" : "comics",
        "type" : "comics",
        "bulk_size" : 100,
        "flush_interval" : "5s"
    }
}'
