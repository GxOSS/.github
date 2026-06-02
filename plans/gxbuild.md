- Make build always create a fresh skeleton
- Adjust skeleton for JTAG
- Rewrite blocks.rs
- Make assemble_* type-agnostic and remove xell/rebooter
- Remove the core priority queue system and just build a settings struct

New build sysem:
- Parse input nand into skeleton, build new settings struct, extract assets to memory
- Overlay options.ini and then cli options ontop
- Perform inisearch and extract assets to memory
- Rank assets and error if no valid candidate
- Patch assets as necessary 
- Create blank nand skeleton, apply settings and build