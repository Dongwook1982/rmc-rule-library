# Deferred Rules — Draft Definitions

Three rules were reviewed for inclusion in the RMC library but deferred due to unresolvable regulatory ambiguity in KDS 24 14 21. These are documented here for transparency and future resolution.

---

## DIM-DEF-001 (candidate for DIM-029)

**Description:** PSC girder precamber (pre-stress-induced upward camber) tolerance at time of erection  
**Source clause:** KDS 24 14 21 §4.3.9  
**Reason for deferral:** Clause states tolerance is "as approved by the structural engineer of record" with no quantitative default. Encoding requires project-specific approval and cannot be standardized across projects without an absolute numerical bound.  
**Proposed resolution:** Await MOLIT revision or obtain project-specific engineer sign-off; encode as a parameter-configurable rule (DIM-029) with default tolerance of ±L/1000 (where L = span length in mm).

---

## MAT-DEF-001 (candidate for MAT-016)

**Description:** Epoxy-coated reinforcing bar coating adhesion strength  
**Source clause:** KDS 24 14 21 §5.4.4  
**Reason for deferral:** Standard references ASTM A775 without specifying a Korean-specific minimum threshold; the applicable value depends on exposure classification and is subject to engineer discretion.  
**Proposed resolution:** Encode as ASTM A775 §7.3 minimum (≥ 1.7 MPa) pending MOLIT clarification; flag as informational (sh:Info) rather than violation.

---

## REG-DEF-001 (candidate for REG-026)

**Description:** Third-party inspection agency certification for critical structural elements  
**Source clause:** KDS 24 14 21 §7.3  
**Reason for deferral:** Clause requires "appropriate certification" without specifying which accreditation bodies are recognized. Encoding a closed list risks excluding legitimate agencies; encoding an open check is not machine-verifiable.  
**Proposed resolution:** Encode as a reference-presence check (certifyingAgencyId must be non-null) and defer value-set validation to a maintained lookup table managed by the project owner.
