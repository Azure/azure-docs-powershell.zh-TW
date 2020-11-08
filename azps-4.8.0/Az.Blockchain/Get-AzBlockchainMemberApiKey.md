---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 646d07646ff7530dc805d4c516a1cf981aafe915
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969347"
---
# <span data-ttu-id="d9bc4-101">Get-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="d9bc4-101">Get-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="d9bc4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d9bc4-102">SYNOPSIS</span></span>
<span data-ttu-id="d9bc4-103">列出 blockchain 成員的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="d9bc4-103">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="d9bc4-104">句法</span><span class="sxs-lookup"><span data-stu-id="d9bc4-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d9bc4-105">說明</span><span class="sxs-lookup"><span data-stu-id="d9bc4-105">DESCRIPTION</span></span>
<span data-ttu-id="d9bc4-106">列出 blockchain 成員的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="d9bc4-106">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="d9bc4-107">示例</span><span class="sxs-lookup"><span data-stu-id="d9bc4-107">EXAMPLES</span></span>

### <span data-ttu-id="d9bc4-108">範例1：清單 blockchain Api 金鑰</span><span class="sxs-lookup"><span data-stu-id="d9bc4-108">Example 1: List blockchain Api keys</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

KeyName Value
------- -----
key1    72_8u5HPZJxtZmtvm4Y4W9o-
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="d9bc4-109">這個命令會列出 blockchain 成員的 Api 金鑰。</span><span class="sxs-lookup"><span data-stu-id="d9bc4-109">This command lists Api keys for a blockchain member.</span></span>

## <span data-ttu-id="d9bc4-110">參數</span><span class="sxs-lookup"><span data-stu-id="d9bc4-110">PARAMETERS</span></span>

### <span data-ttu-id="d9bc4-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="d9bc4-111">-BlockchainMemberName</span></span>
<span data-ttu-id="d9bc4-112">Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="d9bc4-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="d9bc4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9bc4-113">-DefaultProfile</span></span>
<span data-ttu-id="d9bc4-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9bc4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9bc4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9bc4-115">-ResourceGroupName</span></span>
<span data-ttu-id="d9bc4-116">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d9bc4-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d9bc4-117">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="d9bc4-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d9bc4-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d9bc4-118">-SubscriptionId</span></span>
<span data-ttu-id="d9bc4-119">取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="d9bc4-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d9bc4-120">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="d9bc4-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d9bc4-121">-確認</span><span class="sxs-lookup"><span data-stu-id="d9bc4-121">-Confirm</span></span>
<span data-ttu-id="d9bc4-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d9bc4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9bc4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9bc4-123">-WhatIf</span></span>
<span data-ttu-id="d9bc4-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d9bc4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9bc4-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d9bc4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9bc4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9bc4-126">CommonParameters</span></span>
<span data-ttu-id="d9bc4-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d9bc4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9bc4-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d9bc4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9bc4-129">輸入</span><span class="sxs-lookup"><span data-stu-id="d9bc4-129">INPUTS</span></span>

## <span data-ttu-id="d9bc4-130">輸出</span><span class="sxs-lookup"><span data-stu-id="d9bc4-130">OUTPUTS</span></span>

### <span data-ttu-id="d9bc4-131">IApiKey （Blockchain）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="d9bc4-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="d9bc4-132">筆記</span><span class="sxs-lookup"><span data-stu-id="d9bc4-132">NOTES</span></span>

<span data-ttu-id="d9bc4-133">別名</span><span class="sxs-lookup"><span data-stu-id="d9bc4-133">ALIASES</span></span>

## <span data-ttu-id="d9bc4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9bc4-134">RELATED LINKS</span></span>
