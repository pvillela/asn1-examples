# asn1-examples

This repo contains some examples of ASN.1 schemas and values with corresponding DER encodings.  The tools used to work with these examples are:

- VSCode ASN1Vcx [plugin](https://marketplace.visualstudio.com/items?itemName=OSSNokalva.asn1vcx) from [OSS Nokalva](https://www.oss.com/)
- [OSS Nokalva ASN.1 Playground](https://asn1.io/asn1playground/)
- [der2ascii](https://github.com/google/der-ascii)

Steps:
- Compile MyExample.asn by pasting contents into the Schema pane of [OSS Nokalva ASN.1 Playground](https://asn1.io/asn1playground/) (on Chrome) and pressing the Compile button.
- Generate DER file from playground by pasting `data Wrapper ::= myWrapper` into the Value pane and pressing the Encode button.
- Run `der2ascii -i <DER file> -o myWrapper.asc` to generate ASCII decoding of the DER file.
- Similar to above for `SetWrapper` and `SetWrapper1`:
  - `data SetWrapper ::= mySetWrapper`
  - `data SetWrapper1 ::= mySetWrapper1`

  The above demonstrate that the DER encoding of SET objects always follows a canonical ordering.

