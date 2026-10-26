# Awesome ISO 20022 [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of specifications, deadlines, bank announcements, open-source libraries and tools for ISO 20022 payments, focused on payment initiation (pain.001) and the move to structured postal addresses.

ISO 20022 is the messaging standard behind SEPA, Swift cross-border payments (CBPR+), Fedwire, CHAPS and the Swiss payment system. This list is for developers, payment teams and ERP integrators who need the primary sources and working code, not marketing pages.

## Contents

- [Deadlines](#deadlines)
- [Official specifications](#official-specifications)
  - [ISO 20022](#iso-20022)
  - [SEPA (EPC)](#sepa-epc)
  - [Swift CBPR+](#swift-cbpr)
  - [Switzerland (SIX)](#switzerland-six)
  - [United States (Fedwire)](#united-states-fedwire)
  - [United Kingdom (CHAPS)](#united-kingdom-chaps)
  - [Germany (EBICS)](#germany-ebics)
- [Bank announcements](#bank-announcements)
- [Libraries](#libraries)
  - [Java](#java)
  - [JavaScript and TypeScript](#javascript-and-typescript)
  - [Python](#python)
  - [Go](#go)
  - [.NET](#net)
  - [Rust](#rust)
- [ERP and accounting integrations](#erp-and-accounting-integrations)
- [Validators and tools](#validators-and-tools)
- [Learning](#learning)
- [Related: Nacha ACH](#related-nacha-ach)
- [Related lists](#related-lists)

## Deadlines

Structured postal address dates as published by each body. Last checked: 26 October 2026. Each row links to its primary source.

| Scheme | Status | Source |
|---|---|---|
| SEPA (EPC) | The 15 November 2026 end of unstructured addresses was postponed on 10 September 2026. No new date yet. | [EPC](https://www.europeanpaymentscouncil.eu/node/28486) |
| Swift CBPR+ | Structured address requirement deferred on 27 August 2026. Update promised by December 2026. Hybrid allowed since November 2025. | [Swift](https://www.swift.com/insights/news/swift-accepts-community-request-extend-structured-address-migration-iso-20022-payment-messages) |
| Switzerland (SIX) | Unchanged: from 14 November 2026 (by execution date), pain.001.001.09 only, with town and country in their own fields. Banks differ on how strictly they enforce it. | [SIX](https://www.six-group.com/en/products-services/banking-services/payment-standardization/swiss-payments.html) |
| US Fedwire | November 2026 release moved to November 2027. Hybrid addresses supported from that release. | [Federal Reserve](https://www.frbservices.org/news/communications/082726-fedwire-november-release-rescheduled) |
| UK CHAPS | November 2026 RTGS standards release deferred on 27 August 2026. No new date yet. | [Bank of England](https://www.bankofengland.co.uk/news/2026/august/delay-to-the-november-2026-rtgs-standards-release) |

## Official specifications

### ISO 20022

- [ISO 20022 message definitions](https://www.iso20022.org/iso-20022-message-definitions) - The official catalogue of message schemas (XSD), current and archived, including every pain.001 version.
- [External code sets](https://www.iso20022.org/catalogue-messages/additional-content-messages/external-code-sets) - Purpose, category purpose, service level and other code lists, updated quarterly.

### SEPA (EPC)

- [SCT customer-to-PSP implementation guidelines](https://www.europeanpaymentscouncil.eu/document-library/implementation-guidelines/sepa-credit-transfer-customer-psp-implementation-1) - The EPC rules for SEPA Credit Transfer pain.001 files.
- [EPC153-22: Provision of addresses under the EPC payment schemes](https://www.europeanpaymentscouncil.eu/document-library/guidance-documents/epc-guidance-document-provision-addresses-under-epc-payment) - Structured and hybrid address rules (version 2.2, 30 September 2026).
- [EPC news](https://www.europeanpaymentscouncil.eu/publications/news) - Where a new address end date will be announced.

### Swift CBPR+

- [Structured address migration extended](https://www.swift.com/insights/news/swift-accepts-community-request-extend-structured-address-migration-iso-20022-payment-messages) - Swift's August 2026 deferral, updated September 2026.
- [PMPG hybrid postal address guidance](https://www.swift.com/sites/default/files/files/pmpg-hybrid-postal-address-v1.06_202507.pdf) - How hybrid addresses work in CBPR+ (v1.06, PDF).

### Switzerland (SIX)

- [Roadmap Swiss Payments](https://www.six-group.com/en/products-services/banking-services/payment-standardization/swiss-payments.html) - The decision to keep 14 November 2026.
- [ISO 20022 Swiss Payment Standards](https://www.six-group.com/en/products-services/banking-services/payment-standardization/standards/iso-20022.html) - SPS 2026 overview and downloads.
- [Implementation Guidelines Credit Transfer, SPS 2026 v2.3](https://www.six-group.com/dam/download/banking-services/standardization/sps/ig-credit-transfer-sps-2026-en.pdf) - The Swiss pain.001 rules (PDF).

### United States (Fedwire)

- [Fedwire November 2026 release rescheduled](https://www.frbservices.org/news/communications/082726-fedwire-november-release-rescheduled) - The move to November 2027.
- [November 2027 release FAQ](https://www.frbservices.org/resources/financial-services/wires/iso-20022-implementation-center/november-release-faq) - Scope of the next release, including hybrid addresses.

### United Kingdom (CHAPS)

- [ISO 20022 handbook](https://www.bankofengland.co.uk/payment-and-settlement/rtgs-renewal-programme/iso-20022-handbook) - Bank of England guidance for CHAPS messages.
- [Delay to the November 2026 RTGS standards release](https://www.bankofengland.co.uk/news/2026/august/delay-to-the-november-2026-rtgs-standards-release) - The August 2026 deferral.

### Germany (EBICS)

- [EBICS news](https://www.ebics.de/de/aktuelles) - Announcements from the German banking industry, including the September 2026 suspension of legacy format retirement (in German).

## Bank announcements

Banks set their own dates and tolerances within each scheme. Check your own bank's page.

- [BEKB](https://www.bekb.ch/firmenkunden/zahlen/zahlungsverkehr/anpassungen-zahlungsverkehr) - Switzerland. From 14 November 2026, payment files only as pain.001.001.09 and no unstructured addresses (in German).
- [LUKB](https://www.lukb.ch/unternehmen/zahlen/zahlungsverkehr/strukturierte-adressen) - Switzerland. pain file changeover postponed, new date to follow (in German).
- [OKB](https://www.okb.ch/strukturierte-adressen) - Switzerland. pain.001.001.09 only from 13 November 2026 (in German).
- [PostFinance](https://www.postfinance.ch/en/business/kampagnen/iso-updates.html) - Switzerland. Unstructured pain.001 not rejected outright for now, but processing to the payee isn't guaranteed.
- [ZKB](https://www.zkb.ch/de/lps/unternehmen/zahlen/neuer-zahlungsverkehr.html) - Switzerland. Provisional extension for unstructured addresses in certain cases (in German).
- [PKO Bank Polski](https://www.pkobp.pl/aktualnosci/bankowosc-elektroniczna/we-are-changing-the-deadline-for-the-removal-of-certain-file-formats-in-ipko-biznes-and-ipko-biznes-integra) - Poland. Postponed the removal of older file formats.
- [UniCredit (HypoVereinsbank)](https://www.hypovereinsbank.de/content/dam/hypovereinsbank/unternehmen/pdf/Downloadcenter/Overview_Format_Changes_in_November_2026_EN.pdf) - Germany. Overview of format changes (PDF).
- [Volksbank Stuttgart](https://www.volksbank-stuttgart.de/firmenkunden/zahlungsverkehr/ratgeber/aenderungen-pain-formate.html) - Germany. Changes to pain formats (in German).

## Libraries

### Java

- [prowide-iso20022](https://github.com/prowide/prowide-iso20022) - Business model and parser for the full set of ISO 20022 messages.
- [tools20022-api-payments](https://github.com/tools20022/tools20022-api-payments) - Java API for the ISO 20022 payments business domain.
- [bank4j](https://github.com/inisos/bank4j) - Generates payment initiation XML and validates IBANs and BICs.
- [xmlsignverify-core-java](https://github.com/Mastercard/xmlsignverify-core-java) - Mastercard's reference library for signing and verifying ISO 20022 XML.

### JavaScript and TypeScript

- [iso20022.js](https://github.com/svapnil/iso20022.js) - Creates ACH, SEPA, FedNow, Swift and RTP payment initiations and processes bank statements.
- [sepa.js](https://github.com/kewisch/sepa.js) - Generates SEPA XML in the browser or Node.js, mainly geared towards German direct debits.
- [node-ebics-client](https://github.com/node-ebics/node-ebics-client) - EBICS client for Node.js.

### Python

- [pyiso20022](https://github.com/phoughton/pyiso20022) - Creates and parses ISO 20022 messages.
- [python-sepaxml](https://github.com/raphaelm/python-sepaxml) - Generates SEPA credit transfer (pain.001.001.03 and .09) and direct debit XML.
- [pain001](https://github.com/sebastienrousseau/pain001) - Generates and validates pain.001 files from CSV, JSON and other sources.

### Go

- [moov-io/iso20022](https://github.com/moov-io/iso20022) - ISO 20022 message implementations in Go.
- [moov-io/fedwire20022](https://github.com/moov-io/fedwire20022) - ISO 20022 messages for Fedwire.

### .NET

- [ISO20022DotNet](https://github.com/VMelnalksnis/ISO20022DotNet) - ISO 20022 message models for .NET.
- [Money](https://github.com/chstorb/Money) - .NET classes for many ISO 20022 payments messages.

### Rust

- [Reframe](https://github.com/GoPlasmatic/Reframe) - Two-way transformation between Swift MT and ISO 20022.

## ERP and accounting integrations

- [OCA bank-payment](https://github.com/OCA/bank-payment) - Odoo Community Association modules for SEPA and pain.001 payment files.
- [OCA l10n-switzerland](https://github.com/OCA/l10n-switzerland) - Odoo Community Association Swiss localisation: PostFinance e-bills, plus Swiss pain.001 credit transfer modules on some Odoo versions (16.0, 18.0).
- [Dolibarr](https://github.com/Dolibarr/dolibarr) - Open-source ERP and CRM with SEPA credit transfer and direct debit export.

## Validators and tools

- [PacsLint](https://pacslint.com) - Free browser-based pain.001 checker and fixer (schema, EPC and Swiss rules, structured addresses) and .03 to .09 converter. Files are never uploaded to a server. Built by this list's maintainer.
- [qrbill](https://github.com/nexys-admin/qrbill) - Generator and validator for Swiss QR-bills.

## Learning

- [ISO 20022 encyclopedia](https://github.com/nnavnita/iso20022) - Interactive reference of payment message fields, codes and MT equivalents.
- [ISO 20022 Academy](https://github.com/revanthrsai/ISO-20022-Academy) - Lessons with real pain.001, pacs.008 and camt.053 examples.
- [Structured address deadline explained](https://pacslint.com/structured-address-deadline/) - Timeline of the EPC, Swift, Fedwire and CHAPS postponements, with sources. By this list's maintainer.
- [Swiss structured addresses from 14 November 2026](https://pacslint.com/swiss-structured-address-2026/) - Checklist and bank-by-bank status for Switzerland. By this list's maintainer.
- [pain.001.001.03 to .09: what changes](https://pacslint.com/pain001-03-to-09/) - Element-by-element mapping between the two versions. By this list's maintainer.

## Related: Nacha ACH

US ACH files are not ISO 20022, but payment teams often handle both.

- [Nacha ACH Guide for Developers](https://achdevguide.nacha.org/ach-file-overview) - Record layouts, codes, blocking and padding.
- [moov-io/ach](https://github.com/moov-io/ach) - Reader, writer and validator for Nacha ACH files in Go.

## Related lists

- [awesome-fintech](https://github.com/moov-io/awesome-fintech) - Open-source fintech libraries for payments and banking.
- [awesome-payments](https://github.com/awesomelistsio/awesome-payments) - Platforms, APIs and standards across payments.

## Contributing

Contributions are welcome. Read the [contribution guidelines](CONTRIBUTING.md) first.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the maintainer has waived all copyright and related rights to this work.
