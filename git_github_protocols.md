# 如何从git clone其后URL的地址判断是哪种协定？

Git 可以使用四種主要的協定來傳輸資料：本地傳輸，SSH 協定，Git 協定和 HTTP 協定。下面分別介紹一下哪些情形應該使用（或避免使用）這些協定。

值得注意的是，除了 HTTP 協定外，其他所有協定都要求在伺服器端安裝並運行 Git。

- 本地協定
  + 這常見於團隊每一個成員都對一個共用的檔案系統（例如 NFS）擁有訪問權，或者比較少見的多人共用同一台電腦的情況。
  + 取。克隆的時候只需要將遠端倉庫的路徑作為 URL 使用，比如下面這樣：
    * $ git clone /opt/git/project.git
    * $ git clone file:///opt/git/project.git

- SSH 协议
  + Git 使用的傳輸協議中最常見的可能就是 SSH 了。SSH 也是唯一一個同時支持讀寫操作的網路通訊協定。另外兩個網路通訊協定（HTTP 和 Git）通常都是唯讀的，所以雖然二者對大多數人都可用，但執行寫操作時還是需要 SSH。SSH 同時也是一個驗證授權的網路通訊協定
  + 通過 SSH 克隆一個 Git 倉庫，你可以像下面這樣給出 ssh:// 的 URL：
    * $ git clone ssh://user@server/project.git
  + 或者不指明某個協定 — 這時 Git 會預設使用 SSH ：
    * $ git clone user@server:project.git

- Git 協議
  + $ git clone git://github.com/username/reponame.git
  + $ git clone git@github.com:username/reponame.git
  
- https://协定
  + $ git clone https://github.com/username/reponame.git
  + $ git clone http://example.com/gitproject.git

参考
[4.1 伺服器上的 Git - 協議](https://git-scm.com/book/zh-tw/v1/%E4%BC%BA%E6%9C%8D%E5%99%A8%E4%B8%8A%E7%9A%84-Git-%E5%8D%94%E8%AD%B0)
[2.1 Git 基礎 - 取得Git儲存庫](https://git-scm.com/book/zh-tw/v1/Git-%E5%9F%BA%E7%A4%8E-%E5%8F%96%E5%BE%97Git%E5%84%B2%E5%AD%98%E5%BA%AB)
