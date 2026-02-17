
## 🔧 Detailed Documentation Files

### docs/architecture.md
```markdown
# 🏗️ Orange GPU Architecture

## System Overview

The Orange GPU project creates a virtual GPU by utilizing the Orange Pi Lite's 4× Cortex-A7 cores over USB.

## Communication Layers

### Layer 1: Physical (USB 2.0)
- **Data Channel**: Bulk transfers, 480 Mbps
- **Control Channel**: Interrupt transfers, 480 Mbps
- **Optional I2C**: 100 kHz for monitoring

### Layer 2: Protocol
See [protocol.md](protocol.md) for packet structures.

### Layer 3: Compute API
- Load kernels (NEON-optimized)
- Allocate buffers
- Execute parallel workloads
- Synchronize results
