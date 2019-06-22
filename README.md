# warsawjs-workshop-33-collector-backend
(Backend) WarsawJS Workshop #33: Projekt aplikacji w Vue.js do listowania długów wobec innych.

## Testowanie
Odpalanie:
```
json-server --watch db.json
```
GET:
```
fetch('http://localhost:3000/debts/')
  .then(function(response) {
    return response.json()
  }).then(function(json) {
    console.log('parsed json: ', json)
  }).catch(function(ex) {
    console.log('parsing failed: ', ex)
  });
```

POST:
```
fetch('http://localhost:3000/debts/', {
  method: 'post',
  headers: {
    'Accept': 'application/json',
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
       "title":   "New games 2",
       "who": "Robert",
       "amount": 13.99
   })
}).then(function(response) {
      return response.json()
    }).then(function(json) {
      console.log('parsed json: ', json)
    }).catch(function(ex) {
      console.log('parsing failed: ', ex)
    });
```
