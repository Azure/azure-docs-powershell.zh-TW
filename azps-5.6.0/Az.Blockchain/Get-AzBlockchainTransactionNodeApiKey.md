---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: dbde273c1694f4622904ac00b261e902036c6e03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906786"
---
# <span data-ttu-id="cba05-101">Get-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="cba05-101">Get-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="cba05-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cba05-102">SYNOPSIS</span></span>
<span data-ttu-id="cba05-103">列出交易節點的 API 鍵。</span><span class="sxs-lookup"><span data-stu-id="cba05-103">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="cba05-104">語法</span><span class="sxs-lookup"><span data-stu-id="cba05-104">SYNTAX</span></span>

```
Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="cba05-105">描述</span><span class="sxs-lookup"><span data-stu-id="cba05-105">DESCRIPTION</span></span>
<span data-ttu-id="cba05-106">列出交易節點的 API 鍵。</span><span class="sxs-lookup"><span data-stu-id="cba05-106">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="cba05-107">例子</span><span class="sxs-lookup"><span data-stu-id="cba05-107">EXAMPLES</span></span>

### <span data-ttu-id="cba05-108">範例 1：事務節點的清單 Api 金鑰</span><span class="sxs-lookup"><span data-stu-id="cba05-108">Example 1: List Api keys for a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001

KeyName Value
------- -----
key1    H4_GPhxbqYENxwas4Vc4l5U9
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="cba05-109">此命令會列出交易節點的 Api 金鑰。</span><span class="sxs-lookup"><span data-stu-id="cba05-109">This command lists Api keys for a transaction node.</span></span>

## <span data-ttu-id="cba05-110">參數</span><span class="sxs-lookup"><span data-stu-id="cba05-110">PARAMETERS</span></span>

### <span data-ttu-id="cba05-111">-有一個產品名稱</span><span class="sxs-lookup"><span data-stu-id="cba05-111">-BlockchainMemberName</span></span>
<span data-ttu-id="cba05-112">進位成員名稱。</span><span class="sxs-lookup"><span data-stu-id="cba05-112">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba05-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cba05-113">-DefaultProfile</span></span>
<span data-ttu-id="cba05-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cba05-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba05-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cba05-115">-ResourceGroupName</span></span>
<span data-ttu-id="cba05-116">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="cba05-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="cba05-117">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="cba05-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba05-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cba05-118">-SubscriptionId</span></span>
<span data-ttu-id="cba05-119">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="cba05-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="cba05-120">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="cba05-120">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba05-121">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="cba05-121">-TransactionNodeName</span></span>
<span data-ttu-id="cba05-122">交易節點名稱。</span><span class="sxs-lookup"><span data-stu-id="cba05-122">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba05-123">-確認</span><span class="sxs-lookup"><span data-stu-id="cba05-123">-Confirm</span></span>
<span data-ttu-id="cba05-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cba05-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba05-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cba05-125">-WhatIf</span></span>
<span data-ttu-id="cba05-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cba05-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cba05-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cba05-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cba05-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cba05-128">CommonParameters</span></span>
<span data-ttu-id="cba05-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cba05-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cba05-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cba05-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cba05-131">輸入</span><span class="sxs-lookup"><span data-stu-id="cba05-131">INPUTS</span></span>

## <span data-ttu-id="cba05-132">輸出</span><span class="sxs-lookup"><span data-stu-id="cba05-132">OUTPUTS</span></span>

### <span data-ttu-id="cba05-133">Microsoft.Azure.PowerShell.Cmdlets.Azure.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="cba05-133">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="cba05-134">筆記</span><span class="sxs-lookup"><span data-stu-id="cba05-134">NOTES</span></span>

<span data-ttu-id="cba05-135">別名</span><span class="sxs-lookup"><span data-stu-id="cba05-135">ALIASES</span></span>

## <span data-ttu-id="cba05-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="cba05-136">RELATED LINKS</span></span>

