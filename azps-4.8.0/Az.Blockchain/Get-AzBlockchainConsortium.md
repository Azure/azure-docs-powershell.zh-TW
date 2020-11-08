---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: d34e8257d6946476ff5b6a2356ba9b1b06d8a9f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969932"
---
# <span data-ttu-id="2b3fc-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="2b3fc-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="2b3fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b3fc-102">SYNOPSIS</span></span>
<span data-ttu-id="2b3fc-103">列出訂閱可用的 consortiums。</span><span class="sxs-lookup"><span data-stu-id="2b3fc-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="2b3fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b3fc-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2b3fc-105">說明</span><span class="sxs-lookup"><span data-stu-id="2b3fc-105">DESCRIPTION</span></span>
<span data-ttu-id="2b3fc-106">列出訂閱可用的 consortiums。</span><span class="sxs-lookup"><span data-stu-id="2b3fc-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="2b3fc-107">示例</span><span class="sxs-lookup"><span data-stu-id="2b3fc-107">EXAMPLES</span></span>

### <span data-ttu-id="2b3fc-108">範例1：取得 Blockchain consortiums。</span><span class="sxs-lookup"><span data-stu-id="2b3fc-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="2b3fc-109">這個命令會列出特定位置的訂閱下的 consortiums。</span><span class="sxs-lookup"><span data-stu-id="2b3fc-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="2b3fc-110">參數</span><span class="sxs-lookup"><span data-stu-id="2b3fc-110">PARAMETERS</span></span>

### <span data-ttu-id="2b3fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b3fc-111">-DefaultProfile</span></span>
<span data-ttu-id="2b3fc-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2b3fc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b3fc-113">-位置</span><span class="sxs-lookup"><span data-stu-id="2b3fc-113">-Location</span></span>
<span data-ttu-id="2b3fc-114">位置名稱。</span><span class="sxs-lookup"><span data-stu-id="2b3fc-114">Location Name.</span></span>

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

### <span data-ttu-id="2b3fc-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2b3fc-115">-SubscriptionId</span></span>
<span data-ttu-id="2b3fc-116">取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="2b3fc-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="2b3fc-117">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="2b3fc-117">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2b3fc-118">-確認</span><span class="sxs-lookup"><span data-stu-id="2b3fc-118">-Confirm</span></span>
<span data-ttu-id="2b3fc-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2b3fc-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b3fc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b3fc-120">-WhatIf</span></span>
<span data-ttu-id="2b3fc-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2b3fc-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b3fc-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2b3fc-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b3fc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b3fc-123">CommonParameters</span></span>
<span data-ttu-id="2b3fc-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b3fc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b3fc-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2b3fc-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b3fc-126">輸入</span><span class="sxs-lookup"><span data-stu-id="2b3fc-126">INPUTS</span></span>

## <span data-ttu-id="2b3fc-127">輸出</span><span class="sxs-lookup"><span data-stu-id="2b3fc-127">OUTPUTS</span></span>

### <span data-ttu-id="2b3fc-128">IConsortium （Blockchain）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="2b3fc-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="2b3fc-129">筆記</span><span class="sxs-lookup"><span data-stu-id="2b3fc-129">NOTES</span></span>

<span data-ttu-id="2b3fc-130">別名</span><span class="sxs-lookup"><span data-stu-id="2b3fc-130">ALIASES</span></span>

## <span data-ttu-id="2b3fc-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b3fc-131">RELATED LINKS</span></span>

