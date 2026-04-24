# Simple HTTP Server

Prerequisites: basic programming, understanding of processes and I/O  

---

## The Foundation
TCP/IP Networking and Application-Layer Protocols:  
Understanding how reliable communication is established over sockets and how higher-level protocols like HTTP structure requests and responses on top of raw byte streams.

---

## Learning Outcomes
1. Manual handling of TCP socket connections, including binding, listening, and accepting client requests.  
2. Parsing and constructing HTTP/1.0 or HTTP/1.1 requests and responses using raw text-based protocol rules.  
3. Understanding request-response lifecycle, headers, status codes, and basic content serving.  
4. Exposure to concurrency models (optional): handling multiple clients via blocking, threading, or simple multiplexing.

---

## Reference Material
- [RFC 2616 / RFC 7230–7235 (HTTP/1.1 specifications)](https://www.rfc-editor.org/rfc/rfc2616)
- [Beej’s Guide to Network Programming](https://beej.us/guide/bgnet/)
- Computer Networking: A Top-Down Approach — Kurose & Ross (Application Layer chapters)

---

## Scope & Constraints
- Use only low-level socket APIs (no frameworks like Express, Flask, etc.)
- Do not use existing HTTP server libraries
- Handle only basic HTTP methods (GET is sufficient)
- Serve static files from a local directory
- All request parsing must be done manually (string/byte parsing)
- Keep implementation minimal and self-contained

---

## Acceptance Criteria
- The server must:
  - accept TCP connections on a specified port  
  - correctly parse a basic HTTP GET request  
  - respond with valid HTTP headers and body  
  - serve a static file (e.g., index.html)  
  - return appropriate status codes (200, 404 at minimum)  

Test case:

> Running the server locally and accessing `http://localhost:<port>` in a browser must return a valid HTML page. Requesting a non-existent file must return a valid 404 response.
