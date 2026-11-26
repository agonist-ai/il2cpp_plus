> **Fork notice — agonist-ai, branch `6000.6.x`.** This repository is a fork of [focus-creative-games/il2cpp_plus](https://github.com/focus-creative-games/il2cpp_plus) by Code Philosophy (walon and the HybridCLR contributors), MIT licence (see `LICENSE`); all upstream authorship and history are kept. Branch `6000.6.x` ports HybridCLR v8.15 (`v6000.5.x-8.15.0`) to Unity 6000.6 (libil2cpp 6000.6.0b3) for Agonist Development AB and adds a load gate (only bytes whose SHA-256 was registered by a verified delivery are loaded; a one-way "built-in code only" switch). HybridCLR interprets bytecode only: no JIT, no executable memory, no dylib. Port notes: commit d77328a (manual port of vm/Class.cpp, vm/GlobalMetadata.*, vm/MetadataCache.cpp, vm/Runtime.cpp).

# il2cpp_plus

原始il2cpp是AOT运行时，不支持动态注册dll元数据。我们轻微改造了metadata管理模块，插入了一些hook代码，支持动态加载dll元数据。

注意，此项目代码不能单独工作，甚至无法成功编译。必须配合 [HybridCLR](https://github.com/focus-creative-games/hybridclr) 解释器才能正常工作。

main分支不包含任何代码，请切到正确的版本。
