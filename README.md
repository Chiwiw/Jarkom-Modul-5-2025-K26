# Jarkom-Modul5-2025-K26

| Nama | NRP |
|------|-----|
| Hanif Mawla Faizi | 5027241064 |
| Fika Arka Nuriyah | 5027241071 |

# Misi 1 :
## 1. Identifikasi Perangkat:
- Narya: Berfungsi sebagai DNS Server.
- Vilya: Berfungsi sebagai DHCP Server.
- Web Servers: Palantir  dan IronHills.
- Client (Pasukan):
  - Khamul: 5 host (Target/Burnice).
  - Cirdan: 20 host (Lycaon).
  - Isildur: 30 host (Policeboo).
  - Durin: 50 host (Caesar).
  - Gilgalad: 100 host (Ellen).
  - Elendil: 200 host (Jane).


## 2. Pembagian IP VLSM dan Subnet Tree.
**Topologi :**
![WhatsApp Image 2025-11-30 at 22 53 14_cfb69939](https://github.com/user-attachments/assets/5b3ba8b7-1a56-439b-b174-79a65defd812)

Dari topologi dan kebutuhan hsot per client tersebut, kami **membagi subnet** nya menjadi seperti berikut :
![WhatsApp Image 2025-11-30 at 22 32 18_0afb9982](https://github.com/user-attachments/assets/cf73f840-9f68-4167-8c78-8db29ada7cde)

### Tabel VLSM 
| **Subnet**      | **Jaringan**           | **Prefix**     | **Gateway**     | **Broadcast**    | **Range IP**       | **Kebutuhan Host** | **Jumlah IP** | **Netmask**           |
|-----------------|----------------------------------|--------------------|-----------------|------------------|---------------------------|--------------------|----------------|-----------------------|
| **A5**          | (Elendil, Isildur) > Switch > Minastir | 192.224.1.0/24     | 192.224.1.1     | 192.224.1.255    | 192.224.1.1 - 192.224.1.200 | 231                | 256            | 255.255.255.0        |
| **A6**          | (Gilgalad, Cirdan) > Switch > AnduinBanks | 192.224.2.0/25     | 192.224.2.1     | 192.224.2.127    | 192.224.2.1 - 192.224.2.126 | 121                | 128            | 255.255.255.128      |
| **A2**          | Durin > Wilderland               | 192.224.2.128/26   | 192.224.2.129   | 192.224.2.191    | 192.224.2.129 - 192.224.2.190 | 51                 | 64             | 255.255.255.192      |
| **A3**          | Khamul > Switch > Wilderland     | 192.224.2.192/29   | 192.224.2.193   | 192.224.2.199    | 192.224.2.193 - 192.224.2.198 | 6                  | 8              | 255.255.255.248      |
| **A4**          | (Vilya, Narya) > Switch > Rivendell | 192.224.2.200/29   | 192.224.2.201   | 192.224.2.207    | 192.224.2.201 - 192.224.2.206 | 3                  | 8              | 255.255.255.248      |
| **A1**          | IronHills > Switch > Moria       | 192.224.2.208/30   | 192.224.2.209   | 192.224.2.211    | 192.224.2.209 - 192.224.2.210 | 2                  | 4              | 255.255.255.252      |
| **A7**          | Wilderland > Moria               | 192.224.2.212/30   | 192.224.2.213   | 192.224.2.215    | 192.224.2.213 - 192.224.2.214 | 2                  | 4              | 255.255.255.252      |
| **A8**          | Palantir > Pelargir              | 192.224.2.216/30   | 192.224.2.217   | 192.224.2.219    | 192.224.2.217 - 192.224.2.218 | 2                  | 4              | 255.255.255.252      |
| **A9**          | AnduinBanks > Pelargir           | 192.224.2.220/30   | 192.224.2.221   | 192.224.2.223    | 192.224.2.221 - 192.224.2.222 | 2                  | 4              | 255.255.255.252      |
| **A10**         | Pelargir > Minastir              | 192.224.2.224/30   | 192.224.2.225   | 192.224.2.227    | 192.224.2.225 - 192.224.2.226 | 2                  | 4              | 255.255.255.252      |
| **A11**         | Moria > Osgiliath                | 192.224.2.228/30   | 192.224.2.229   | 192.224.2.231    | 192.224.2.229 - 192.224.2.230 | 2                  | 4              | 255.255.255.252      |
| **A12**         | Rivendell > Osgiliath            | 192.224.2.232/30   | 192.224.2.233   | 192.224.2.235    | 192.224.2.233 - 192.224.2.234 | 2                  | 4              | 255.255.255.252      |
| **A13**         | Minastir > Osgiliath             | 192.224.2.236/30   | 192.224.2.237   | 192.224.2.239    | 192.224.2.237 - 192.224.2.238 | 2                  | 4              | 255.255.255.252      |


### Subnet Tree 
<img width="1629" height="1021" alt="Subnet Tree fix drawio" src="https://github.com/user-attachments/assets/fcc4823c-6c8a-430d-a82a-a5b924fa621d" />

