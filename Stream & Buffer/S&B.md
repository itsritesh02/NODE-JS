## What is Stream in Node.js?

A Stream is used to **read or write data in small chunks** instead of loading the entire data at once.

### Simple Example

If we have a large video file, Stream reads it **piece by piece**.

```text
Large File
   ↓
Chunk 1 → Chunk 2 → Chunk 3 → Chunk 4


## What is Buffer in Node.js?

Buffer is a temporary memory area used to store **binary data**.

It is commonly used when working with:
- Files
- Streams
- Network operations

### Simple Example

When data comes in small chunks, Buffer temporarily stores that data before processing.

```text
Data → Buffer → Process