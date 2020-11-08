---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCluster.md
ms.openlocfilehash: 078140a16a84089e5672fe160999d7db8577f7fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128893"
---
# <span data-ttu-id="b6987-101">New-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="b6987-101">New-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="b6987-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6987-102">SYNOPSIS</span></span>
<span data-ttu-id="b6987-103">建立群集</span><span class="sxs-lookup"><span data-stu-id="b6987-103">Create cluster</span></span>

## <span data-ttu-id="b6987-104">句法</span><span class="sxs-lookup"><span data-stu-id="b6987-104">SYNTAX</span></span>

```
New-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-Location] <String>
 [-IdentityType <String>] [-SkuName <String>] -SkuCapacity <Int64> [-Tags <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6987-105">說明</span><span class="sxs-lookup"><span data-stu-id="b6987-105">DESCRIPTION</span></span>

<span data-ttu-id="b6987-106">建立群集</span><span class="sxs-lookup"><span data-stu-id="b6987-106">Create cluster</span></span>

## <span data-ttu-id="b6987-107">示例</span><span class="sxs-lookup"><span data-stu-id="b6987-107">EXAMPLES</span></span>

### <span data-ttu-id="b6987-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b6987-108">Example 1</span></span>
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

<span data-ttu-id="b6987-109">建立群集</span><span class="sxs-lookup"><span data-stu-id="b6987-109">Create cluster</span></span>

## <span data-ttu-id="b6987-110">參數</span><span class="sxs-lookup"><span data-stu-id="b6987-110">PARAMETERS</span></span>

### <span data-ttu-id="b6987-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6987-111">-AsJob</span></span>
<span data-ttu-id="b6987-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b6987-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b6987-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b6987-113">-ClusterName</span></span>
<span data-ttu-id="b6987-114">[群集名稱]。</span><span class="sxs-lookup"><span data-stu-id="b6987-114">The cluster name.</span></span>

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

### <span data-ttu-id="b6987-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6987-115">-DefaultProfile</span></span>
<span data-ttu-id="b6987-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6987-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6987-117">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="b6987-117">-IdentityType</span></span>
<span data-ttu-id="b6987-118">身分識別類型、值可以是 "SystemAssigned"，"None"。</span><span class="sxs-lookup"><span data-stu-id="b6987-118">the identity type, value can be 'SystemAssigned', 'None'.</span></span>

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

### <span data-ttu-id="b6987-119">-位置</span><span class="sxs-lookup"><span data-stu-id="b6987-119">-Location</span></span>
<span data-ttu-id="b6987-120">將部署群集的地理區域。</span><span class="sxs-lookup"><span data-stu-id="b6987-120">The geographic region that the cluster will be deployed.</span></span>

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

### <span data-ttu-id="b6987-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6987-121">-ResourceGroupName</span></span>
<span data-ttu-id="b6987-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6987-122">The resource group name.</span></span>

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

### <span data-ttu-id="b6987-123">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="b6987-123">-SkuCapacity</span></span>
<span data-ttu-id="b6987-124">Sku 容量，值必須是100的倍數，且在1000-2000 的範圍內。</span><span class="sxs-lookup"><span data-stu-id="b6987-124">Sku Capacity, value need to be multiple of 100 and in the range of 1000-2000.</span></span>

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

### <span data-ttu-id="b6987-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b6987-125">-SkuName</span></span>
<span data-ttu-id="b6987-126">Sku 名稱，現在只能是「CapacityReservation」</span><span class="sxs-lookup"><span data-stu-id="b6987-126">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="b6987-127">-標記</span><span class="sxs-lookup"><span data-stu-id="b6987-127">-Tags</span></span>
<span data-ttu-id="b6987-128">群集的標籤</span><span class="sxs-lookup"><span data-stu-id="b6987-128">Tags of the cluster</span></span>

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

### <span data-ttu-id="b6987-129">-確認</span><span class="sxs-lookup"><span data-stu-id="b6987-129">-Confirm</span></span>
<span data-ttu-id="b6987-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b6987-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6987-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6987-131">-WhatIf</span></span>
<span data-ttu-id="b6987-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b6987-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6987-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b6987-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6987-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6987-134">CommonParameters</span></span>
<span data-ttu-id="b6987-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6987-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6987-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b6987-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6987-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b6987-137">INPUTS</span></span>

### <span data-ttu-id="b6987-138">System.object</span><span class="sxs-lookup"><span data-stu-id="b6987-138">System.String</span></span>

## <span data-ttu-id="b6987-139">輸出</span><span class="sxs-lookup"><span data-stu-id="b6987-139">OUTPUTS</span></span>

### <span data-ttu-id="b6987-140">PSCluster 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="b6987-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSCluster</span></span>

## <span data-ttu-id="b6987-141">筆記</span><span class="sxs-lookup"><span data-stu-id="b6987-141">NOTES</span></span>

## <span data-ttu-id="b6987-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6987-142">RELATED LINKS</span></span>