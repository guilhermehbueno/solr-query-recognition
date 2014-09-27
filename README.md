solr-query-recognition
======================

See in: https://www.lucidchart.com/documents/view/4d2f6939-a1d5-4268-8257-66cf8e824ad3

Examples:

Query:'tv sony 60" '

Returns:
{
  'tv': 'undefined',
  'sony': 'brandName',
  '60"': 'specification'
}


Query:'tv sony maior que 60" '
Returns:
{
  'tv': 'undefined',
  'sony': 'brandName',
  'maior que': 'condition',
  '60"': 'specification'
}
