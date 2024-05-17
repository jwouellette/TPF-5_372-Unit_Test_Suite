# L1-Br01-AbutmentFooting01

| Test code | Test author     | Test dataset source | Test direction |
|-----------|-----------------|---------------------|----------------|
| L1-Br01-AbutmentFooting01   | J Ouellette | TPF-5(372) | Export/Import  |

>**After completing the test description delete all the instructions (in Italic, marked with :information_source:). Including this one.**

## Intent
>:information_source: *describe the intention of the test, and (optionally) list the main IFC concepts covered.*
The intent is to test the proper IFC mapping of a bridge abutment wall/footing, including reinforcing.

<details><summary>Main IFC concept involved in this test</summary> 

- Spatial Decomposition, specifically IfcBridgePart.ABUTMENT [COMPLEX]
- Use of IfcWall for main element
- Use of IfcVoidingFeature for keyway recesses
- Use of IfcReinforcing for steel reinforcing elements
- Use of schema-based and custom properties and property sets
</details>


## Prerequisites
>:information_source: *list the tests that must be passed before performing this test. If not applicable, delete the whole "Prerequisites" section.*

All validation criteria (and usages) of prerequisites' tests shall be **verified for this test too** (regression test principle). Prerequisites for the present test case are listed below.

| Test code | Test title                     | Comments |
|-----------|--------------------------------|----------|
| PJ01      | Project Setup                  | none     |
| GL01      | Global Positioning RFI dataset | none     |



## Test dataset (input)
>:information_source: *list the input for the test. May include a reference IFC file. If dataset requires further description use the `README.md` in the Dataset folder of this test*

This test case utilises the dataset collected in the Dataset folder and summarised in the table below. **For more details on each item see [Dataset description](Dataset/README.md).**

| Filename (format)         | Description                                                        |
|---------------------------|--------------------------------------------------------------------|
| L1-Br01-AbutmentFooting01.pdf | Construction details of an Abutment, per L4-Br01 bridge design     |


## Validation criteria
>:information_source: *list the validation criteria to define the success of the test. These may include:*
>- ***Formal rules**, reference to bSI Validation Service rules (or to an IDS file)*
>- ***Informal criteria**, mainly aimed to verify “Required SW features” (see Step 3)*
>- ***Expected geometry**, to provide a visual idea of the expected result*
>- ***Control parameters**, to check the content of the model against the given dataset*

:zap: For this test case to be considered passed, **all criteria listed in this section**, and **the ones of prerequisites tests** shall be verified. :zap:

### Formal rules
>:information_source: *add link to bSI Validation Service rules or to IDS file/bSDD domain*

#### IFC standard (schema and specification)
When validated using the bSI Validation Service, the IFC must pass:
- Syntax & Schema check
- All following rules:
  - ALB002 - Alignment layout
  - ALB003 - Alignment directions
  - TBD000 - Alignment shape representation
  - TBD000 - Stationing along alignment

>:information_source: *above is just an example of how to reference rules form the bSI Validation Service. Use a placeholder when a rule is not yet defined*

#### Test case-specific checks
>:information_source: *list or copy-paste the requirements in plain language, and **point to the IDS that formalises them - where applicable***

Link to IDS file: [ABCD123.ids]() :construction:

- There must be 1 instance(s) of `IfcWall` and must be named `AbutmentFooting_N`, its PredefinedType must be `SOLIDWALL`
- There must be 5 instance(s) of `IfcVoidingFeature` and named `Keyway01` thru `Keyway05`, their PredefinedType must be `CUTOUT`
- There must be 1 instance(s) of `IfcBridgePart` and must be named `Abutment_N`, its PredefinedType must be `ABUTMENT`, CompositionType must be `COMPLEX`
- There must be x instances of IfcReinforcingBar... type xx
- There must be x instances of IfcReinforcingBar... type xx
- There must be x instances of IfcReinforcingBar... type xx
- There must be x instances of IfcReinforcingBar... type xx
- 

>:information_source: *above is just an example of plain language requirements. Note how the last one can be either listed as IFC-agnostic requirement, or can be specified in an IFC-fashioned way. It's up to the test case owner to decide.*

### Informal criteria
>:information_source: *list informal criteria, or refer to external documentation*

...

### Expected geometry
>:information_source: *add image of the expected geometry. Upload the jpeg/png file in the Dataset folder of this test*

...

### Control parameters
>:information_source: *add parameters/data that can be use to support the validation of import into a receiving application. Example: total lenght of one alignment, coordinates for end point of the alignment.*

...

## Link to requirements
>:information_source: *list requirements covered by this test, or refer to external documentation*

...
