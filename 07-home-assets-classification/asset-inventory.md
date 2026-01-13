# Home Network Asset Inventory

> This inventory reflects independent analysis of a my real home network environment and applies cybersecurity asset management principles.

---

## Purpose
The purpose of this inventory is to identify network-connected assets and classify them based on sensitivity and impact to support informed security decisions.

---

## Asset Inventory Table

| Asset | Network access | Owner | Location | Notes | Sensitivity |
|-----|---------------|------|---------|------|------------|
| Primary network router | Continuous | Internet service provider (ISP) | On-premises (center of home) | Controls all network traffic and device connectivity. | Confidential |
| Secondary router | Continuous | Homeowner | On-premises (ground floor) | Extends network coverage and increases attack surface. | Confidential |
| Desktop computer | Occasional | Homeowner | On-premises | Stores private and personal information such as documents and photos. | Restricted |
| External hard drive & memory cards | Occasional | Homeowner | On-premises | Stores sensitive data and is frequently shared with others. | Restricted |
| Smart security camera (Wi-Fi) | Continuous | Homeowner | On-premises | Internet-connected camera capturing video and audio. | Confidential |
| Smart TVs (two units) | Occasional | Homeowner | On-premises (multiple floors) | Wi-Fi-connected devices with limited stored data. | Internal-only |
| Legacy printer | Occasional | Homeowner | On-premises | Older printer that may retain printed document data. | Internal-only |
| Mobile phones (family members) | Continuous | Family members | On- and off-premises | Personal devices that auto-connect to Wi-Fi and store private data. | Internal-only |
| Guest smartphones | Occasional | Guests | On- and off-premises | Temporarily connect to the home network. | Internal-only |

---

## Sensitivity Categories

| Category | Access designation |
|--------|------------------|
| Restricted | Need-to-know |
| Confidential | Limited to specific users |
| Internal-only | Authorized on-premises users |
| Public | Anyone |

---

## CIA Triad Mapping & Risk Scoring

The following table maps each asset to the CIA Triad (Confidentiality, Integrity, Availability) and assigns an overall risk score based on likelihood and impact if the asset were compromised.

| Asset | Confidentiality Impact | Integrity Impact | Availability Impact | Overall Risk |
|-----|-----------------------|------------------|--------------------|-------------|
| Primary network router | High | High | High | **High** |
| Secondary router | High | High | Medium | **High** |
| Desktop computer | High | Medium | Medium | **High** |
| External hard drive & memory cards | High | Medium | Low | **High** |
| Smart security camera (Wi-Fi) | High | Medium | Medium | **High** |
| Smart TVs (two units) | Low | Low | Medium | **Low** |
| Legacy printer | Medium | Low | Low | **Low** |
| Mobile phones (family members) | High | Medium | Medium | **Medium** |
| Guest smartphones | Low | Low | Low | **Low** |

---
### CIA Triad Evaluation Logic

- **Confidentiality** reflects the sensitivity of data exposed if the asset is compromised.
- **Integrity** measures the potential for unauthorized modification of data or configurations.
- **Availability** considers the impact of service disruption or device unavailability.
- **Overall Risk** is determined by combining impact severity with likelihood of exploitation.

Assets that control network access, store sensitive data, or are continuously connected are rated higher risk.

---
## Classification Rationale
Assets were classified based on potential impact to confidentiality, integrity, and availability if compromised, with particular attention to data sensitivity and network control.

