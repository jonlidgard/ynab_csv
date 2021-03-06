## csv2ynab
```
usage: csv2ynab [options] <source> <dest>

description: csv2ynab processes Revolut & PayPal csv files for import into YNAB

positional arguments:
  source                the .csv file to process
  dest                  the output file (defaults to stdout)

optional arguments:
  -h, --help            show this help message and exit
  -E ENCODING, --encoding ENCODING
                        File encoding (default: utf-8)
  -c, --category        Fill in the category field
  -m, --memo            Fill in the Memo field
  -n, --nobank          Skip Bank entries
  -V, --version         show version and exit```

Revolut files are processed to remove the ',' from the Inflow & Outflow fields

PayPal files are processed to remove the 'Temporary Hold' and 'Currency Conversion' entries

IMPORTANT:  This program is set to work in the UK with GBP & will need modifying to work in other countries.
            MINIMAL testing carried out, check the output carefully!
            Revolut, PayPal & YNAB file specs valid as of 20th Jan 2018.
