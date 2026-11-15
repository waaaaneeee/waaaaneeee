# bibimbyte

**Software Engineer — Application Security & Backend Systems**

Systems security. Kernel internals. Memory safety. Trust boundaries enforced from application logic to ring 0.

```text
untrusted  :  application     :   database
           :                  :
request ----> route handler ----> PostgreSQL
webhook    :  validate        :   row-level security
upload     :  authenticate    :   constraints
           :  authorize       :   audit trail
    trust boundary     trust boundary
```

**User / Kernel Boundary**

```text
user space :  entry           :   kernel
           :                  :
process ----> syscall ----------> ring 0
ASLR, PIE  :  seccomp         :   SMEP, SMAP
W^X, CET   :  capabilities    :   KASLR
canaries   :  copy_from_user  :   page tables
   syscall boundary  privilege boundary
```

## Engineering Focus

**01 / Systems Security**\
Privilege separation. Syscall attack surface. Seccomp, capabilities, namespaces.

**02 / Binary Exploitation**\
Memory corruption primitives. Return-oriented programming. Mitigation analysis: ASLR, W^X, CET, stack canaries.

**03 / Kernel Internals**\
Syscall entry path. Virtual memory and page tables. SMEP, SMAP, KASLR.

**04 / Memory Safety**\
Ownership and lifetimes. Safety contracts. FFI boundaries. Allocator behavior.

**05 / Reverse Engineering**\
ELF layout. System V ABI. x86-64 disassembly. Control-flow recovery.

**06 / Secure Backend Architecture**\
Least privilege. Database-enforced authorization. Transactional integrity.

---

*Repositories are restricted from public access due to the potential misuse of security-sensitive implementations.*
