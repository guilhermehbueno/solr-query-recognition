solr-query-recognition
======================

See in: https://www.lucidchart.com/documents/view/4d2f6939-a1d5-4268-8257-66cf8e824ad3

Examples:

Query:'tv sony 60" '

Returns:
```javascript
{
  'tv': 'undefined',
  'sony': 'brandName',
  '60"': 'specification'
}
```


Query:'tv sony maior que 60" '
Returns:
```javascript
{
  'tv': 'undefined',
  'sony': 'brandName',
  'maior que': 'condition',
  '60"': 'specification'
}
```


```java
Recon.fromQuery("tv sony 60 polegadas").has(field("brand")) // true
Recon.fromQuery("tv sony 60 polegadas").get(field("brand")) //sony
Recon.fromQuery("tv sony 60 polegadas").has(field("brand").after(word("tv"))) // true
```
