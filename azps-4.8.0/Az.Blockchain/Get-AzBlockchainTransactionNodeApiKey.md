---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 401073a8d97affaec866486b19113373c001ae58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971494"
---
# <span data-ttu-id="fa4a1-101">Get-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="fa4a1-101">Get-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="fa4a1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fa4a1-102">SYNOPSIS</span></span>
<span data-ttu-id="fa4a1-103">列出交易節點的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="fa4a1-103">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="fa4a1-104">句法</span><span class="sxs-lookup"><span data-stu-id="fa4a1-104">SYNTAX</span></span>

```
Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="fa4a1-105">說明</span><span class="sxs-lookup"><span data-stu-id="fa4a1-105">DESCRIPTION</span></span>
<span data-ttu-id="fa4a1-106">列出交易節點的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="fa4a1-106">List the API keys for the transaction node.</span></span>

## <span data-ttu-id="fa4a1-107">示例</span><span class="sxs-lookup"><span data-stu-id="fa4a1-107">EXAMPLES</span></span>

### <span data-ttu-id="fa4a1-108">範例1：列出交易節點的 Api 金鑰</span><span class="sxs-lookup"><span data-stu-id="fa4a1-108">Example 1: List Api keys for a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001

KeyName Value
------- -----
key1    H4_GPhxbqYENxwas4Vc4l5U9
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="fa4a1-109">這個命令會列出事務節點的 Api 金鑰。</span><span class="sxs-lookup"><span data-stu-id="fa4a1-109">This command lists Api keys for a transaction node.</span></span>

## <span data-ttu-id="fa4a1-110">參數</span><span class="sxs-lookup"><span data-stu-id="fa4a1-110">PARAMETERS</span></span>

### <span data-ttu-id="fa4a1-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="fa4a1-111">-BlockchainMemberName</span></span>
<span data-ttu-id="fa4a1-112">Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="fa4a1-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="fa4a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa4a1-113">-DefaultProfile</span></span>
<span data-ttu-id="fa4a1-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fa4a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa4a1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa4a1-115">-ResourceGroupName</span></span>
<span data-ttu-id="fa4a1-116">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="fa4a1-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="fa4a1-117">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="fa4a1-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="fa4a1-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fa4a1-118">-SubscriptionId</span></span>
<span data-ttu-id="fa4a1-119">取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="fa4a1-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="fa4a1-120">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="fa4a1-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fa4a1-121">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="fa4a1-121">-TransactionNodeName</span></span>
<span data-ttu-id="fa4a1-122">交易節點名稱。</span><span class="sxs-lookup"><span data-stu-id="fa4a1-122">Transaction node name.</span></span>

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

### <span data-ttu-id="fa4a1-123">-確認</span><span class="sxs-lookup"><span data-stu-id="fa4a1-123">-Confirm</span></span>
<span data-ttu-id="fa4a1-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="fa4a1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa4a1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa4a1-125">-WhatIf</span></span>
<span data-ttu-id="fa4a1-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fa4a1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa4a1-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fa4a1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa4a1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa4a1-128">CommonParameters</span></span>
<span data-ttu-id="fa4a1-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fa4a1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa4a1-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="fa4a1-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa4a1-131">輸入</span><span class="sxs-lookup"><span data-stu-id="fa4a1-131">INPUTS</span></span>

## <span data-ttu-id="fa4a1-132">輸出</span><span class="sxs-lookup"><span data-stu-id="fa4a1-132">OUTPUTS</span></span>

### <span data-ttu-id="fa4a1-133">IApiKey （Blockchain）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="fa4a1-133">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="fa4a1-134">筆記</span><span class="sxs-lookup"><span data-stu-id="fa4a1-134">NOTES</span></span>

<span data-ttu-id="fa4a1-135">別名</span><span class="sxs-lookup"><span data-stu-id="fa4a1-135">ALIASES</span></span>

## <span data-ttu-id="fa4a1-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="fa4a1-136">RELATED LINKS</span></span>

