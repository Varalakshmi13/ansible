# ansible

Markup languages :  (key - value)
XML
JSON
YAML

###
key : value

key : Multiple values(list)
key : key-value (Map, Dict)

Makefile : Compulsary tab space
Ansible: No tab space

For Json : jq is json query
cat /tmp/1.json | jq
cat /tmp/1.json | jq .CourseName
cat /tmp/1.json | jq '.topics.aws[]'

yq in backend converts to jq