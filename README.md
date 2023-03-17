# Muon-Network

Joining the Testnet (ALICE)

Cấu hình: 
4 GB of RAM, dual-core CPU, 20GB of storage space

1/ Cài đặt cần thiết: 

    sudo apt update && apt upgrade -y
    
cài docker:

    sudo apt install docker-compose -y
    
2/ Tải bộ cài node:

    curl -o docker-compose.yml https://raw.githubusercontent.com/muon-protocol/muon-node-js/testnet/docker-compose-pull.yml
    
3/ Chạy node:

    docker-compose up -d
    
4/ Back up thông tin node:
    
    docker cp muon-node:/usr/src/muon-node-js/.env ./backup.env
    
Dùng SFTP từ Termius lấy file backup.env lưu về máy tính

5/ Kiểm tra PeerID & Address: thay thế server-ip bằng địa chỉ IP của bạn

    http://<server-ip>:8000/status
    
6/ Vào trang web: mint token $ALICE bằng $BNB testnet

    https://alice.muon.net/join/
    
Tiếp tục, thêm thông tin PeerID & address vừa nhận được ở bước 5. Add node là thành công!


# Restore lại thông tin node cũ:

1/ Chép file backup.env vào lại root.

2/ Dùng lệnh restore  file backup.env chép vào muon-node-js

    docker cp backup.env muon-node:/usr/src/muon-node-js/.env
    
    
3/ khởi động lại node:

    docker-compose restart
    
Chanel: https://t.me/RunnodeVietNamese
Youtube: https://www.youtube.com/@nodevalidatorvietnam
Twitter: https://twitter.com/Node    

