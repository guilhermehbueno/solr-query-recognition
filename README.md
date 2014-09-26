solr-query-recognition
======================

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
