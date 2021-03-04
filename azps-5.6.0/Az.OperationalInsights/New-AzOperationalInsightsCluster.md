---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
ms.openlocfilehash: c34bb862d3928e6dbbaa55a9660c4868e38941b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916900"
---
# <span data-ttu-id="f573a-101">New-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="f573a-101">New-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="f573a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f573a-102">SYNOPSIS</span></span>
<span data-ttu-id="f573a-103">建立集區</span><span class="sxs-lookup"><span data-stu-id="f573a-103">Create cluster</span></span>

## <span data-ttu-id="f573a-104">語法</span><span class="sxs-lookup"><span data-stu-id="f573a-104">SYNTAX</span></span>

```
New-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-Location] <String>
 [-IdentityType <String>] [-SkuName <String>] -SkuCapacity <Int64> [-Tags <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f573a-105">描述</span><span class="sxs-lookup"><span data-stu-id="f573a-105">DESCRIPTION</span></span>

<span data-ttu-id="f573a-106">建立集區</span><span class="sxs-lookup"><span data-stu-id="f573a-106">Create cluster</span></span>

## <span data-ttu-id="f573a-107">例子</span><span class="sxs-lookup"><span data-stu-id="f573a-107">EXAMPLES</span></span>

### <span data-ttu-id="f573a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="f573a-108">Example 1</span></span>
```powershell
New-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name} -Location eastus -IdentityType SystemAssigned -SkuName CapacityReservation -SkuCapacity 1000

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : ProvisioningAccount
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="f573a-109">建立集區</span><span class="sxs-lookup"><span data-stu-id="f573a-109">Create cluster</span></span>

## <span data-ttu-id="f573a-110">參數</span><span class="sxs-lookup"><span data-stu-id="f573a-110">PARAMETERS</span></span>

### <span data-ttu-id="f573a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f573a-111">-AsJob</span></span>
<span data-ttu-id="f573a-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f573a-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f573a-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f573a-113">-ClusterName</span></span>
<span data-ttu-id="f573a-114">組名。</span><span class="sxs-lookup"><span data-stu-id="f573a-114">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f573a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f573a-115">-DefaultProfile</span></span>
<span data-ttu-id="f573a-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f573a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f573a-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="f573a-117">-IdentityType</span></span>
<span data-ttu-id="f573a-118">身分識別類型，值可以是 'SystemAssigned'， 'None'。</span><span class="sxs-lookup"><span data-stu-id="f573a-118">the identity type, value can be 'SystemAssigned', 'None'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f573a-119">-位置</span><span class="sxs-lookup"><span data-stu-id="f573a-119">-Location</span></span>
<span data-ttu-id="f573a-120">將部署該組集的地理區域。</span><span class="sxs-lookup"><span data-stu-id="f573a-120">The geographic region that the cluster will be deployed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f573a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f573a-121">-ResourceGroupName</span></span>
<span data-ttu-id="f573a-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f573a-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f573a-123">-Sku以</span><span class="sxs-lookup"><span data-stu-id="f573a-123">-SkuCapacity</span></span>
<span data-ttu-id="f573a-124">SKU 容量，值必須為 100 的倍數，且範圍在 1000-2000 之間。</span><span class="sxs-lookup"><span data-stu-id="f573a-124">Sku Capacity, value need to be multiple of 100 and in the range of 1000-2000.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f573a-125">-SKUName</span><span class="sxs-lookup"><span data-stu-id="f573a-125">-SkuName</span></span>
<span data-ttu-id="f573a-126">SKU 名稱，現在只能是 "CapacityReservation"</span><span class="sxs-lookup"><span data-stu-id="f573a-126">Sku Name, now can be 'CapacityReservation' only</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CapacityReservation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f573a-127">-標記</span><span class="sxs-lookup"><span data-stu-id="f573a-127">-Tags</span></span>
<span data-ttu-id="f573a-128">該組群的標記</span><span class="sxs-lookup"><span data-stu-id="f573a-128">Tags of the cluster</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f573a-129">-確認</span><span class="sxs-lookup"><span data-stu-id="f573a-129">-Confirm</span></span>
<span data-ttu-id="f573a-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f573a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f573a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f573a-131">-WhatIf</span></span>
<span data-ttu-id="f573a-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f573a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f573a-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f573a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f573a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f573a-134">CommonParameters</span></span>
<span data-ttu-id="f573a-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f573a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f573a-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f573a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f573a-137">輸入</span><span class="sxs-lookup"><span data-stu-id="f573a-137">INPUTS</span></span>

### <span data-ttu-id="f573a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f573a-138">System.String</span></span>

## <span data-ttu-id="f573a-139">輸出</span><span class="sxs-lookup"><span data-stu-id="f573a-139">OUTPUTS</span></span>

### <span data-ttu-id="f573a-140">Microsoft.Azure.Commands.OperationalInsights.models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="f573a-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="f573a-141">筆記</span><span class="sxs-lookup"><span data-stu-id="f573a-141">NOTES</span></span>

## <span data-ttu-id="f573a-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="f573a-142">RELATED LINKS</span></span>
