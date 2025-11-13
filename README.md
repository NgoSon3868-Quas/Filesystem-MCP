# Cấu hình MCP Server Filesystem

Repository này chứa cấu hình MCP Server Filesystem để sử dụng trên nhiều máy tính.

## Cấu hình

File `mcp.json` chứa cấu hình để thêm vào `.cursor/mcp.json` hoặc `~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem",
        "C:\\Users\\son.ngongoc",
        "D:\\Tranning Cusor"
      ]
    }
  }
}
```

## Lưu ý quan trọng

⚠️ **Điều chỉnh đường dẫn**: Bạn cần thay đổi các đường dẫn trong `args` cho phù hợp với máy tính của bạn:
- Thay `C:\\Users\\son.ngongoc` bằng đường dẫn thư mục của bạn
- Thay `D:\\Tranning Cusor` bằng đường dẫn thư mục bạn muốn cho phép truy cập

## Sử dụng

1. Clone repository này:
   ```bash
   git clone https://github.com/NgoSon3868-Quas/Filesystem-MCP.git
   cd Filesystem-MCP
   ```

2. Chỉnh sửa file `mcp.json` và thay đổi các đường dẫn cho phù hợp

3. Copy nội dung từ `mcp.json` vào file cấu hình MCP của bạn:
   - Windows: `C:\Users\<username>\.cursor\mcp.json`
   - Mac/Linux: `~/.cursor/mcp.json`
   
   Hoặc merge vào file `mcpServers` hiện có của bạn.

4. Khởi động lại Cursor IDE

## Yêu cầu

- Node.js và npm đã được cài đặt
- Package `@modelcontextprotocol/server-filesystem` sẽ được tự động tải khi sử dụng

## Tính năng

MCP Server Filesystem cung cấp các công cụ để:
- Đọc và ghi files
- Quản lý thư mục
- Tìm kiếm files
- Xem thông tin files và thư mục

## Bảo mật

⚠️ Chỉ cấu hình các thư mục bạn muốn cho phép truy cập. Không nên cấu hình thư mục hệ thống quan trọng.

## Kiểm tra cấu hình

Sau khi thêm cấu hình và khởi động lại Cursor:
1. Vào Settings > Tools & MCP
2. Kiểm tra trong danh sách "Installed MCP Servers" có `filesystem` với trạng thái "Ready"
