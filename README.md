# 🔹 Hari 3: DHCP Server dan DNS

## 🎯 Tujuan
Mempelajari dan mengimplementasikan layanan dasar jaringan:
- DHCP Server: Memberikan alamat IP secara otomatis ke perangkat jaringan
- DNS Server: Menerjemahkan nama domain menjadi alamat IP

## 🧱 Topologi
- 1 Router (Sebagai DHCP Server)
- 1 Switch
- 3 PC Client (PC0, PC1, PC2)
- 1 Server (Sebagai DNS Server)

## 🛠️ Konfigurasi

### 1. Konfigurasi Router sebagai DHCP Server

int fa0/0

ip address 192.168.1.1 255.255.255.0

no shutdown

ip dhcp pool LAN

network 192.168.1.0 255.255.255.0

default-router 192.168.1.1

dns-server 192.168.1.10


### 2. Konfigurasi Server (Sebagai DNS)

IP Address: 192.168.1.10

Subnet Mask: 255.255.255.0

Gateway: 192.168.1.1


Aktifkan DNS Service

Tambahkan entry:

Domain Name: belajar.local

Address: 192.168.1.10


### 3. Konfigurasi PC (PC0 - PC2)

Set IP ke DHCP

Cek koneksi:

Pastikan mendapat IP otomatis

Lakukan ping ke belajar.local untuk uji DNS


✅ Output yang Diharapkan

Semua PC berhasil mendapatkan IP dari DHCP

PC dapat mengakses server menggunakan nama domain (DNS resolve sukses)
