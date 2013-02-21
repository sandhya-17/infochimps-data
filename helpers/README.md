# Helper Datasets

* `helpers/torture` -- data with edge cases for text processing, etc; for example, a file with various examples of bad UTF-8 encoding.
* `helpers/numbers` -- more useful than you'd think, these files have one column, holding a 0 (`zeros-*.tsv`), a 1 (`ones-*.tsv`) or the line number starting at zero (`integers-*.tsv`). The files labeled `1Mi` have `2^20` (a bit over one million) lines; the files labeled `1ki` have `2^10` (1024) lines.


## helpers/torture/utf8-test

The `UTF8-test*` files are adapted from [Markus Kuhn](http://www.cl.cam.ac.uk/~mgk25/)'s [UTF-8 decoder stress test](http://www.cl.cam.ac.uk/~mgk25/ucs/examples/UTF-8-test.txt)

DO NOT EDIT the `UTF8-test*.json` files. Your editor will screw them up. Quoting @johnezang,

> The file contains JSON with very specific UTF-8 encoding errors that are likely to be stripped or mutilated. It requires bit perfect binary replication. Even editing with something like TextEdit.app is likely to destroy the UTF-8 errors contained within.

The files should have md5 hashes of `32d1547bd128a4278abeafbdd011396b` (array_of_string) and `9bcfa43fafd7405843ff094d5a1299a1` (plain_string). 

To recreate, copy the text below (starting with 'Q', ending with '=') and run

    pbpaste | openssl enc -d -base64 | bunzip2 > UTF8-test-array_of_string.json
    md5 UTF8-test-array_of_string.json

You should see

    MD5 (UTF8-test-array_of_string.json) = 32d1547bd128a4278abeafbdd011396b

```
QlpoOTFBWSZTWSw1iJcACbL////7YXn/////f//Orj////X/////////////////
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
```