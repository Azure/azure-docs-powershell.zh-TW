---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/update-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
ms.openlocfilehash: f76ca0db3f4203bf1906c29c32c1973ea098789c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911517"
---
# <span data-ttu-id="814bc-101">Update-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="814bc-101">Update-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="814bc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="814bc-102">SYNOPSIS</span></span>
<span data-ttu-id="814bc-103">更新組</span><span class="sxs-lookup"><span data-stu-id="814bc-103">update cluster</span></span>

## <span data-ttu-id="814bc-104">語法</span><span class="sxs-lookup"><span data-stu-id="814bc-104">SYNTAX</span></span>

```
Update-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-SkuName <String>]
 [-SkuCapacity <Int64>] [-KeyVaultUri <String>] [-KeyName <String>] [-KeyVersion <String>] [-Tags <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="814bc-105">描述</span><span class="sxs-lookup"><span data-stu-id="814bc-105">DESCRIPTION</span></span>
<span data-ttu-id="814bc-106">更新組</span><span class="sxs-lookup"><span data-stu-id="814bc-106">update cluster</span></span>

## <span data-ttu-id="814bc-107">例子</span><span class="sxs-lookup"><span data-stu-id="814bc-107">EXAMPLES</span></span>

### <span data-ttu-id="814bc-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="814bc-108">Example 1</span></span>
```powershell
Update-AzOperationalInsightsCluster -ResourceGroupName azps-test-group -ClusterName yabo-cluster10 -Location eastus -SkuName CapacityReservation -SkuCapacity 1200 -KeyVaultUri {uri} -KeyName {key-name} -KeyVersion {version}

Identity           : Microsoft.Azure.Commands.OperationalInsights.Models.PSIdentity
Sku                : Microsoft.Azure.Commands.OperationalInsights.Models.PSClusterSku
NextLink           :
ClusterId          : {cluster-id}
ProvisioningState  : Updating
KeyVaultProperties :
Location           : South Central US
Id                 : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
Name               : {cluster-name}
Type               : Microsoft.OperationalInsights/clusters
Tags               : {}
```

<span data-ttu-id="814bc-109">具有金鑰庫屬性和 SKU 的更新組</span><span class="sxs-lookup"><span data-stu-id="814bc-109">update cluster with key vault properties and sku</span></span>

## <span data-ttu-id="814bc-110">參數</span><span class="sxs-lookup"><span data-stu-id="814bc-110">PARAMETERS</span></span>

### <span data-ttu-id="814bc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="814bc-111">-AsJob</span></span>
<span data-ttu-id="814bc-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="814bc-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="814bc-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="814bc-113">-ClusterName</span></span>
<span data-ttu-id="814bc-114">組名。</span><span class="sxs-lookup"><span data-stu-id="814bc-114">The cluster name.</span></span>

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

### <span data-ttu-id="814bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="814bc-115">-DefaultProfile</span></span>
<span data-ttu-id="814bc-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="814bc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="814bc-117">-KeyName</span><span class="sxs-lookup"><span data-stu-id="814bc-117">-KeyName</span></span>
<span data-ttu-id="814bc-118">金鑰名稱</span><span class="sxs-lookup"><span data-stu-id="814bc-118">Key Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="814bc-119">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="814bc-119">-KeyVaultUri</span></span>
<span data-ttu-id="814bc-120">金鑰庫 Uri、「清除保護」和「柔刪除」必須針對此 Keyvault 啟用</span><span class="sxs-lookup"><span data-stu-id="814bc-120">Key Vault Uri, "Purge Protection" and "Soft Delete" have to be enabled for this keyvault</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="814bc-121">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="814bc-121">-KeyVersion</span></span>
<span data-ttu-id="814bc-122">金鑰版本</span><span class="sxs-lookup"><span data-stu-id="814bc-122">Key Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="814bc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="814bc-123">-ResourceGroupName</span></span>
<span data-ttu-id="814bc-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="814bc-124">The resource group name.</span></span>

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

### <span data-ttu-id="814bc-125">-Sku以</span><span class="sxs-lookup"><span data-stu-id="814bc-125">-SkuCapacity</span></span>
<span data-ttu-id="814bc-126">SKU 容量</span><span class="sxs-lookup"><span data-stu-id="814bc-126">Sku Capacity</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="814bc-127">-SKUName</span><span class="sxs-lookup"><span data-stu-id="814bc-127">-SkuName</span></span>
<span data-ttu-id="814bc-128">SKU 名稱，現在只能是 "CapacityReservation"</span><span class="sxs-lookup"><span data-stu-id="814bc-128">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="814bc-129">-標記</span><span class="sxs-lookup"><span data-stu-id="814bc-129">-Tags</span></span>
<span data-ttu-id="814bc-130">該組群的標記</span><span class="sxs-lookup"><span data-stu-id="814bc-130">Tags of the cluster</span></span>

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

### <span data-ttu-id="814bc-131">-確認</span><span class="sxs-lookup"><span data-stu-id="814bc-131">-Confirm</span></span>
<span data-ttu-id="814bc-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="814bc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="814bc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="814bc-133">-WhatIf</span></span>
<span data-ttu-id="814bc-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="814bc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="814bc-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="814bc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="814bc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="814bc-136">CommonParameters</span></span>
<span data-ttu-id="814bc-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="814bc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="814bc-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="814bc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="814bc-139">輸入</span><span class="sxs-lookup"><span data-stu-id="814bc-139">INPUTS</span></span>

### <span data-ttu-id="814bc-140">System.String</span><span class="sxs-lookup"><span data-stu-id="814bc-140">System.String</span></span>

## <span data-ttu-id="814bc-141">輸出</span><span class="sxs-lookup"><span data-stu-id="814bc-141">OUTPUTS</span></span>

### <span data-ttu-id="814bc-142">Microsoft.Azure.Commands.OperationalInsights.models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="814bc-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="814bc-143">筆記</span><span class="sxs-lookup"><span data-stu-id="814bc-143">NOTES</span></span>

## <span data-ttu-id="814bc-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="814bc-144">RELATED LINKS</span></span>
