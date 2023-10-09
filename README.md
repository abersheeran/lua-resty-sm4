在 openresty 上使用国密算法 SM4

## 快速使用

实际使用过程中请注意是否将对应文件放在resty目录下，若不是 请修改 `require` 为对应导入的包路径

```lua
local resty_sm4 = require "resty.sm4"
local key = '1234567890abcdef'  -- 十六进制字符的 Key
local text = 'test'
local sm4 = resty_sm4:new(key)
# 加密
local en_text = sm4:encrypt(text)
print(en_text)
#解密
local de_text = sm4:decrypt(text)
print(en_text)
```
