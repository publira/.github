# Welcome to Publira

We build modern tools and ecosystems for digital publishing, focusing on e-books and webcomics (manga).

## Featured Open Source Projects

Here are some of our core open-source repositories that power our ecosystem:

### [epub](https://github.com/publira/epub)
A fast, memory-efficient EPUB parsing and generation library written in Go.
It features file-system-agnostic stream processing (`io.ReaderAt` / `io.Writer`) and strict validation compliance with major Japanese e-book formats (EBPAJ, KADOKAWA) and Kindle publishing guidelines.

### [epub-web](https://github.com/publira/epub-web)
A web application that generates fixed-layout EPUBs from image sequences and extracts images from existing EPUB files.
The backend is powered by Go, and the frontend is built with React, TypeScript, and Tailwind CSS. It is fully containerized and Docker-ready for instant deployment.

### [comic-viewer](https://github.com/publira/comic-viewer)
A highly extensible, headless-UI inspired React comic viewer designed for modern web applications.
It provides robust core functionalities such as memory-safe virtualization for high-resolution images, responsive double-page spreads, and a pluggable data pipeline for dynamic processing (e.g., WASM decryption).

## Our Vision

We are currently building a **next-generation digital publishing platform** powered by these open-source technologies. 
As our internal platform evolves, we remain committed to giving back to the community by continuing to open-source the core parsers, viewer engines, and infrastructure components that make it all possible.