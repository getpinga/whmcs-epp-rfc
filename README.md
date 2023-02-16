# Compatibility

This module is supposed to work with:

- Any Generic RFC EPP registry.

- Caucasus Online - .ge

- CentralNic - all

- CoCCA - all

- CORE/Knipp - all

- GoDaddy Registry - all

- Google Nomulus - all

- HKIRC - .hk

- Identity Digital - all

- RoTLD - .ro

- RyCE - all

- SIDN - all

- ZADNA - .za

- ZDNS - .all

# WHMCS Module Installation instructions

1. Download and install [WHMCS](https://whmcs.com/)

2. Place the repository as **epp** directory in `[WHMCS]/modules/registrars`, place your key.pem and cert.pem files in the same epp directory.

3. Activate from Configuration -> Apps & Integrations -> (search for _epp_) -> Activate

4. Configure from Configuration -> System Settings -> Domain Registrars

5. Add a new TLD using Configuration -> System Settings -> Domain Pricing

6. Create a **whois.json** file in `[WHMCS]/resources/domains` and add the following:

```
[
    {
        "extensions": ".yourtld",
        "uri": "socket://your.whois.url",
        "available": "NOT FOUND"
    }
]
```

You should be good to go now.
