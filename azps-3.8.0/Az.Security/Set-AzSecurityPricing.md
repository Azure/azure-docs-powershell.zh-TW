---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: af51b5d864591f868db2ae588eed1d727fc53239
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959697"
---
# <span data-ttu-id="8943a-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="8943a-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="8943a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8943a-102">SYNOPSIS</span></span>
<span data-ttu-id="8943a-103">設定作用中的 Azure 安全中心層的定價。</span><span class="sxs-lookup"><span data-stu-id="8943a-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="8943a-104">句法</span><span class="sxs-lookup"><span data-stu-id="8943a-104">SYNTAX</span></span>

### <span data-ttu-id="8943a-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="8943a-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8943a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8943a-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8943a-107">說明</span><span class="sxs-lookup"><span data-stu-id="8943a-107">DESCRIPTION</span></span>
<span data-ttu-id="8943a-108">設定作用中的 Azure 安全中心層的定價。</span><span class="sxs-lookup"><span data-stu-id="8943a-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="8943a-109">示例</span><span class="sxs-lookup"><span data-stu-id="8943a-109">EXAMPLES</span></span>

### <span data-ttu-id="8943a-110">範例1</span><span class="sxs-lookup"><span data-stu-id="8943a-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "default" -PricingTier "Standard"
Id                                                                                                 Name    PricingTier
--                                                                                                 ----    -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default default Standard
```

<span data-ttu-id="8943a-111">將訂閱 Azure 安全中心定價層級設定為 "標準"</span><span class="sxs-lookup"><span data-stu-id="8943a-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>

### <span data-ttu-id="8943a-112">範例2</span><span class="sxs-lookup"><span data-stu-id="8943a-112">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "myService1" -ResourceGroupName "myService1" -PricingTier "Standard"

Id                                                                                                                     
--                                                                                                                     
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/...
```

<span data-ttu-id="8943a-113">將 "myService1" 資源群組 [Azure 安全性中心] 定價層級設定為 "標準"</span><span class="sxs-lookup"><span data-stu-id="8943a-113">Sets the "myService1" resource group Azure Security Center pricing tier to "Standard"</span></span>

## <span data-ttu-id="8943a-114">參數</span><span class="sxs-lookup"><span data-stu-id="8943a-114">PARAMETERS</span></span>

### <span data-ttu-id="8943a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8943a-115">-DefaultProfile</span></span>
<span data-ttu-id="8943a-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8943a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8943a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8943a-117">-InputObject</span></span>
<span data-ttu-id="8943a-118">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="8943a-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8943a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="8943a-119">-Name</span></span>
<span data-ttu-id="8943a-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="8943a-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8943a-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="8943a-121">-PricingTier</span></span>
<span data-ttu-id="8943a-122">定價層。</span><span class="sxs-lookup"><span data-stu-id="8943a-122">Pricing Tier.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8943a-123">-確認</span><span class="sxs-lookup"><span data-stu-id="8943a-123">-Confirm</span></span>
<span data-ttu-id="8943a-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8943a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8943a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8943a-125">-WhatIf</span></span>
<span data-ttu-id="8943a-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8943a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8943a-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8943a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8943a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8943a-128">CommonParameters</span></span>
<span data-ttu-id="8943a-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8943a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8943a-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8943a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8943a-131">輸入</span><span class="sxs-lookup"><span data-stu-id="8943a-131">INPUTS</span></span>

### <span data-ttu-id="8943a-132">PSSecurityPricing 中的 Pricings （Security..。</span><span class="sxs-lookup"><span data-stu-id="8943a-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="8943a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="8943a-133">OUTPUTS</span></span>

### <span data-ttu-id="8943a-134">PSSecurityPricing 中的 Pricings （Security..。</span><span class="sxs-lookup"><span data-stu-id="8943a-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="8943a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="8943a-135">NOTES</span></span>

## <span data-ttu-id="8943a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="8943a-136">RELATED LINKS</span></span>
