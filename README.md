# poc-cadquery-2026-04-17

programmatic 3D CAD modeling with CadQuery

## what i built

a parametric Python script that generates a 3D model using CadQuery, showing how design-as-code enables rapid iteration. the POC creates an L-shaped mounting bracket with adjustable dimensions and parametrically-positioned mounting holes.

## the finding

CadQuery abstracts away OCP (OpenCascade) complexity through method chaining and a pythonic API. the surprising insight: you can express 3D design intent in ~30 lines of code that would take 10x longer in traditional CAD tools. the parametric nature (width, height, hole_diameter as function arguments) enables rapid iteration and design exploration that's impossible in GUI-based CAD.

## how to run

```bash
pip install -r requirements.txt
python main.py
```

outputs a bracket.step file (3D model in STEP format) that can be imported into any CAD software.

## notes

- CadQuery's method chaining (fluent API) is the abstraction that enables rapid iteration
- design-as-code means you can version control your designs (git), parameterize them, and generate variations programmatically
- STEP export makes it compatible with industry-standard CAD software
- limitations: complex surface modeling is harder than parametric solids; visualization is limited without external viewers

