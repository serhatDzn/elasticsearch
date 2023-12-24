### Index oluşturma ve data ekleme


PUT products/_doc/3
{
  "name":"Iphone 14",
  "rating": 8,
  "published": true,
  "category": "mobile phones",
  "price": {
    "usd":2500,
    "eur":2000
  }
}

### data çekme

GET products/_doc/1

GET products/_source/1

### Shard ve replica görme

GET _cat/shards/products

### identifiers

Put ile kayıt eklerken eğer o kayıt yok ise oluşturur, eğer varsa değiştirir. Burada bir uyarı ifadesi gelmesini istiyorsak create kullanırız. ID değeri evrmeden kayıt yapılmasını istediğimizde ise POST metodunu kullanırız.

PUT products/_create/1
{
  "name":"Samsung",
  "rating": 8,
  "published": true,
  "category": "mobile phones",
  "price": {
    "usd":2500,
    "eur":2000
  }
}


POST products/_doc
{
  "name":"Huawei",
  "rating": 8,
  "published": true,
  "category": "mobile phones",
  "price": {
    "usd":2500,
    "eur":2000
  }
}