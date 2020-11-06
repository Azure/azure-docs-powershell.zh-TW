---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityPricing.md
ms.openlocfilehash: 27d27cf3df8c41eaa507d9223c73f2b36637a04c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445460"
---
# <span data-ttu-id="c7f45-101">Get-AzureRmSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="c7f45-101">Get-AzureRmSecurityPricing</span></span>

## <span data-ttu-id="c7f45-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7f45-102">SYNOPSIS</span></span>
<span data-ttu-id="c7f45-103">取得作用域的 Azure 安全中心的定價層資料。</span><span class="sxs-lookup"><span data-stu-id="c7f45-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7f45-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7f45-104">SYNTAX</span></span>

### <span data-ttu-id="c7f45-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="c7f45-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7f45-106">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="c7f45-106">ResourceGroupLevelResource</span></span>
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7f45-107">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="c7f45-107">ResourceGroupScope</span></span>
```
Get-AzureRmSecurityPricing -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c7f45-108">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="c7f45-108">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7f45-109">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7f45-109">ResourceId</span></span>
```
Get-AzureRmSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7f45-110">說明</span><span class="sxs-lookup"><span data-stu-id="c7f45-110">DESCRIPTION</span></span>
<span data-ttu-id="c7f45-111">Azure 安全中心定價層會根據範圍決定，使用此 Cmdlet，您就可以取得已設定的定價層級。</span><span class="sxs-lookup"><span data-stu-id="c7f45-111">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="c7f45-112">[訂閱] 定價層將所有資源群組納入其下。</span><span class="sxs-lookup"><span data-stu-id="c7f45-112">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="c7f45-113">資源群組定價層將覆寫訂閱定價層級。</span><span class="sxs-lookup"><span data-stu-id="c7f45-113">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="c7f45-114">示例</span><span class="sxs-lookup"><span data-stu-id="c7f45-114">EXAMPLES</span></span>

### <span data-ttu-id="c7f45-115">範例1</span><span class="sxs-lookup"><span data-stu-id="c7f45-115">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="c7f45-116">取得訂閱和其底下的資源群組的所有已設定的定價層級。</span><span class="sxs-lookup"><span data-stu-id="c7f45-116">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="c7f45-117">範例2</span><span class="sxs-lookup"><span data-stu-id="c7f45-117">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="c7f45-118">取得「myService1」資源 gorup 的已設定定價層級。</span><span class="sxs-lookup"><span data-stu-id="c7f45-118">Gets the configured pricing tier for the "myService1" resource gorup.</span></span>

## <span data-ttu-id="c7f45-119">參數</span><span class="sxs-lookup"><span data-stu-id="c7f45-119">PARAMETERS</span></span>

### <span data-ttu-id="c7f45-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7f45-120">-DefaultProfile</span></span>
<span data-ttu-id="c7f45-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c7f45-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7f45-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="c7f45-122">-Name</span></span>
<span data-ttu-id="c7f45-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="c7f45-123">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7f45-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7f45-124">-ResourceGroupName</span></span>
<span data-ttu-id="c7f45-125">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c7f45-125">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource, ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7f45-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7f45-126">-ResourceId</span></span>
<span data-ttu-id="c7f45-127">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="c7f45-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7f45-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7f45-128">CommonParameters</span></span>
<span data-ttu-id="c7f45-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7f45-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7f45-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c7f45-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7f45-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c7f45-131">INPUTS</span></span>

### <span data-ttu-id="c7f45-132">System.object</span><span class="sxs-lookup"><span data-stu-id="c7f45-132">System.String</span></span>

## <span data-ttu-id="c7f45-133">輸出</span><span class="sxs-lookup"><span data-stu-id="c7f45-133">OUTPUTS</span></span>

### <span data-ttu-id="c7f45-134">PSSecurityPricing 中的 Pricings （Security..。</span><span class="sxs-lookup"><span data-stu-id="c7f45-134">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="c7f45-135">筆記</span><span class="sxs-lookup"><span data-stu-id="c7f45-135">NOTES</span></span>

## <span data-ttu-id="c7f45-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7f45-136">RELATED LINKS</span></span>
