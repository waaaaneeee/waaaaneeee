# bibimbyte

**Software Engineer — Application Security & Backend Systems**

Technical interests in backend trust boundaries, operating-system isolation, and memory safety.

**Application / Database Boundary**

```text
untrusted client    | application                  | PostgreSQL
                    |                              |
request ------------|-> handler                    |
                    |   authenticate / authorize   |
                    |   validate input             |
                    |   parameterized SQL ---------|-> query execution
                    |                              |   role privileges
                    |                              |   row policies (if enabled)
                    |                              |   constraints / transactions
```

**User / Kernel Boundary**

```text
user space          | kernel space (Linux)
                    |
process -- syscall -|-> syscall entry
                    |   seccomp filter (if configured)
                    |   syscall handler
                    |     argument / permission checks
                    |     uaccess helpers where needed
process <-----------|-- result / error code
           privilege boundary
```

## Engineering Focus

**Systems Security**\
Limiting process authority through syscall filters, capability restrictions, and isolated namespace views.

**Binary Exploitation**\
Memory corruption as a route to control-flow hijacking, and the constraints imposed by exploit mitigations.

**Kernel Internals**\
Linux syscall paths and virtual memory, with attention to page-table permissions and user/kernel isolation.

**Memory Safety**\
Ownership, lifetimes, and the invariants required at unsafe code and FFI boundaries.

**Reverse Engineering**\
Recovering program behavior from ELF binaries through x86-64 disassembly and System V ABI conventions.

**Secure Backend Architecture**\
Application authorization and least-privilege database access, with constraints and transactions preserving data integrity.

---

*Repositories are restricted from public access due to the potential misuse of security-sensitive implementations.*
