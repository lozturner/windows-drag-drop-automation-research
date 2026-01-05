# Windows Drag-and-Drop & Input Automation Stack 🖱️💻

Deep research into Windows drag-and-drop automation using ShareX, Miro, and various automation tools.

## 🎯 Research Overview

This repository contains research and findings on automating Windows drag-and-drop operations, including:

### 1. ShareX Integration 📸

![ShareX Developer View](https://pplx-res.cloudinary.com/image/upload/v1738450991/user_uploads/zldjgbqpn/image.jpg)

**Key Technologies:**
- ⚡ ShareX automation capabilities
- 🔧 IDropTarget interface implementation
- 📊 Real-time event monitoring
- 🐛 Debug console integration

### 2. Core Windows API Components 🔌

```
┌─────────────────────────────────────┐
│   Windows Drag-Drop Architecture    │
├─────────────────────────────────────┤
│                                     │
│  IDropTarget::DragEnter()          │
│           ↓                         │
│  IDataObject enumeration           │
│           ↓                         │
│  grfKeyState=MK_LBUTTON           │
│           ↓                         │
│  pdwEffect=DROPEFFECT_COPY        │
│                                     │
└─────────────────────────────────────┘
```

![Drag-Drop Operation Live View](https://pplx-res.cloudinary.com/image/upload/v1738450994/user_uploads/zjybzkvuc/image.jpg)

### 3. Real-Time Developer View 🔍

This shows the actual desktop with ShareX on the left, drag gesture in progress, Miro receiving on the right, with debug console showing live hook messages:

**Live Event Stream:**
- `IDropTarget::DragEnter()` called
- `IDataObject` enumeration
- `grfKeyState=MK_LBUTTON`
- `pdwEffect=DROPEFFECT_COPY`

![ShareX and Miro Integration](https://pplx-res.cloudinary.com/image/upload/v1738450998/user_uploads/btzksvbps/image.jpg)

## 🛠️ Technical Stack

### Required Components:
- **ShareX** - Screen capture & automation
- **Miro** - Receiving application
- **Windows API** - Drag-drop interfaces
- **Debug Tools** - Real-time monitoring

### Key Interfaces:
- `IDropTarget`
- `IDataObject`
- `DragEnter`
- `DragOver`
- `Drop`

## 📋 Implementation Notes

1. **Hook Installation**: Monitor at system level
2. **Event Tracking**: Capture all drag-drop events
3. **State Management**: Track `grfKeyState` flags
4. **Effect Handling**: Manage `DROPEFFECT_COPY` operations

## 🚀 Use Cases

- Automated screenshot workflows
- Batch file operations
- Integration testing
- UI automation
- Development debugging

## 📚 References

- Windows Drag-Drop API Documentation
- ShareX Automation Guide
- IDropTarget Interface Specification

---

*Research conducted using live debugging and real-time monitoring tools* 🔬
