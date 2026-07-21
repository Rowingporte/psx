# POSIX Qualification Specs

RTEMS pre-qualification specification items (`if/` interface + `req/` requirement)
for the POSIX / libc functions in the POSIX-Qual function list — 133 functions
across mutexes, condition variables, semaphores, message queues, spinlocks,
pthread attributes/lifecycle/scheduling/keys, POSIX time, ctype, string/memory,
and environment.

## Layout

```
spec/c/if/    118 interface items   (interface-type: unspecified-function/object/define)
spec/c/req/   122 requirement items (action requirements: pre/post-conditions + transition-map)
```

Each `req/` item is grounded in the actual `cpukit` source behavior (return codes,
error conditions) and validates clean under `specwareverify`.

## Notes

- These items reference base RTEMS interface items (e.g. `../if/einval`,
  `../if/pthread`, `../if/group`) provided by the RTEMS `rtems-package` /
  `rtems-central` spec tree; drop these files into that tree's `spec/c/` to
  build/validate them.
- Generated for RTEMS 6 (gr740 / SPARC LEON qualification target).

Licensed CC-BY-SA-4.0 OR BSD-2-Clause (matching the RTEMS spec corpus).
