---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityPricing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityPricing.md
ms.openlocfilehash: a1b07c5fb76d912ec117d42497f0d0b14bfb298c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137998"
---
# <span data-ttu-id="f9c64-101">Get-AzSecurityPricing</span><span class="sxs-lookup"><span data-stu-id="f9c64-101">Get-AzSecurityPricing</span></span>

## <span data-ttu-id="f9c64-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9c64-102">SYNOPSIS</span></span>
<span data-ttu-id="f9c64-103">取得作用域的 Azure 安全中心的定價層資料。</span><span class="sxs-lookup"><span data-stu-id="f9c64-103">Gets the pricing tier data for Azure Security Center for a scope.</span></span>

## <span data-ttu-id="f9c64-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9c64-104">SYNTAX</span></span>

### <span data-ttu-id="f9c64-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="f9c64-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityPricing [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9c64-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="f9c64-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityPricing -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9c64-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9c64-107">ResourceId</span></span>
```
Get-AzSecurityPricing -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9c64-108">說明</span><span class="sxs-lookup"><span data-stu-id="f9c64-108">DESCRIPTION</span></span>
<span data-ttu-id="f9c64-109">Azure 安全中心定價層會根據範圍決定，使用此 Cmdlet，您就可以取得已設定的定價層級。</span><span class="sxs-lookup"><span data-stu-id="f9c64-109">Azure Security Center pricing tier is decided per scope, with this cmdlet you can get the configured pricing tiers.</span></span>
<span data-ttu-id="f9c64-110">[訂閱] 定價層將所有資源群組納入其下。</span><span class="sxs-lookup"><span data-stu-id="f9c64-110">Subscription pricing tier include all the resource groups under it.</span></span>
<span data-ttu-id="f9c64-111">資源群組定價層將覆寫訂閱定價層級。</span><span class="sxs-lookup"><span data-stu-id="f9c64-111">Resource Group pricing tier will override the subscription pricing tier.</span></span>

## <span data-ttu-id="f9c64-112">示例</span><span class="sxs-lookup"><span data-stu-id="f9c64-112">EXAMPLES</span></span>

### <span data-ttu-id="f9c64-113">範例1</span><span class="sxs-lookup"><span data-stu-id="f9c64-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityPricing
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
Id--/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/VirtualMachines
--                                                                                                                             ----       -----------
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlServers
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/pricings/default                              default    Standard
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/AppServices
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/StorageAccounts
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/SqlServerVirtualMachin…
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KubernetesService
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/ContainerRegistry
/subscriptions/fbaa2b23-e9dd-4bed-93c1-9e2a44f64bc0/providers/Microsoft.Security/pricings/KeyVaults
```

<span data-ttu-id="f9c64-114">取得訂閱和其底下的資源群組的所有已設定的定價層級。</span><span class="sxs-lookup"><span data-stu-id="f9c64-114">Gets all the configured pricing tiers for the subscription and the resource groups under it.</span></span>

### <span data-ttu-id="f9c64-115">範例2</span><span class="sxs-lookup"><span data-stu-id="f9c64-115">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityPricing -ResourceGroupName "myService1"
Id                                                                                                                             Name       PricingTier
--                                                                                                                             ----       -----------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/pricings/myService1 myService1 Standard
```

<span data-ttu-id="f9c64-116">取得「myService1」資源群組的已設定定價層級。</span><span class="sxs-lookup"><span data-stu-id="f9c64-116">Gets the configured pricing tier for the "myService1" resource group.</span></span>

## <span data-ttu-id="f9c64-117">參數</span><span class="sxs-lookup"><span data-stu-id="f9c64-117">PARAMETERS</span></span>

### <span data-ttu-id="f9c64-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9c64-118">-DefaultProfile</span></span>
<span data-ttu-id="f9c64-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9c64-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9c64-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f9c64-120">-Name</span></span>
<span data-ttu-id="f9c64-121">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f9c64-121">Resource name.</span></span>

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

### <span data-ttu-id="f9c64-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9c64-122">-ResourceId</span></span>
<span data-ttu-id="f9c64-123">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="f9c64-123">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9c64-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9c64-124">CommonParameters</span></span>
<span data-ttu-id="f9c64-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9c64-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9c64-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f9c64-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9c64-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f9c64-127">INPUTS</span></span>

### <span data-ttu-id="f9c64-128">System.object</span><span class="sxs-lookup"><span data-stu-id="f9c64-128">System.String</span></span>

## <span data-ttu-id="f9c64-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f9c64-129">OUTPUTS</span></span>

### <span data-ttu-id="f9c64-130">PSSecurityPricing 中的 Pricings （Security..。</span><span class="sxs-lookup"><span data-stu-id="f9c64-130">Microsoft.Azure.Commands.Security.Models.Pricings.PSSecurityPricing</span></span>

## <span data-ttu-id="f9c64-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f9c64-131">NOTES</span></span>

## <span data-ttu-id="f9c64-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9c64-132">RELATED LINKS</span></span>
