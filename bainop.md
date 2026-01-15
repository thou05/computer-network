
## Dạng 1
### IPv4: 231.58.197.46/23
- Số bit dùng cho phần mạng: `23`
- Số bit dùng cho phần host: `32 - 23 = 9`
- Số lượng địa chỉ dùng gán cho các hosts: 510
- Mặt nạ mạng con ở định dạng nhị phân: 
	`11111111 | 11111111 | 11111110 | 00000000`
- Mặt nạ mạng con ở dạng thập phân chấm: `255.255.254.0`
- Địa chỉ mạng: `231.58.196.0/23`
- Địa chỉ host đầu tiên: `231.58.196.1/23`
- Địa chỉ host thứ hai: `231.58.196.2/23`
- Địa chỉ host cuối cùng: `231.58.197.254/23`
- Địa chỉ quảng bá: `231.58.197.255/23`

### IPv4: 14.75.189.236/25
- Số bit dùng cho phần mạng: `25`
- Số bit dùng cho phần host: `7`
- Số lượng địa chỉ dùng gán cho các hosts: 126
- Mặt nạ mạng con ở định dạng nhị phân: 
	`11111111 | 11111111 | 11111111 | 10000000`
- Mặt nạ mạng con ở dạng thập phân chấm: `255.255.255.128`
- Địa chỉ mạng: `14.75.189.128/25`
- Địa chỉ host đầu tiên: `14.75.189.129/25`
- Địa chỉ host thứ hai: `14.75.189.130/25`
- Địa chỉ host cuối cùng: `14.75.189.254/25`
- Địa chỉ quảng bá: `14.75.189.255/25`

## Dạng 2
### IPv4 135.246.79.68/24. Chia thành bốn mạng con
- Địa chỉ mạng của địa chỉ IP hiện tại: `135.246.79.0/24`
- Số bit mượn: 2^(c-1) < 4 <= 2^c  => c = 2
- Mặt nạ mạng con mới: 
	- dạng nhị phân: `11111111 | 11111111 | 11111111 | 11000000`
	- dạng chấm: `255.255.255.192`
- Liệt kê địa chỉ các mạng con
	- Địa chỉ mạng con 1: `135.246.79.0/26`
	- Địa chỉ mạng con 2: `135.246.79.64/26`
	- Địa chỉ mạng con 3: `135.246.79.128/26`
	- Địa chỉ mạng con 4: `135.246.79.192/26`

### IPv4 203.185.207.99/23. Chia thành sáu mạng con
- Địa chỉ mạng của địa chỉ IP hiện tại: `203.185.206.0/23`
- Số bit mượn: 2^(c-1) < 6 <= 2^c  => c = 3
- Mặt nạ mạng con mới: 
	- dạng nhị phân: `11111111 | 11111111 | 11111111 | 11000000`
	- dạng chấm: `255.255.255.192`
- Liệt kê địa chỉ các mạng con
	- Địa chỉ mạng con 1: `203.285.206.0/26`
	- Địa chỉ mạng con 2: `203.285.206.64/26`
	- Địa chỉ mạng con 3: `203.285.206.128/26`
	- Địa chỉ mạng con 4: `203.285.207.0/26`
	- Địa chỉ mạng con 5: `203.285.206.192/26`
	- Địa chỉ mạng con 6: `203.285.207.64/26`


## Dạng 3
### Cho địa chỉ IPv4: 139.199.205.47/21.
- Địa chỉ mạng: `139.199.200.0/21`
- Sắp xếp VLAN theo số bits dành cho phần mạng
	- VLAN 2: /23
	- VLAN 3: /24
	- VLAN 6: /25
	- VLAN 4: /26
	- VLAN 5: /26
	- VLAN 1: /27
- Chia mạng con đáp ứng yêu cầu
	- Chia mạng ban đầu /21 thành 4 mạng con /23
		- Mạng con 1: `139.199.200.0/23` -> vlan 1
		- Mạng con 2: `139.199.202.0/23`
		- Mạng con 3: `139.199.204.0/23`
		- Mạng con 4: `139.199.206.0/23`
	- Chia 2 mạng con 2,3 /23 thành các mạng con /24
		- Mạng con 2.1: `139.199.202.0/24`  -> vlan 3
		- Mạng con 2.2: `139.199.203.0/24` 
		- Mạng con 3.1: `139.199.204.0/24`
		- Mạng con 3.2: `139.199.205.0/24`
	- Chia 2 mạng con 2.2, 3.1 /24 thành các mạng con /25
		- Mạng con 2.2.1: `139.199.203.0/25`  -> vlan 6
		- Mạng con 2.2.2: `139.199.203.128/25` 
		- Mạng con 3.1.1: `139.199.204.0/25`
		- Mạng con 3.1.1: `139.199.204.128/25` 
	- Chia 2 mạng con 2.2.2 và 3.1.1 /25 thành các mạng con /26
		- Mạng con 2.2.2.1: `139.199.203.128/26`  -> vlan 3
		- Mạng con 2.2.2.2: `139.199.203.192/26` -> vlan 5
		- Mạng con 3.1.1.1: `139.199.204.0/26`
		- Mạng con 3.1.1.2: `139.199.204.64/26`
	- Chia mạng con 3.1.1.1 /26 thành 2 mạng con /27
		- Mạng con 3.1.1.1: `139.199.204.0/27` -> vlan 1
		- Mạng con 3.1.1.1: `139.199.204.32/27`

### Cho địa chỉ IPv4: 129.140.176.24/23.
- Địa chỉ mạng: `129.140.175.0/23`
- Sắp xếp VLAN
	- VLAN 4: /24
	- VLAN 3: /25
	- VLAN 5: /25
	- VLAN 2: /26
	- VLAN 6: /26
	- VLAN 1: /27
- Chia mạng con
	- Chia mạng ban đầu /23 thành 2 mạng con /24
		- Mạng con 1: `129.140.175.0/24` -> vlan 4
		- Mạng con 2: `129.140.176.0/24`
	- Chia mạng con 2 /23 thành 2 mạng con /25
		- Mạng con 2.1: `129.140.176.0/25` -> vlan 3
		- Mạng con 2.1: `129.140.176.128/25` -> vlan 5
	- Các VLAN còn lại không còn chỗ trống để chia

## Dạng 4
### Cho dải địa chỉ IPv6: 20AB:C7D9:EF16::/48. Chia mạng này để cấp địa chỉ cho các mạng LAN
- Số hextet mượn : 64-48=16 bits = 1 hextet
- Số mạn LAN có thể được gán IPv6 từ dải địa chỉ này = 2^16
- Liệt kê địa chỉ mạng con
	- Địa chỉ mạng con 1: `20AB:C7D9:EF16::/64`
	- Địa chỉ mạng con 2: `20AB:C7D9:EF16:1::/64`
	- Địa chỉ mạng con  2^16 - 1: `20AB:C7D9:EF16:FFFE::/64`
	- Địa chỉ mạng con  2^16 : `20AB:C7D9:EF16:FFFF::/64`

### Cho dải địa chỉ IPv6: 2024:7F6E::/32. Chia mạng này để cấp địa chỉ cho các mạng LAN
- Số hextet mượn : 64-48=32 bits = 2 hextet
- Số mạn LAN có thể được gán IPv6 từ dải địa chỉ này = 2^32
- Liệt kê địa chỉ mạng con
	- Địa chỉ mạng con 1: `2024:7F6E::/64`
	- Địa chỉ mạng con 2: `2024:7F6E:1::/64`
	- Địa chỉ mạng con  2^32 - 1: `2024:7F6E:FFFF:FFFE::/64`
	- Địa chỉ mạng con  2^32 : `2024:7F6E:FFFF:FFFF::/64`