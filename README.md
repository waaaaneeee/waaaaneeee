# bibimbyte

**Software Engineer — Application Security & Backend Systems**

Backend systems. Low-level security research. Trust boundaries enforced from application logic to kernel interfaces.

```text
untrusted  :  application     :   database
           :                  :
request ----> route handler ----> PostgreSQL
webhook    :  validate        :   row-level security
upload     :  authenticate    :   constraints
           :  authorize       :   audit trail
    trust boundary     trust boundary
```

**Memory & Privilege Boundaries**

```text
checked    :  unchecked       :   privileged
           :                  :
Rust -------> unsafe, FFI ------> kernel
ownership  :  raw pointers    :   syscall ABI
lifetimes  :  C ABI           :   page permissions
           :  invariants      :   seccomp
    unsafe boundary  privilege boundary
```

## Engineering Focus

**01 / Memory Safety & Unsafe Boundaries**\
Ownership semantics. Safety contracts. FFI boundaries. Explicit memory invariants.

**02 / Binary Analysis & Executable Internals**\
ELF internals. System V ABI. x86-64 assembly. Loader behavior and execution flow.

**03 / Privilege Separation**\
System call surface. Process isolation. Linux capabilities. Seccomp filtering.

**04 / Secure Backend Architecture**\
Least privilege. Database-enforced authorization. Transactional integrity. Defense in depth.

---

*Repositories are restricted from public access due to the potential misuse of security-sensitive implementations.*
