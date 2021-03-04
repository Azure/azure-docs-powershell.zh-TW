---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityPricing.md
ms.openlocfilehash: f55c42178daacdbf2be80982fb151514372d2d3d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910622"
---
# <span data-ttu-id="efb29-101">Set-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="efb29-101">Set-AzSecurityPricing</span></span>

## <span data-ttu-id="efb29-102">簡介</span><span class="sxs-lookup"><span data-stu-id="efb29-102">SYNOPSIS</span></span>

<span data-ttu-id="efb29-103">啟用或停用 Azure 資訊安全中心訂閱的 Azure Defender 方案。</span><span class="sxs-lookup"><span data-stu-id="efb29-103">Enables or disables Azure Defender plans for a subscription in Azure Security Center.</span></span>

## <span data-ttu-id="efb29-104">語法</span><span class="sxs-lookup"><span data-stu-id="efb29-104">SYNTAX</span></span>

### <span data-ttu-id="efb29-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="efb29-105">SubscriptionLevelResource (Default)</span></span>

```powershell
Set-AzSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="efb29-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="efb29-106">InputObject</span></span>

```powershell
Set-AzSecurityPricing -InputObject <PSSecurityPricing> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efb29-107">描述</span><span class="sxs-lookup"><span data-stu-id="efb29-107">DESCRIPTION</span></span>

<span data-ttu-id="efb29-108">啟用或停用訂閱的任何 Azure Defender 方案。</span><span class="sxs-lookup"><span data-stu-id="efb29-108">Enable or disable any of the Azure Defender plans for a subscription.</span></span>

<span data-ttu-id="efb29-109">有關 Azure Defender 和可用方案的詳細資訊，請參閱 [Azure Defender 簡介](https://docs.microsoft.com/azure/security-center/azure-defender)。</span><span class="sxs-lookup"><span data-stu-id="efb29-109">For details about Azure Defender and the available plans, see [Introduction to Azure Defender](https://docs.microsoft.com/azure/security-center/azure-defender).</span></span>

## <span data-ttu-id="efb29-110">例子</span><span class="sxs-lookup"><span data-stu-id="efb29-110">EXAMPLES</span></span>

### <span data-ttu-id="efb29-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="efb29-111">Example 1</span></span>

```powershell
PS C:\> Set-AzSecurityPricing -Name "virtualmachines" -PricingTier "Standard"
```

<span data-ttu-id="efb29-112">啟用 **適用于訂閱之伺服器的 Azure Defender。**</span><span class="sxs-lookup"><span data-stu-id="efb29-112">Enables **Azure Defender for servers** for the subscription.</span></span>

<span data-ttu-id="efb29-113">「標準」是指 Azure Defender 計畫的「On」狀態，如 Azure 資訊安全中心的 Azure 入口網站定價和設定區域所示。</span><span class="sxs-lookup"><span data-stu-id="efb29-113">"Standard" refers to the "On" state for an Azure Defender plan as shown in Azure Security Center's pricing and settings area of the Azure portal.</span></span>


## <span data-ttu-id="efb29-114">參數</span><span class="sxs-lookup"><span data-stu-id="efb29-114">PARAMETERS</span></span>

### <span data-ttu-id="efb29-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efb29-115">-DefaultProfile</span></span>

<span data-ttu-id="efb29-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="efb29-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efb29-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efb29-117">-InputObject</span></span>

<span data-ttu-id="efb29-118">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="efb29-118">Input Object.</span></span>

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

### <span data-ttu-id="efb29-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="efb29-119">-Name</span></span>

<span data-ttu-id="efb29-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="efb29-120">Resource name.</span></span>

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

### <span data-ttu-id="efb29-121">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="efb29-121">-PricingTier</span></span>

<span data-ttu-id="efb29-122">定價層級。</span><span class="sxs-lookup"><span data-stu-id="efb29-122">Pricing Tier.</span></span>

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

### <span data-ttu-id="efb29-123">-確認</span><span class="sxs-lookup"><span data-stu-id="efb29-123">-Confirm</span></span>

<span data-ttu-id="efb29-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="efb29-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efb29-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efb29-125">-WhatIf</span></span>

<span data-ttu-id="efb29-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="efb29-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efb29-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="efb29-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efb29-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efb29-128">CommonParameters</span></span>

<span data-ttu-id="efb29-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="efb29-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efb29-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efb29-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efb29-131">輸入</span><span class="sxs-lookup"><span data-stu-id="efb29-131">INPUTS</span></span>

### <span data-ttu-id="efb29-132">Microsoft.Azure.Commands.Security.models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="efb29-132">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="efb29-133">輸出</span><span class="sxs-lookup"><span data-stu-id="efb29-133">OUTPUTS</span></span>

### <span data-ttu-id="efb29-134">Microsoft.Azure.Commands.Security.models.Pricings.PSSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="efb29-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="efb29-135">筆記</span><span class="sxs-lookup"><span data-stu-id="efb29-135">NOTES</span></span>

## <span data-ttu-id="efb29-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="efb29-136">RELATED LINKS</span></span>
