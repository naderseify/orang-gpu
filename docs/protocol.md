# 📡 USB Protocol Specification

## Device Identification

**Vendor ID:** `0x1f3a` (Orange Pi)  
**Product ID:** `0x1010` (GPU Device)

## Endpoints

| Endpoint | Direction | Transfer Type | Purpose |
|----------|-----------|---------------|---------|
| 0x01 | OUT | Bulk | Command/Data out |
| 0x82 | IN | Bulk | Results in |
| 0x03 | OUT | Interrupt | Control out |
| 0x84 | IN | Interrupt | Status in |

## Command Packets

```c
struct gpu_command {
    uint8_t  magic;      // 0xAA
    uint8_t  cmd;        // Command ID
    uint16_t seq;        // Sequence number
    uint32_t kernel_id;  // Kernel identifier
    uint32_t global[3];  // Global work size
    uint32_t local[3];   // Local work size
    uint32_t args_size;  // Arguments size
    uint32_t crc;        // CRC32
    uint8_t  args[0];    // Variable arguments
} __attribute__((packed));
