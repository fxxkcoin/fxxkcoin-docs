# fxxkcoin-docs

### 信任的节点
+ node.fxxkcoin.feiwuis.me

### API
POST
`
/api/newwallet
`
新建钱包

参数:  
| 参数名 | 长度 | 类型 | 备注 |
| :----: | :----: | :----: | :----: |
| address | 64 | long long | 地址 |


POST
`
/api/getaddressbalance
`
获取地址的余额

参数:  
| 参数名 | 长度 | 类型 | 备注 |
| :----: | :----: | :----: | :----: |
| address | 64 | long long | 地址 |


POST
`
/api/transfer
`
发送交易

参数:  
| 参数名 | 长度 | 类型 | 备注 |
| :----: | :----: | :----: | :----: |
| from | 64 | long long | 发送地址的 secret* |
| to | 64 | long long | 接收地址 |
| amount | 64 | double | 金额 |

发送地址 secret 的伪代码为
```
sha256(sha256(sha256(备份密钥) + intval(备份码)))
```


POST
`
/api/getaddresstranscations
`
获取地址交易记录

参数:  
| 参数名 | 长度 | 类型 | 备注 |
| :----: | :----: | :----: | :----: |
| address | 64 | long long | 地址 |
