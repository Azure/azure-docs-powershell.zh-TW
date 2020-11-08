---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: e9dfe0e7ed4612ca99a2decf3aa91b521a7e9664
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139443"
---
# <span data-ttu-id="9a2c3-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="9a2c3-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="9a2c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9a2c3-102">SYNOPSIS</span></span>
<span data-ttu-id="9a2c3-103">設定作用中的 Azure 安全中心層的定價。</span><span class="sxs-lookup"><span data-stu-id="9a2c3-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="9a2c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="9a2c3-104">SYNTAX</span></span>

### <span data-ttu-id="9a2c3-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="9a2c3-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a2c3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9a2c3-106">InputObject</span></span>
```
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a2c3-107">說明</span><span class="sxs-lookup"><span data-stu-id="9a2c3-107">DESCRIPTION</span></span>
<span data-ttu-id="9a2c3-108">設定作用中的 Azure 安全中心層的定價。</span><span class="sxs-lookup"><span data-stu-id="9a2c3-108">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="9a2c3-109">示例</span><span class="sxs-lookup"><span data-stu-id="9a2c3-109">EXAMPLES</span></span>

### <span data-ttu-id="9a2c3-110">範例1</span><span class="sxs-lookup"><span data-stu-id="9a2c3-110">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="9a2c3-111">將訂閱 Azure 安全中心定價層級設定為 "標準"</span><span class="sxs-lookup"><span data-stu-id="9a2c3-111">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>


## <span data-ttu-id="9a2c3-112">參數</span><span class="sxs-lookup"><span data-stu-id="9a2c3-112">PARAMETERS</span></span>

### <span data-ttu-id="9a2c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a2c3-113">-DefaultProfile</span></span>
<span data-ttu-id="9a2c3-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9a2c3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a2c3-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a2c3-115">-InputObject</span></span>
<span data-ttu-id="9a2c3-116">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="9a2c3-116">Input Object.</span></span>

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

### <span data-ttu-id="9a2c3-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="9a2c3-117">-Name</span></span>
<span data-ttu-id="9a2c3-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="9a2c3-118">Resource name.</span></span>

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

### <span data-ttu-id="9a2c3-119">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="9a2c3-119">-PricingTier</span></span>
<span data-ttu-id="9a2c3-120">定價層。</span><span class="sxs-lookup"><span data-stu-id="9a2c3-120">Pricing Tier.</span></span>

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

### <span data-ttu-id="9a2c3-121">-確認</span><span class="sxs-lookup"><span data-stu-id="9a2c3-121">-Confirm</span></span>
<span data-ttu-id="9a2c3-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9a2c3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a2c3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a2c3-123">-WhatIf</span></span>
<span data-ttu-id="9a2c3-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9a2c3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a2c3-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a2c3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a2c3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a2c3-126">CommonParameters</span></span>
<span data-ttu-id="9a2c3-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9a2c3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a2c3-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9a2c3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a2c3-129">輸入</span><span class="sxs-lookup"><span data-stu-id="9a2c3-129">INPUTS</span></span>

### <span data-ttu-id="9a2c3-130">PSSecurityPricing 中的 Pricings （Security..。</span><span class="sxs-lookup"><span data-stu-id="9a2c3-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="9a2c3-131">輸出</span><span class="sxs-lookup"><span data-stu-id="9a2c3-131">OUTPUTS</span></span>

### <span data-ttu-id="9a2c3-132">PSSecurityPricing 中的 Pricings （Security..。</span><span class="sxs-lookup"><span data-stu-id="9a2c3-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="9a2c3-133">筆記</span><span class="sxs-lookup"><span data-stu-id="9a2c3-133">NOTES</span></span>

## <span data-ttu-id="9a2c3-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a2c3-134">RELATED LINKS</span></span>
