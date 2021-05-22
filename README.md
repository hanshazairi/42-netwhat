# 42cursus - netwhat

## Internet Protocol (IP)
- IPv4 addresses are 32 bits long *(4,294,967,296 or 2^32 addresses)*
- IPv6 addresses are 128 bits long *(3.4E38 addresses)*

### IPv4 Address Classes
| *Class* | *Address Range*                 | *Number of Networks* | *Addresses per Network* | *Number of Addresses*   |
| :-----: | :-----------------------------: | :------------------: | :---------------------: | :---------------------: |
| Class A | `0.0.0.0` - `127.255.255.255`   | 128 *(2^7)*          | 16,777,216 *(2^24)*     | 2,147,483,648 *(2^31)*  |
| Class B | `128.0.0.0` - `191.255.255.255` | 16,384 *(2^14)*      | 65,536 *(2^16)*         | 1,073,741,824 *(2^30)*  |
| Class C | `192.0.0.0` - `223.255.255.255` | 2,097,152 *(2^21)*   | 256 *(2^8)*             | 536,870,912 *(2^29)*    |
| Class D | `224.0.0.0` - `239.255.255.255` | *Undefined*          | *Undefined*             | 268,435,456 *(2^28)*    |
| Class E | `240.0.0.0` - `255.255.255.255` | *Undefined*          | *Undefined*             | 268,435,456 *(2^28)*    |

### Private IPv4 Addresses
1. `10.0.0.0` - `10.255.255.255`
2. `172.16.0.0` - `172.31.255.255`
3. `192.168.0.0` - `192.168.255.255`

## Netmask
- 32-bit binary mask used to divide an IPv4 address into subnets
- First `x.x.x.0` address in the subnet is the assigned network address
- Last `x.x.x.255` address in the subnet is the assigned broadcast addressx

### IPv4 Address Default Netmask
| *Class* | *Default Netmask*       | *CIDR Notation* |
| :-----: | :---------------------: | :-------------: |
| Class A | `255.0.0.0`             | `/8`            |
| Class B | `255.255.0.0`           | `/16`           |
| Class C | `255.255.255.0`         | `/24`           |
| Class D | *Undefined*             | *Undefined*     |
| Class E | *Undefined*             | *Undefined*     |

## Transmission Control Protocol (TCP)
- Connection-oriented protocol
- Does not support broadcasting
- Comparatively slower than UDP
- Reliable and guarantees delivery of data to destination
- Sequences data; packets arrive in-order at the receiver
- Extensive error checking mechanism; provides flow control & acknowledgment of data

## User Datagram Protocol (UDP)
- Datagram-oriented protocol
- Supports broadcasting
- Faster, simpler & more efficient than TCP
- Delivery of data to destination cannot be guaranteed in UDP
- No sequencing of data; has to be managed by application layer if ordering is required
- Only has basic error checking mechanism using checksums

## Open Systems Interconnection (OSI) Model
1. Application Layer
2. Presentation Layer
3. Session Layer
4. Transport Layer
5. Network Layer
6. Data Link Layer
7. Physical Layer

## Dynamic Host Configuration Protocol (DHCP)
- Used for both IPv4 & IPv6
- Uses UDP as its transport protocol
- Automates IP configuration, including IP address, subnet mask, default gateway & DNS information

## Domain Name System (DNS)
- Translates internet domain and host names to IP address

## Ping
- Operates by sending *Internet Control Message Protocol (ICMP)* echo request packets to target host and waiting for ICMP echo reply
- `ping localhost` or `ping 127.0.0.1` to test IP stack
