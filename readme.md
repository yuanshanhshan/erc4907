# ERC-4907 开发教程

[ERC-4907](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-4907.md) 是 [ERC-721](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-721.md) 的一个扩展。它提出了一个可以授予其他地址拥有角色（"user"），以及 user  角色自动撤销的时间（"expires"）的标准。`user`角色代表 "使用 "NFT的权限，但不代表拥有转让或设置其他地址为 user 的能力。

这个教程教大家如何使用 ChainIDE, MetaMask, 和 Solidity 部署 ERC-4907 智能合约。

如果你有任何问题，请加入[ChainIDE Discord!](https://discord.gg/QpGq4hjWrh)


以下是部署 ERC-4907 智能合约的步骤：

1. 安装 MetaMask

2. 编写 ERC-4907

3. 编译，部署和验证

4. 在 test.double.one 上列出  

### 1. 配置钱包

#### 1.1. 安装钱包

当我们在区块链上部署一个智能合约或对已部署的智能合约进行交易时，
我们需要支付 GAS ，为此，我们需要有一个Web3钱包，可以是 MetaMask。
所以，首先，我们要安装 MetaMask 。请点击[这里](https://metamask.io/)来安装 MetaMask 。

#### 1.2. 将 Mumbai 测试网络添加到 MetaMask 中
点击右上角的 "连接钱包"，选择 "Injected Web3 Provider "按钮，然后在 MetaMask 上选择，连接到MetaMask钱包（Polygon Mainnet 是主网络，Mumbai 是测试网络--连接到 Mumbai）。

![image-20230114120433122](https://d3gvnlbntpm4ho.cloudfront.net/ERC721_Deployment_on_Mumbai_Polygon/image-20230114120433122.png)


#### 1.3. 获取测试代币
一旦 Mumbai 被添加到 MetaMask ，导航到 [Polygon Faucet](https://faucet.polygon.technology/)以接收测试代币。在水龙头页面，选择 MUmbai 作为网络，MATIC 作为代币，并粘贴你的 MetaMask 钱包地址。然后，点击提交，水龙头将在一分钟内向你发送一些测试 MATIC 。

<img src="https://d3gvnlbntpm4ho.cloudfront.net/ERC+721+Deployment+on++Mumbai/Polygon_PR_get_tokens.png" width="100%" height="100%" />



### 2. 编写 ERC-4907 智能合约

你的ERC-4907智能合约必须包含必要的函数。一个的ERC-4907智能合约必须有以下函数。

-   `setUser()`: 设置 NFT 的 user 和 expires

-   `userOf()`: 返回 NFT user 的地址

-   `userExpires()`: 返回 NFT 的 expires


ChainIDE团队已经准备了完整的ERC-4907例子，包括所有需要的函数，你可以使用该内置模板**ERC4907.sol**，并根据你的要求添加/删除功能。

### 3. 编译，部署和验证
对此，你可以参考 ERC-721 Showcase 。


### 4. 在 test.double.one 上列出
自动部署是 Double Protocol 上的一个强大工具，它使NFT项目或任何人都能在 Double Protocol 上即时部署 "NFT集合"，以实现对这些NFT的租赁服务。

点击[这里](https://docs.double.one/for-developers/integration-tutorials/nft-rental-auto-deployment)查看详情 

