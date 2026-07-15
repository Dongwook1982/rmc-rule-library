# Rule Traceability Matrix

This matrix maps each rule in the RMC library to its source regulatory clause, validation method, target IFC class, and severity level.

> Source: KDS 24 14 21 (MOLIT 2021) and ISO 19650-1:2018  
> Last reviewed: 2025-06-01 by SeniorEngineer-A, SeniorEngineer-B, QualityManager

---

## A. Dimensional Tolerance Rules (DIM-001 – DIM-028)

| Rule ID | Description | KDS Clause | Target Class | Tolerance | Unit | Severity |
|---------|-------------|------------|--------------|-----------|------|----------|
| DIM-001 | PSC girder horizontal alignment | §4.3.2 | IfcBeam | ±5.0 | mm | Critical |
| DIM-002 | PSC girder vertical camber | §4.3.3 | IfcBeam | ±8.0 | mm | Critical |
| DIM-003 | Bearing seat level | §4.4.1 | IfcBearing | ±3.0 | mm | Critical |
| DIM-004 | Bearing pad verticality | §4.4.2 | IfcBearing | ±0.5 | deg | Critical |
| DIM-005 | Deck slab thickness | §4.5.1 | IfcSlab | ±5.0 | mm | Major |
| DIM-006 | Deck surface flatness (3 m) | §4.5.2 | IfcSlab | 0–5.0 | mm | Major |
| DIM-007 | Abutment cap elevation | §4.6.1 | IfcWall | ±5.0 | mm | Critical |
| DIM-008 | Pier column verticality | §4.6.2 | IfcColumn | 0–2.0 | ‰ | Critical |
| DIM-009 | Pier cap width | §4.6.3 | IfcColumn | ±5.0 | mm | Major |
| DIM-010 | Box culvert alignment | §4.7.1 | IfcCovering | ±10.0 | mm | Major |
| DIM-011 | Girder span length | §4.3.4 | IfcBeam | ±10.0 | mm | Major |
| DIM-012 | Girder section depth | §4.3.5 | IfcBeam | ±5.0 | mm | Major |
| DIM-013 | Girder section width | §4.3.6 | IfcBeam | ±5.0 | mm | Major |
| DIM-014 | Diaphragm position (longitudinal) | §4.3.7 | IfcMember | ±10.0 | mm | Minor |
| DIM-015 | Bearing centerline offset | §4.4.3 | IfcBearing | ±3.0 | mm | Major |
| DIM-016 | Deck cross-slope | §4.5.3 | IfcSlab | ±0.2 | % | Minor |
| DIM-017 | Expansion joint gap | §4.8.1 | IfcBuildingElementProxy | ±3.0 | mm | Major |
| DIM-018 | Parapet wall alignment | §4.9.1 | IfcWall | ±5.0 | mm | Minor |
| DIM-019 | Drainage pipe invert level | §4.10.1 | IfcPipeSegment | ±10.0 | mm | Minor |
| DIM-020 | Footing plan position | §4.6.4 | IfcFooting | ±15.0 | mm | Major |
| DIM-021 | Footing top elevation | §4.6.5 | IfcFooting | ±10.0 | mm | Major |
| DIM-022 | Pile cap top elevation | §4.6.6 | IfcPile | ±10.0 | mm | Major |
| DIM-023 | Precast segment end-face squareness | §4.3.8 | IfcBeam | 0–3.0 | mm | Minor |
| DIM-024 | Wing wall batter | §4.6.7 | IfcWall | 0–3.0 | ‰ | Minor |
| DIM-025 | Curb and gutter line | §4.9.2 | IfcBuildingElementProxy | ±8.0 | mm | Minor |
| DIM-026 | Approach slab settlement | §4.11.1 | IfcSlab | ±10.0 | mm | Minor |
| DIM-027 | Noise barrier post plumb | §4.12.1 | IfcColumn | 0–3.0 | mm/m | Minor |
| DIM-028 | Pedestrian railing post spacing | §4.12.2 | IfcRailing | ±15.0 | mm | Minor |

---

## B. Material Compliance Rules (MAT-001 – MAT-015)

| Rule ID | Description | KDS Clause | Target Class | Minimum | Maximum | Unit | Severity |
|---------|-------------|------------|--------------|---------|---------|------|----------|
| MAT-001 | Girder concrete compressive strength | §5.2.1 | IfcBeam | 40.0 | — | MPa | Critical |
| MAT-002 | Pier concrete compressive strength | §5.2.2 | IfcColumn | 30.0 | — | MPa | Critical |
| MAT-003 | Deck slab concrete strength | §5.2.3 | IfcSlab | 27.0 | — | MPa | Major |
| MAT-004 | Prestressing strand tensile strength | §5.3.1 | IfcTendon | 1860.0 | — | MPa | Critical |
| MAT-005 | Prestressing force (jacking stress ratio) | §5.3.2 | IfcTendon | — | 0.75 | ratio | Critical |
| MAT-006 | Prestressing strand elongation | §5.3.3 | IfcTendon | — | 2.5 | % | Major |
| MAT-007 | Reinforcing steel yield strength | §5.4.1 | IfcReinforcingBar | 400.0 | — | MPa | Critical |
| MAT-008 | Reinforcing bar cover depth | §5.4.2 | IfcReinforcingBar | 40.0 | — | mm | Critical |
| MAT-009 | Concrete air-entrainment (XF class) | §5.2.4 | IfcBeam | 4.0 | 7.0 | % | Major |
| MAT-010 | Bearing elastomer hardness | §5.5.1 | IfcBearing | 60.0 | 70.0 | IRHD | Major |
| MAT-011 | Bearing elastomer shear modulus | §5.5.2 | IfcBearing | 0.9 | 1.2 | MPa | Major |
| MAT-012 | Expansion joint sealant bond strength | §5.6.1 | IfcBuildingElementProxy | 1.0 | — | MPa | Minor |
| MAT-013 | Waterproofing membrane thickness | §5.7.1 | IfcCovering | 4.0 | — | mm | Minor |
| MAT-014 | Structural steel yield strength (diaphragm) | §5.8.1 | IfcMember | 275.0 | — | MPa | Major |
| MAT-015 | Grout compressive strength (bearing pad) | §5.5.3 | IfcBearing | 40.0 | — | MPa | Critical |

---

## C. Regulatory Requirement Rules (REG-001 – REG-025)

| Rule ID | Description | Source | Target Class | Validation Method | Severity |
|---------|-------------|--------|--------------|-------------------|----------|
| REG-001 | IfcProject must have GlobalId | ISO 19650-1 §4.2 | IfcProject | SemanticCheck | Critical |
| REG-002 | Elements must have IfcClassification | ISO 19650-1 §5.1 | IfcElement | SemanticCheck | Critical |
| REG-003 | Element Name must be non-empty | KDS §3.1 | IfcElement | PropertySetValidation | Major |
| REG-004 | Element Description must be non-empty | KDS §3.1 | IfcElement | PropertySetValidation | Minor |
| REG-005 | Installation date must be present | ISO 19650-1 §6.3 | IfcElement | PropertySetValidation | Critical |
| REG-006 | Inspection record ref (PSC girders) | KDS §7.1 | IfcBeam | PropertySetValidation | Critical |
| REG-007 | Concrete mix reference must exist | KDS §5.1 | IfcBeam | PropertySetValidation | Critical |
| REG-008 | Prestress record must be linked | KDS §5.3.4 | IfcTendon | PropertySetValidation | Critical |
| REG-009 | Load test certificate (bearings) | KDS §5.5.4 | IfcBearing | PropertySetValidation | Major |
| REG-010 | Survey date within 30 days of TLS | ISO 19650-1 §7.2 | IfcElement | DateValidation | Major |
| REG-011 | IfcSite must include GPS coordinates | ISO 19650-1 §4.3 | IfcSite | SemanticCheck | Minor |
| REG-012 | IfcBeam assigned to one IfcBridgePart | KDS §3.2 | IfcBeam | SemanticCheck | Major |
| REG-013 | Concrete batch test report reference | KDS §5.2.5 | IfcBeam | PropertySetValidation | Critical |
| REG-014 | Steel certification document ref | KDS §5.4.3 | IfcReinforcingBar | PropertySetValidation | Critical |
| REG-015 | Waterproofing certificate (deck slab) | KDS §5.7.2 | IfcSlab | PropertySetValidation | Major |
| REG-016 | Expansion joint product approval doc | KDS §5.6.2 | IfcBuildingElementProxy | PropertySetValidation | Major |
| REG-017 | IfcElement must have valid OwnerHistory | ISO 19650-1 §4.4 | IfcElement | SemanticCheck | Minor |
| REG-018 | MVD: IfcBeam must have Pset_BeamCommon | ISO 19650-1 §5.2 | IfcBeam | MVDValidation | Major |
| REG-019 | MVD: IfcColumn must have Pset_ColumnCommon | ISO 19650-1 §5.2 | IfcColumn | MVDValidation | Major |
| REG-020 | MVD: IfcSlab must have Pset_SlabCommon | ISO 19650-1 §5.2 | IfcSlab | MVDValidation | Major |
| REG-021 | Quality control plan ref in IfcProject | KDS §7.2 | IfcProject | PropertySetValidation | Critical |
| REG-022 | Corrective action record for non-conformances | ISO 19650-1 §8.1 | IfcElement | PropertySetValidation | Critical |
| REG-023 | Handover package mandatory Psets populated | ISO 19650-1 §9.1 | IfcElement | PropertySetValidation | Critical |
| REG-024 | Design revision history traceable | ISO 19650-1 §6.2 | IfcElement | SemanticCheck | Minor |
| REG-025 | IFC schema version must be IFC4X3 | ISO 19650-1 §4.1 | IfcProject | SemanticCheck | Critical |
