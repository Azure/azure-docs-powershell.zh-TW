---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberApiKey.md
ms.openlocfilehash: b94a7158830530be9df31531101c9c9c5be90df1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912110"
---
# <span data-ttu-id="47775-101">Get-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="47775-101">Get-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="47775-102">簡介</span><span class="sxs-lookup"><span data-stu-id="47775-102">SYNOPSIS</span></span>
<span data-ttu-id="47775-103">列出適用于介面介面的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="47775-103">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="47775-104">語法</span><span class="sxs-lookup"><span data-stu-id="47775-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="47775-105">描述</span><span class="sxs-lookup"><span data-stu-id="47775-105">DESCRIPTION</span></span>
<span data-ttu-id="47775-106">列出適用于介面介面的 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="47775-106">Lists the API keys for a blockchain member.</span></span>

## <span data-ttu-id="47775-107">例子</span><span class="sxs-lookup"><span data-stu-id="47775-107">EXAMPLES</span></span>

### <span data-ttu-id="47775-108">範例 1：清單 api 鍵</span><span class="sxs-lookup"><span data-stu-id="47775-108">Example 1: List blockchain Api keys</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

KeyName Value
------- -----
key1    72_8u5HPZJxtZmtvm4Y4W9o-
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="47775-109">此命令會列出適用于介面介面成員之 Api 鍵。</span><span class="sxs-lookup"><span data-stu-id="47775-109">This command lists Api keys for a blockchain member.</span></span>

## <span data-ttu-id="47775-110">參數</span><span class="sxs-lookup"><span data-stu-id="47775-110">PARAMETERS</span></span>

### <span data-ttu-id="47775-111">-有一個產品名稱</span><span class="sxs-lookup"><span data-stu-id="47775-111">-BlockchainMemberName</span></span>
<span data-ttu-id="47775-112">進位成員名稱。</span><span class="sxs-lookup"><span data-stu-id="47775-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="47775-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47775-113">-DefaultProfile</span></span>
<span data-ttu-id="47775-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="47775-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47775-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47775-115">-ResourceGroupName</span></span>
<span data-ttu-id="47775-116">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="47775-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="47775-117">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="47775-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="47775-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47775-118">-SubscriptionId</span></span>
<span data-ttu-id="47775-119">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="47775-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="47775-120">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="47775-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="47775-121">-確認</span><span class="sxs-lookup"><span data-stu-id="47775-121">-Confirm</span></span>
<span data-ttu-id="47775-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="47775-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47775-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47775-123">-WhatIf</span></span>
<span data-ttu-id="47775-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="47775-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47775-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47775-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47775-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47775-126">CommonParameters</span></span>
<span data-ttu-id="47775-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="47775-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47775-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="47775-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47775-129">輸入</span><span class="sxs-lookup"><span data-stu-id="47775-129">INPUTS</span></span>

## <span data-ttu-id="47775-130">輸出</span><span class="sxs-lookup"><span data-stu-id="47775-130">OUTPUTS</span></span>

### <span data-ttu-id="47775-131">Microsoft.Azure.PowerShell.Cmdlets.Azure.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="47775-131">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="47775-132">筆記</span><span class="sxs-lookup"><span data-stu-id="47775-132">NOTES</span></span>

<span data-ttu-id="47775-133">別名</span><span class="sxs-lookup"><span data-stu-id="47775-133">ALIASES</span></span>

## <span data-ttu-id="47775-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="47775-134">RELATED LINKS</span></span>

