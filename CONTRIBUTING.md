# Contributing to OpenPrint3D

Thank you for your interest in contributing!  
OpenPrint3D is an early-stage, community-driven project that defines open, slicer-independent formats for:

- **Printer** profiles  
- **Filament** profiles  
- **Process** profiles  

To keep contributions consistent and interoperable, please follow the guidelines below.

---

## 📁 Repository Structure

```text
schema/        → JSON Schema definitions (printer, filament, process)
printer/       → Printer profile instances
filament/      → Filament profile instances
process/       → Process profile instances
tools/         → Validation and development helpers
```

✅ 1. Install Dependencies
You only need one Python package:
```bash
pip install jsonschema
```

✅ 2. Validate Before Submitting
Use the provided tool:
```bash
python tools/validate_schema.py schema/<schema-file>.json <your-profile>.json
```

### Examples

Validate a filament profile:
```bash 
python tools/validate_schema.py schema/filament.schema.json filament/Polymaker/PolyLite-PLA.json
```

Validate a printer profile:
```bash
python tools/validate_schema.py schema/printer.schema.json printer/Elegoo/Centauri-Carbon.json
```

Validate a process profile:
```bash
python tools/validate_schema.py schema/process.schema.json process/Standard/0.20mm-quality.json
```

If valid, you’ll see:
```bash
[ OK ] path/to/your-file.json
```
