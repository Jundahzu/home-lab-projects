# Class Website

這個資料夾對應的是班上傳播技能展使用的網站服務。

- 目的：提供班級展覽資訊、作品介紹與相關公告，讓同學和親友可以在線上瀏覽。
- 技術堆疊：在 ESXi 虛擬機上跑 Linux，使用 Docker 佈署 WordPress 及其所需的資料庫服務。
- 佈署方式：透過 Docker Compose 啟動 WordPress，搭配 Nginx 反向代理，並使用 Cloudflare Tunnel 將服務安全地公開到外網。
- 儲存：網站內容與上傳檔案放在 NAS 的共用資料夾中，透過 NFS 掛載到虛擬機，方便備份與集中管理。
- 關聯：實際運行在自建的小型機房中，配合 FortiGate 防火牆與 SSL VPN，讓需要維護網站的同學也能從外部安全連回後台。
