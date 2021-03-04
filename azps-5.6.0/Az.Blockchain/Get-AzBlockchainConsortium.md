---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchainconsortium
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainConsortium.md
ms.openlocfilehash: 077b1f18e18fbf47d8c89d02c44722c0a1561dac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902645"
---
# <span data-ttu-id="4e919-101">Get-AzBlockchainConsortium</span><span class="sxs-lookup"><span data-stu-id="4e919-101">Get-AzBlockchainConsortium</span></span>

## <span data-ttu-id="4e919-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4e919-102">SYNOPSIS</span></span>
<span data-ttu-id="4e919-103">列出訂閱可用的聯合企業。</span><span class="sxs-lookup"><span data-stu-id="4e919-103">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="4e919-104">語法</span><span class="sxs-lookup"><span data-stu-id="4e919-104">SYNTAX</span></span>

```
Get-AzBlockchainConsortium -Location <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4e919-105">描述</span><span class="sxs-lookup"><span data-stu-id="4e919-105">DESCRIPTION</span></span>
<span data-ttu-id="4e919-106">列出訂閱可用的聯合企業。</span><span class="sxs-lookup"><span data-stu-id="4e919-106">Lists the available consortiums for a subscription.</span></span>

## <span data-ttu-id="4e919-107">例子</span><span class="sxs-lookup"><span data-stu-id="4e919-107">EXAMPLES</span></span>

### <span data-ttu-id="4e919-108">範例 1：取得進一步開發公司。</span><span class="sxs-lookup"><span data-stu-id="4e919-108">Example 1: Get Blockchain consortiums.</span></span>
```powershell
PS C:\> Get-AzBlockchainConsortium -Location eastus

```

<span data-ttu-id="4e919-109">此命令會列出特定位置訂閱下的聯合企業。</span><span class="sxs-lookup"><span data-stu-id="4e919-109">This command lists the consortiums under a subscription for a specific location.</span></span>

## <span data-ttu-id="4e919-110">參數</span><span class="sxs-lookup"><span data-stu-id="4e919-110">PARAMETERS</span></span>

### <span data-ttu-id="4e919-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e919-111">-DefaultProfile</span></span>
<span data-ttu-id="4e919-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e919-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e919-113">-位置</span><span class="sxs-lookup"><span data-stu-id="4e919-113">-Location</span></span>
<span data-ttu-id="4e919-114">位置名稱。</span><span class="sxs-lookup"><span data-stu-id="4e919-114">Location Name.</span></span>

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

### <span data-ttu-id="4e919-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e919-115">-SubscriptionId</span></span>
<span data-ttu-id="4e919-116">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="4e919-116">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4e919-117">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="4e919-117">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4e919-118">-確認</span><span class="sxs-lookup"><span data-stu-id="4e919-118">-Confirm</span></span>
<span data-ttu-id="4e919-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4e919-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e919-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e919-120">-WhatIf</span></span>
<span data-ttu-id="4e919-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4e919-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e919-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e919-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e919-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e919-123">CommonParameters</span></span>
<span data-ttu-id="4e919-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4e919-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e919-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e919-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e919-126">輸入</span><span class="sxs-lookup"><span data-stu-id="4e919-126">INPUTS</span></span>

## <span data-ttu-id="4e919-127">輸出</span><span class="sxs-lookup"><span data-stu-id="4e919-127">OUTPUTS</span></span>

### <span data-ttu-id="4e919-128">Microsoft.Azure.PowerShell.Cmdlets.Azure.Models.Api20180601Preview.IConsortium</span><span class="sxs-lookup"><span data-stu-id="4e919-128">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortium</span></span>

## <span data-ttu-id="4e919-129">筆記</span><span class="sxs-lookup"><span data-stu-id="4e919-129">NOTES</span></span>

<span data-ttu-id="4e919-130">別名</span><span class="sxs-lookup"><span data-stu-id="4e919-130">ALIASES</span></span>

## <span data-ttu-id="4e919-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e919-131">RELATED LINKS</span></span>

