## Perl TLV parser, EMV parser

**To parse a TLV string with tags of 80 7A 59 6F01 and 3 bytes of length:**

``` Perl
use TLV::Parser;
@tags = qw/ 80 7A 59 6F01 /;
$href = {
    tag_aref => \@tags,
    l_len    => 3,
};
$tlv_parser = TLV::Parser->new($href);
$tlv_parser->($tlv_string);
```

**To parse an emv_string:**

``` Perl
use TLV::EMV::Parser;
$emv_parser = TLV::EMV::Parser->new();
$emv_parser->parse($emv_string);
```
