# Welcome to Publira

Publira builds digital publishing for comics in the open: a publishing platform, and the e-book and comic libraries and tools that grew out of it. Every project below is open source.

## The platform

### [publira](https://github.com/publira/publira)

A multi-tenant SaaS that gives publishers with limited IT resources a digital distribution platform for comics, which they can run under their own brand. Publishers and editors register the book information they receive from creators, and readers read it on the web or on mobile. It is built for portability, ease of operation, and freedom from vendor lock-in.

## Libraries and tools

Independently useful projects that grew out of the platform.

### [epub](https://github.com/publira/epub)

A Go library for decoding, encoding, and validating EPUB 3 files. It is built around `io.ReaderAt` and `io.Writer` rather than a filesystem, opens assets on demand to keep memory use low, and validates against EBPAJ- and KADOKAWA-style conventions.

### [comic-viewer](https://github.com/publira/comic-viewer)

A highly extensible, headless-UI inspired React comic viewer. It provides memory-safe virtualization of high-resolution pages, responsive single and double-page spreads, RTL and LTR reading directions, and a plugin API for custom data pipelines, while leaving the UI to you.

### [epub-web](https://github.com/publira/epub-web)

A web application that builds fixed-layout EPUBs from a set of images and extracts the images back out of an existing EPUB. Go on the backend, React and TypeScript on the frontend, and a container image ready to run.

### [next-cache-handlers](https://github.com/publira/next-cache-handlers)

A Redis-backed Next.js `cacheHandler` and `cacheHandlers` for self-hosted, multi-instance deployments. Every instance shares one server cache, covering `"use cache"`, ISR, and tag revalidation, and it works with Valkey as well as Redis. Published on npm as [`@publira/next-cache-handlers`](https://www.npmjs.com/package/@publira/next-cache-handlers).

## Our Vision

We are building a next-generation digital publishing platform in the open. The platform is open source alongside the parsers, viewer engines, and infrastructure components that make it work, so that a publisher can adopt it, run it, and adapt it without depending on us.
