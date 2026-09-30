# OpenCircuit HDL Playground

A browser-based Verilog learning and rapid-experiment environment with a real parser, expression compiler, cycle simulator, waveform renderer, and VCD exporter. Everything runs locally in the browser; source code is never uploaded.

## Features

- Verilog module parsing with line-aware diagnostics.
- Scalar and vector signals up to 32 bits.
- Binary, decimal, octal, and hexadecimal literals.
- Arithmetic, bitwise, shift, equality, logical, unary, and ternary expressions.
- Continuous `assign` statements with fixed-point settling and loop detection.
- `always @(posedge clock)` blocks with simultaneous nonblocking updates.
- JSON input vectors for combinational and sequential designs.
- Responsive multibit/single-bit SVG waveform rendering.
- Standard VCD download for GTKWave, Surfer, and other viewers.
- Included counter and combinational examples.

## Live application

https://opencircuitlabs.github.io/hdl-playground/

## Development

```bash
npm install
npm test
```

The app has no runtime dependencies or build step. Serve the repository root with any static HTTP server.

## Supported subset

This project is deliberately a deterministic educational Verilog subset, not an IEEE SystemVerilog simulator. It supports separate signal declarations, continuous assignments, expression evaluation, and simple positive-edge sequential blocks. It rejects unsupported syntax rather than guessing. Full Verilog/SystemVerilog projects should use Verilator, Icarus Verilog, or another standards-compliant simulator.

## License

MIT © 2026 OpenCircuitLabs
