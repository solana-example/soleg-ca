## 1.文章推荐
https://foresightnews.pro/article/detail/53748

## 2.钱包(开发环境)
- 钱包路径
```
 /Users/example/.config/solana/id.json  
```

- 钱包地址:
```shell
DKQEpKgGjNrLH7oF6qF6RQNdQi3nmvEbiAwEVEtAvKsd  
```

## 3.搭建SOL开发环境

1.设置钱包做主钱包，来部署智能合约等

```shell
solana config set -k <文件路径+id.json或自定义名字>
solana config set -k /Users/example/.config/solana/id.json
```

2.启动SOL测试网络
```shell
solana-test-validator
```

## 4.部署合约

```shell
solana program deploy target/deploy/steel.so --url http://localhost:8899

solana program deploy target/deploy/soleg_ca.so --url http://localhost:8899

5DBFd6y14vp7ZpAx3CCURMG9w6t23uvgXXxJf2sgWChK
```

## 5.备注

HDtTFeszRJH5SfYRscz2pKpw34rK5oJmKY9Q7gzpkU9M

创建token

```shell

(base) xukuideMacBook-Pro:soleg-ca xukui$ spl-token create-token
Creating token AdpXH7v92grh3d9ZoAbvcRm764MMVoGLB84bfrLVVac8 under program TokenkegQfeZyiNwAJbNbGKPFXCWuBvf9Ss623VQ5DA

Address:  AdpXH7v92grh3d9ZoAbvcRm764MMVoGLB84bfrLVVac8
Decimals:  9

Signature: pt1b6M1Rfaipody6cXbRyvd1C4KPaVHqcvjkvUvJfr8WN9GXTJu8Qk2mfEjKBuHGemRSKrWoez6maz13Tc2T1Vp

(base) xukuideMacBook-Pro:soleg-ca xukui$ 


```
创建token账户

```angular2html

(base) xukuideMacBook-Pro:soleg-ca xukui$ spl-token create-account AdpXH7v92grh3d9ZoAbvcRm764MMVoGLB84bfrLVVac8
Creating account 3VwWGUK3qDh9cadYx47Tdde7XYyk2Wu4ZeXex5CdCwhc

Signature: 3WNarAE4xr3K9qbuyR75VunyLr8Fxh6ry2aYQSycCBWWWMz9sGprD5UGiee3soKnjR4TXFXU6gUGHPET92B4psqW

(base) xukuideMacBook-Pro:soleg-ca xukui$

```

给自己的这个TokenAccount发送(mint)

```angular2html

(base) xukuideMacBook-Pro:soleg-ca xukui$ spl-token balance AdpXH7v92grh3d9ZoAbvcRm764MMVoGLB84bfrLVVac8
100

```

```angular2html
(base) xukuideMacBook-Pro:soleg-ca xukui$ spl-token transfer --fund-recipient  AdpXH7v92grh3d9ZoAbvcRm764MMVoGLB84bfrLVVac8 1 DKQEpKgGjNrLH7oF6qF6RQNdQi3nmvEbiAwEVEtAvKsd
Transfer 1 tokens
Sender: 3VwWGUK3qDh9cadYx47Tdde7XYyk2Wu4ZeXex5CdCwhc
Recipient: DKQEpKgGjNrLH7oF6qF6RQNdQi3nmvEbiAwEVEtAvKsd
Recipient associated token account: 3VwWGUK3qDh9cadYx47Tdde7XYyk2Wu4ZeXex5CdCwhc

Signature: 4eKSvdX2fTnBN4Hu5KpiKh6FA3fMDP2XuKGBgyTHUrxRyaNJDWP3ucmy76xa5itCQtYaMHfTDmtxWr5AK71BF9MC
```
