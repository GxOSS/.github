- Add nand preprocessor to core
- Remove nand parser from builder
- Make build always create a fresh skeleton
- Adjust skeleton for JTAG
- Rewrite blocks.rs
- Make assemble_* type-agnostic and remove xell/rebooter
- Remove the core priority queue system and just build an options struct

New build sysem:
- Preprocess nand, assets and stfs
- Apply xeini and optini to skeleton with data
- Build logical 512+16 image, joins blocks if needed
- Add ecc data, verify, apply blockmap, and return
