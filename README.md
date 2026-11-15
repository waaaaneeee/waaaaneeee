# bibimbyte

**Software Engineer — Application Security & Backend Systems**

Technical interests in backend trust boundaries, operating-system isolation, and memory safety.

**Application / Database Boundary**

```text
untrusted client    | application                  | PostgreSQL
request ------------|-> authenticate / authorize   |
                    |   validate input             |
                    |   parameterized SQL ---------|-> query execution
                    |                              |   role privileges
                    |                              |   row policies (if enabled)
```

**User / Kernel Boundary**

```text
user space          | kernel space (Linux)
process -- syscall -|-> entry / seccomp (if configured)
                    |   handler: argument / permission checks
                    |     uaccess helpers where needed
process <-----------|-- result / error code
```

## Engineering Focus

**Systems Security**\
Process isolation through capability restrictions and namespace boundaries.

**Binary Exploitation**\
Memory-corruption primitives and the constraints imposed by exploit mitigations.

**Kernel Internals**\
Virtual memory and page-table protections in Linux.

**Memory Safety**\
Ownership and lifetime invariants across unsafe code and FFI.

**Reverse Engineering**\
ELF analysis through x86-64 disassembly and System V ABI conventions.

**Secure Backend Architecture**\
Data integrity through database constraints and transaction isolation.

---

*Repositories are restricted from public access due to the potential misuse of security-sensitive implementations.*
