# Pod 5 & 6

## Team

| Name              | Email                         |
| ----------------- | ----------------------------- |
| Andre Mendonça    | andremendonca@novopayment.com |
| Hector Corredor   | hcorredor@novopayment.com     |
| Juan Pablo Romero | jpromero@novopayment.com      |
| Luis Villamizar   | lvillamizar@novopayment.com   |
| Melanie Godoy     | mgodoy@novopayment.com        |
| Nelida Cerna      | nvalencia@novopayment.com     |
| Samuel Padilla    | spadilla@novopayment.com      |
| [[Marre Palma]]   | mpalma@novopayment.com        |
|                   | cyate@novopayment.com         |

**Helpers (not direct reports):**
- Lina Quintana - lquintana@novopayment.com (Product Owner)
- Ivana Hurtado - ihurtado@novopayment.com (Scrum Master)
- Sebastian Gomez - sgomez@novopayment.com (PM - Spend)

## Pods

- Pod 1 - Card Solutions
- Pod 2 - Digital Acquiring
- Pod 3 - (frontend admin for Pichincha, Banorte)
- Pod 4 - Tokenization

Pods were formed to unify clients that used to be organized purely by product/client copies of the same programs. They're grouped by product type now (digital banking, card payment, cash management, tokenization/SDKs/mandates).

**Product abbreviations:** CPM = Conexión Personas Mobile · CPO = Conexión Personas Online · CEO = Conexión Empresas Online

## Product → client → test coverage

| Product | Clients | Test coverage |
|---|---|---|
| CEO, CPO, CPM | Banorte, Tebca, Banco Pichincha, Coopcentral, Produbanco, Banco Guayaquil | CEO/CPO - Web; CPM - Android & iOS (Banorte, Tebca) |
| SDK (tokenization) | Mio, Cibao, Billet, Dale, BNP, Lynk (Vimenca, Banrural possible) | Mobile (Android) |
| Backoffice (Digital Banking + Card Solutions) | Primetrust, Waufin (internal use) | Web |
| Digital Banking | Primetrust, BNP | Web, Mobile, APIs |
| Spend (in development) | Tebca | Web, Mobile |

CEO/CPO is a cash-management product (Banorte, Pichincha, Coopcentral, Produbanco, Guayaquil). Primetrust blends digital banking and card solutions, backend now under Pod 2. BNP is digital banking. Spend is a newer product that behaves somewhat like CEO/CPO, starting with Tebca.

## Repo ownership

| App | Responsible |
|---|---|
| Conexión Empresas Online (CEO) | Hector |
| Conexión Personas Online (CPO) | Hector |
| Prime Money / Primetrust (web + Android) | Hector, Melanie |
| Backoffices Multiplatform | Hector |
| php-base | Hector |
| Bot Mia | Hector |
| Spend Management | Sam |
| Banco Nacional de Panamá (BNP) | Juan Pablo, Melanie |
| SDK Tokenización | Melanie |
| Tebca Peru (KMP) | Luis |
| Banorte | Luis |
| Coopcentral | Luis |

## Team priorities

- Cifra
- AI Adoption, Code Analysis

Target work split: 70% features, 20% refactor, 10% innovation (can flex to include production support).

