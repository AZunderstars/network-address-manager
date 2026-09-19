# network-address-manager

A command-line tool in C++20 for managing network addresses: single IPs,
IP ranges and subnets, and groups of them. I wrote it in three days as a
take-home task for a job application.

## What it does
- Add, find and remove named addresses
- Three address types (single IP, range, subnet) built on one `IP` base class
- Group addresses together (duplicates are rejected)
- Filter by type
- Save the whole list to a file and load it back

## How it's organized
- `AddressManager` runs the commands and lookups
- `AddressGroup` handles group membership
- All printing is in a separate `Messenger` class, so the logic doesn't mix with output

## Build and run
```bash
cmake -S . -B build
cmake --build build
./build/<target-name>
```
