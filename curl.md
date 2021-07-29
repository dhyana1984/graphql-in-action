```
curl -X POST -H "Content-Type: application/json" \
--data '{"query":"{allTrails{name}}"}' \
http://snowtooth.moonhighway.com
```

# issues:
## The service(git@github.com:beinan/graphql_server_starter.git) need to change "bcrypt": "^1.0.2", to "bcrypt": "^3.0.6"

# derective
```
query forAllScreen($isNarrowScreen: Blooean){
  product(id:"0001"){
    id
    name @include(if:$isNarrowScreen)
    image @skip(if: $isNarrowScreen)
  }
}
```