# IETF 115 Hackathon - PQC Certificates

## Folder structure of this repo

- root
  - company / implementation name 1
    - implementation_name.zip
    - any other files
  - company / implementation name 2
    - ...



## Zip format

At the hackathon, we are all going to script our PKI toolkits to produce and read zip bundles of certs in the following format. Scripts should place data into files with the following names so that parsing scripts 

(parantheses denotes optional files)

- artifacts.zip
    - \<alg oid\>
    - ta/     # trust anchor, aka root CA, aka self-signed
            - ta.der
            - ta_priv.der
            - (*.pem)
        - ca/     # certificate authority, aka intermediate CA
            - ca.der
            - ca_priv.der
            - (*.pem)
        - ee/     # end entity
            - cert.der
            - cert_priv.der    # corresponding private key
            - cert.csr
            - (*.pem)
        - crl/
            - crl_ta.crl
            - crl_ca.crl
        - ocsp/
            - ocsp.der


## OIDs

The OID mappings to be used for this hackathon are documented in `oid_mapping_oqs.md`.