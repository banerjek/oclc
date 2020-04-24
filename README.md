# oclc
Bash scripts to interact with OCLC using the API

A couple gotchas when using the OCLC API:

1. Generating HMAC signatures is picky and nonintuitive. Specific text literals that differ from what would be expected must appear on specific lines, and HTTP variables in the sig are required to be in specific order that differs from the order they're actually passed. 

This means that if you create your own functions, formatting a correct HMAC signature for any new function requires consulting the HMAC generator at https://platform.worldcat.org/api-explorer/hmac -- don't just read the directions or use the methods you see here for other operations.

2. Be sure to strip leading zeros from OCLC numbers in input files 
