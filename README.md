predicate-cracking
==================
### Notes
1. Find the address to overwrite (e.g. "x64dbg.exe"), this address may be changed for each (re)compilation:
  ```
  00000000004015F2 | 74 24                    | je predicate-cracking.401618            |
  ```
2. copy `00000000004015F2` to `cracker/bb.py`
3. replace this `je bla bla bla` instruction with 2 `nop` instructions (same size)
4. This works because the program is waiting for user input (blocking), the patching can be done

### Reference
- [JavaScript API | Frida • A world-class dynamic instrumentation framework](https://frida.re/docs/javascript-api/)
- [Windows | Frida • A world-class dynamic instrumentation framework](https://frida.re/docs/examples/windows/)
- [**iddoeldor/frida-snippets: Hand-crafted Frida examples**](https://github.com/iddoeldor/frida-snippets#intercept-entire-module)



```
Context  : {"pc":"0x7fff4b3a1a50","sp":"0x8af528","rax":"0x7fff4b3a1a50","rcx":"0x324","rdx":"0x8af5f0","rbx":"0x8afbc8","rsp":"0x8af528","rbp":"0x8af550","rsi":"0x8af5f0","rdi":"0x10","r8":"0x10","r9":"0x10","r10":"0x0","r11":"0x246","r12":"0x10","r13":"0x8","r14":"0x0","r15":"0x0","rip":"0x7fff4b3a1a50"}
```