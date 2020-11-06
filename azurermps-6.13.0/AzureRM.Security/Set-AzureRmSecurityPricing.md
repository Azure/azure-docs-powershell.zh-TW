---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityPricing.md
ms.openlocfilehash: f5b23c9221fe8d344e9220590283ab7799a0a3fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448908"
---
# <span data-ttu-id="5ce26-101">Set-AzureRmSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="5ce26-101">Set-AzureRmSecurityPricing</span></span>

## <span data-ttu-id="5ce26-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ce26-102">SYNOPSIS</span></span>
<span data-ttu-id="5ce26-103">設定作用中的 Azure 安全中心層的定價。</span><span class="sxs-lookup"><span data-stu-id="5ce26-103">Sets the pricing of Azure Security Center tier for a scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ce26-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ce26-104">SYNTAX</span></span>

### <span data-ttu-id="5ce26-105">SubscriptionLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="5ce26-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityPricing -Name <String> -PricingTier <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ce26-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="5ce26-106">ResourceGroupLevelResource</span></span>
```
Set-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String> -PricingTier <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ce26-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="5ce26-107">InputObject</span></span>
```
Set-AzureRmSecurityPricing -InputObject <PSAddPricingInputObject> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ce26-108">說明</span><span class="sxs-lookup"><span data-stu-id="5ce26-108">DESCRIPTION</span></span>
<span data-ttu-id="5ce26-109">設定作用中的 Azure 安全中心層的定價。</span><span class="sxs-lookup"><span data-stu-id="5ce26-109">Sets the pricing of Azure Security Center tier for a scope.</span></span>

## <span data-ttu-id="5ce26-110">示例</span><span class="sxs-lookup"><span data-stu-id="5ce26-110">EXAMPLES</span></span>

### <span data-ttu-id="5ce26-111">範例1</span><span class="sxs-lookup"><span data-stu-id="5ce26-111">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityPricing -Name "default" -PricingTier "Standard"
Id                                                                                                 Name    PricingTier
--                                                                                                 ----    -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default default Standard
```

<span data-ttu-id="5ce26-112">將訂閱 Azure 安全中心定價層級設定為 "標準"</span><span class="sxs-lookup"><span data-stu-id="5ce26-112">Sets the subscription Azure Security Center pricing tier to "Standard"</span></span>

### <span data-ttu-id="5ce26-113">範例2</span><span class="sxs-lookup"><span data-stu-id="5ce26-113">Example 2</span></span>
```powershell
PS C:\> Set-AzureRmSecurityPricing -Name "myService1" -ResourceGroupName "myService1" -PricingTier "Standard"

Id                                                                                                                     
--                                                                                                                     
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/...
```

<span data-ttu-id="5ce26-114">將 "myService1" 資源群組 [Azure 安全性中心] 定價層級設定為 "標準"</span><span class="sxs-lookup"><span data-stu-id="5ce26-114">Sets the "myService1" resource group Azure Security Center pricing tier to "Standard"</span></span>

## <span data-ttu-id="5ce26-115">參數</span><span class="sxs-lookup"><span data-stu-id="5ce26-115">PARAMETERS</span></span>

### <span data-ttu-id="5ce26-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ce26-116">-DefaultProfile</span></span>
<span data-ttu-id="5ce26-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5ce26-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce26-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ce26-118">-InputObject</span></span>
<span data-ttu-id="5ce26-119">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="5ce26-119">Input Object.</span></span>

```yaml
Type: PSAddPricingInputObject
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ce26-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="5ce26-120">-Name</span></span>
<span data-ttu-id="5ce26-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="5ce26-121">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce26-122">-PricingTier</span><span class="sxs-lookup"><span data-stu-id="5ce26-122">-PricingTier</span></span>
<span data-ttu-id="5ce26-123">定價層。</span><span class="sxs-lookup"><span data-stu-id="5ce26-123">Pricing Tier.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce26-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ce26-124">-ResourceGroupName</span></span>
<span data-ttu-id="5ce26-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="5ce26-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce26-126">-確認</span><span class="sxs-lookup"><span data-stu-id="5ce26-126">-Confirm</span></span>
<span data-ttu-id="5ce26-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5ce26-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce26-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ce26-128">-WhatIf</span></span>
<span data-ttu-id="5ce26-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5ce26-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ce26-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ce26-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ce26-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ce26-131">CommonParameters</span></span>
<span data-ttu-id="5ce26-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ce26-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ce26-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ce26-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ce26-134">輸入</span><span class="sxs-lookup"><span data-stu-id="5ce26-134">INPUTS</span></span>

### <span data-ttu-id="5ce26-135">System.object</span><span class="sxs-lookup"><span data-stu-id="5ce26-135">System.String</span></span>
<span data-ttu-id="5ce26-136">PSAddPricingInputObject 中的 Pricings （）</span><span class="sxs-lookup"><span data-stu-id="5ce26-136">Microsoft.Azure.Commands.Security.Cmdlets.Pricings.PSAddPricingInputObject</span></span>

## <span data-ttu-id="5ce26-137">輸出</span><span class="sxs-lookup"><span data-stu-id="5ce26-137">OUTPUTS</span></span>

### <span data-ttu-id="5ce26-138">PSSecurityPricing 中的 Pricings （Security..。</span><span class="sxs-lookup"><span data-stu-id="5ce26-138">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="5ce26-139">筆記</span><span class="sxs-lookup"><span data-stu-id="5ce26-139">NOTES</span></span>

## <span data-ttu-id="5ce26-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ce26-140">RELATED LINKS</span></span>
