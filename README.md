# kubectl-node-debug

**kubectl-node-debug** is a Krew plugin that allows you to select a Kubernetes node interactively using `fzf` and start a debug session with `kubectl debug`. The session automatically enters `chroot /host` for troubleshooting.

## ✨ Features
- 🔹 **Interactive fzf-based node selection**
- 🚀 **Seamless debugging** using `kubectl debug`
- 🖥️ **Auto `chroot /host` execution** inside the debug shell

## 📌 Installation

### Install via Krew
```sh
kubectl krew install node-debug
```

### Manual Installation
1. Download the latest release from [GitHub Releases](https://github.com/tayeh/kubectl-node-debug/releases).
2. Extract and move the binary to `/usr/local/bin`:
   ```sh
   tar -xzvf kubectl-node-debug.tar.gz
   chmod +x kubectl-node-debug
   mv kubectl-node-debug /usr/local/bin/
   ```
3. Verify installation:
   ```sh
   kubectl node-debug --help
   ```

## 🚀 Usage
Simply run:
```sh
kubectl node-debug
```
1. Select a node.
2. The tool opens a debug shell on the selected node.
3. Automatically enters `chroot /host`.

### Example:
```sh
kubectl node-debug
```
```
🔹 Select a Node:
▶ ip-10-0-129-51.compute.internal
```

🔹 Now you're inside the debug shell of the selected node!

## 🛠️ Uninstallation
```sh
kubectl krew uninstall node-debug
```

## 🤝 Contributing
Feel free to open issues or PRs on [GitHub](https://github.com/tayeh/kubectl-node-debug)!

---
🚀 **Happy debugging!**

