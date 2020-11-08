---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: cd28e66466239bf7fb0478774c1914180d2ede42
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126239"
---
# <span data-ttu-id="0d1ab-101">Get-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="0d1ab-101">Get-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="0d1ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d1ab-102">SYNOPSIS</span></span>
<span data-ttu-id="0d1ab-103">在延伸資源範圍內取得彈性網路 Hardenings 資源的清單。</span><span class="sxs-lookup"><span data-stu-id="0d1ab-103">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="0d1ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d1ab-104">SYNTAX</span></span>

### <span data-ttu-id="0d1ab-105">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="0d1ab-105">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```
## <span data-ttu-id="0d1ab-106">說明</span><span class="sxs-lookup"><span data-stu-id="0d1ab-106">DESCRIPTION</span></span>
<span data-ttu-id="0d1ab-107">[自我調整網路 Hardenings] 是由 Azure 安全中心自動計算，使用此 Cmdlet 來取得延伸資源範圍內的彈性網路 Hardenings 資源清單。</span><span class="sxs-lookup"><span data-stu-id="0d1ab-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="0d1ab-108">示例</span><span class="sxs-lookup"><span data-stu-id="0d1ab-108">EXAMPLES</span></span>

### <span data-ttu-id="0d1ab-109">範例1</span><span class="sxs-lookup"><span data-stu-id="0d1ab-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```

<span data-ttu-id="0d1ab-110">在延伸資源範圍內取得彈性網路 Hardenings 資源的清單。</span><span class="sxs-lookup"><span data-stu-id="0d1ab-110">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

### <span data-ttu-id="0d1ab-111">範例2</span><span class="sxs-lookup"><span data-stu-id="0d1ab-111">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```
<span data-ttu-id="0d1ab-112">取得單一彈性網路 Hardenings 資源</span><span class="sxs-lookup"><span data-stu-id="0d1ab-112">Get  a single Adaptive Network Hardenings resource</span></span>

## <span data-ttu-id="0d1ab-113">參數</span><span class="sxs-lookup"><span data-stu-id="0d1ab-113">PARAMETERS</span></span>

### <span data-ttu-id="0d1ab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d1ab-114">-DefaultProfile</span></span>
<span data-ttu-id="0d1ab-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d1ab-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d1ab-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d1ab-116">-ResourceGroupName</span></span>
<span data-ttu-id="0d1ab-117">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="0d1ab-117">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1ab-118">-CoNtext.resourcename</span><span class="sxs-lookup"><span data-stu-id="0d1ab-118">-ResourceName</span></span>
<span data-ttu-id="0d1ab-119">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="0d1ab-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1ab-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="0d1ab-120">-ResourceNamespace</span></span>
<span data-ttu-id="0d1ab-121">資源的命名空間。</span><span class="sxs-lookup"><span data-stu-id="0d1ab-121">The Namespace of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNamespace
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1ab-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0d1ab-122">-ResourceType</span></span>
<span data-ttu-id="0d1ab-123">資源的類型。</span><span class="sxs-lookup"><span data-stu-id="0d1ab-123">The type of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1ab-124">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="0d1ab-124">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="0d1ab-125">適應網路加強資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d1ab-125">The name of the Adaptive Network Hardening resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d1ab-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d1ab-126">-SubscriptionId</span></span>
<span data-ttu-id="0d1ab-127">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="0d1ab-127">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="0d1ab-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d1ab-128">CommonParameters</span></span>
<span data-ttu-id="0d1ab-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d1ab-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d1ab-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0d1ab-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d1ab-131">輸入</span><span class="sxs-lookup"><span data-stu-id="0d1ab-131">INPUTS</span></span>

### <span data-ttu-id="0d1ab-132">System.object</span><span class="sxs-lookup"><span data-stu-id="0d1ab-132">System.String</span></span>

## <span data-ttu-id="0d1ab-133">輸出</span><span class="sxs-lookup"><span data-stu-id="0d1ab-133">OUTPUTS</span></span>

### <span data-ttu-id="0d1ab-134">PSSecurityAdaptiveNetworkHardenings 中的 AdaptiveNetworkHardenings （Security..。</span><span class="sxs-lookup"><span data-stu-id="0d1ab-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span></span>

## <span data-ttu-id="0d1ab-135">筆記</span><span class="sxs-lookup"><span data-stu-id="0d1ab-135">NOTES</span></span>

## <span data-ttu-id="0d1ab-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d1ab-136">RELATED LINKS</span></span>