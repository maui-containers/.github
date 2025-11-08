# .NET MAUI Containers

**Containerized and virtualized environments for .NET MAUI development, testing, and CI/CD across all platforms.**

---

## 🎯 Purpose

The **maui-containers** organization provides pre-built, reproducible environments for .NET MAUI developers — spanning **Docker images** (Linux/Windows) and **macOS virtual machines** (via Tart).  
Each image is optimized for building, testing, and shipping .NET MAUI apps without the pain of manually configuring SDKs, workloads, or emulators.

---

## 🧩 What’s Inside

| Category | Description |
|-----------|--------------|
| 🐳 **Docker Images** | Cross-platform MAUI build/test environments for Linux and Windows. |
| 🍏 **Tart macOS VMs** | macOS VM images with Xcode and MAUI workloads for iOS/macOS builds. |
| 🧪 **Test Images** | Android Emulator + Appium automation for UI testing. |
| ⚙️ **Provisioning Scripts** | Unified scripts for image creation and workload setup. |

All images are published under the `maui-containers` org on Docker Hub and GHCR.

---

## 🚀 Quick Start

### Development Container
```bash
docker run -it maui-containers/maui-linux:dotnet10.0 bash
```

### GitHub Actions Runner
```bash
docker run -d   -e GITHUB_TOKEN=your_token   -e GITHUB_ORG=your_org   -e GITHUB_REPO=your_repo   maui-containers/maui-linux:dotnet10.0
```

### macOS VM (Tart)
```bash
tart clone ghcr.io/maui-containers/maui-macos:tahoe-dotnet10.0 maui-dev
tart run maui-dev
```

---

## 🏷 Tagging Convention

```
{platform}-dotnet{version}-workloads{version}
```

Examples:
- `maui-linux:dotnet10.0`
- `maui-macos:tahoe-dotnet9.0`
- `maui-emulator-linux:android34-dotnet9.0`

---

## ✅ Common Features

- .NET SDK + MAUI workloads  
- Android SDK + OpenJDK  
- PowerShell + Git + Dev tools  
- GitHub & Gitea runners  
- (macOS) Xcode + iOS/tvOS simulators

---

## 🤝 Contributing

We welcome contributions!  
Check out our contribution guide and propose enhancements for new platforms, base images, or CI automation scripts.

---

## TL;DR

**maui-containers** gives .NET MAUI developers production-ready Docker and VM environments for everything from local builds to cloud CI runners — unified, consistent, and tuned for cross-platform productivity.
