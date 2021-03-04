---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: 87b53048ede0a5b2484da18ccd0a2f6a531aa92b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916497"
---
# <span data-ttu-id="f3c92-101">Get-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="f3c92-101">Get-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="f3c92-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f3c92-102">SYNOPSIS</span></span>
<span data-ttu-id="f3c92-103">在延伸資源的範圍中，獲得自適性網路增強資源的清單。</span><span class="sxs-lookup"><span data-stu-id="f3c92-103">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="f3c92-104">語法</span><span class="sxs-lookup"><span data-stu-id="f3c92-104">SYNTAX</span></span>

### <span data-ttu-id="f3c92-105">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="f3c92-105">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```
## <span data-ttu-id="f3c92-106">描述</span><span class="sxs-lookup"><span data-stu-id="f3c92-106">DESCRIPTION</span></span>
<span data-ttu-id="f3c92-107">由 Azure 資訊安全中心自動計算自適性網路轉切，使用此 Cmdlet 取得延伸資源範圍中的自適性網路增強資源清單。</span><span class="sxs-lookup"><span data-stu-id="f3c92-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="f3c92-108">例子</span><span class="sxs-lookup"><span data-stu-id="f3c92-108">EXAMPLES</span></span>

### <span data-ttu-id="f3c92-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="f3c92-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```

<span data-ttu-id="f3c92-110">在延伸資源的範圍中，獲得自適性網路增強資源的清單。</span><span class="sxs-lookup"><span data-stu-id="f3c92-110">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

### <span data-ttu-id="f3c92-111">範例 2</span><span class="sxs-lookup"><span data-stu-id="f3c92-111">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```
<span data-ttu-id="f3c92-112">取得單一自適性網路增強資源</span><span class="sxs-lookup"><span data-stu-id="f3c92-112">Get  a single Adaptive Network Hardenings resource</span></span>

## <span data-ttu-id="f3c92-113">參數</span><span class="sxs-lookup"><span data-stu-id="f3c92-113">PARAMETERS</span></span>

### <span data-ttu-id="f3c92-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3c92-114">-DefaultProfile</span></span>
<span data-ttu-id="f3c92-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f3c92-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3c92-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3c92-116">-ResourceGroupName</span></span>
<span data-ttu-id="f3c92-117">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f3c92-117">Resource group name.</span></span>

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

### <span data-ttu-id="f3c92-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f3c92-118">-ResourceName</span></span>
<span data-ttu-id="f3c92-119">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f3c92-119">Resource name.</span></span>

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

### <span data-ttu-id="f3c92-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="f3c92-120">-ResourceNamespace</span></span>
<span data-ttu-id="f3c92-121">資源的命名空間。</span><span class="sxs-lookup"><span data-stu-id="f3c92-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="f3c92-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f3c92-122">-ResourceType</span></span>
<span data-ttu-id="f3c92-123">資源的類型。</span><span class="sxs-lookup"><span data-stu-id="f3c92-123">The type of the resource.</span></span>

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

### <span data-ttu-id="f3c92-124">-AdaptiveNetwork1eningResourceName</span><span class="sxs-lookup"><span data-stu-id="f3c92-124">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="f3c92-125">自適性網路增強資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f3c92-125">The name of the Adaptive Network Hardening resource.</span></span>

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

### <span data-ttu-id="f3c92-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3c92-126">-SubscriptionId</span></span>
<span data-ttu-id="f3c92-127">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f3c92-127">Azure subscription ID.</span></span>

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
### <span data-ttu-id="f3c92-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3c92-128">CommonParameters</span></span>
<span data-ttu-id="f3c92-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f3c92-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3c92-130">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f3c92-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3c92-131">輸入</span><span class="sxs-lookup"><span data-stu-id="f3c92-131">INPUTS</span></span>

### <span data-ttu-id="f3c92-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f3c92-132">System.String</span></span>

## <span data-ttu-id="f3c92-133">輸出</span><span class="sxs-lookup"><span data-stu-id="f3c92-133">OUTPUTS</span></span>

### <span data-ttu-id="f3c92-134">Microsoft.Azure.Commands.Security.models.AdaptiveNetworkWorkenings.PSSecurityAdaptiveNetwork。</a0></span><span class="sxs-lookup"><span data-stu-id="f3c92-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span></span>

## <span data-ttu-id="f3c92-135">筆記</span><span class="sxs-lookup"><span data-stu-id="f3c92-135">NOTES</span></span>

## <span data-ttu-id="f3c92-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="f3c92-136">RELATED LINKS</span></span>