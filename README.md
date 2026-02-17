# 🍊 Orange GPU - Turn Your Orange Pi into a USB GPU

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)]()
[![GitHub stars](https://img.shields.io/github/stars/yourusername/orang-gpu)]()

**Turn a $15 Orange Pi Lite into a USB GPU accelerator for your Raspberry Pi!**

## 🎯 Overview

Orange GPU transforms an Orange Pi Lite into a virtual GPU that connects via **dual USB 2.0** (480 Mbps each) to a Raspberry Pi. It appears as a `/dev/orang` device and can accelerate:
- Matrix operations (for LLM inference)
- Neural network computations
- Custom parallel workloads

## ✨ Features

- ⚡ **Dual USB 2.0** - 960 Mbps aggregate bandwidth
- 🧮 **NEON optimized** - Full ARM Cortex-A7 SIMD utilization
- 🔧 **U-Boot based** - Bare-metal performance, no Linux overhead
- 🔌 **Hot-pluggable** - Dynamic device attachment/detachment
- 📊 **Real-time monitoring** - Temperature, load, memory usage via I2C
- 🎯 **OpenCL-like API** - Familiar programming model

## 🏗️ Architecture

