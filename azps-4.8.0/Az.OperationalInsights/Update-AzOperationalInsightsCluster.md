---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/update-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Update-AzOperationalInsightsCluster.md
ms.openlocfilehash: 47d1c373fbbc9d078fced52e8695970acf8c9d7e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128881"
---
# <span data-ttu-id="ca315-101">Update-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="ca315-101">Update-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="ca315-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca315-102">SYNOPSIS</span></span>
<span data-ttu-id="ca315-103">更新群集</span><span class="sxs-lookup"><span data-stu-id="ca315-103">update cluster</span></span>

## <span data-ttu-id="ca315-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca315-104">SYNTAX</span></span>

```
Update-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-SkuName <String>]
 [-SkuCapacity <Int64>] [-KeyVaultUri <String>] [-KeyName <String>] [-KeyVersion <String>] [-Tags <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca315-105">說明</span><span class="sxs-lookup"><span data-stu-id="ca315-105">DESCRIPTION</span></span>
<span data-ttu-id="ca315-106">更新群集</span><span class="sxs-lookup"><span data-stu-id="ca315-106">update cluster</span></span>

## <span data-ttu-id="ca315-107">示例</span><span class="sxs-lookup"><span data-stu-id="ca315-107">EXAMPLES</span></span>

### <span data-ttu-id="ca315-108">範例1</span><span class="sxs-lookup"><span data-stu-id="ca315-108">Example 1</span></span>
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

<span data-ttu-id="ca315-109">使用主要 vault 屬性和 sku 更新群集</span><span class="sxs-lookup"><span data-stu-id="ca315-109">update cluster with key vault properties and sku</span></span>

## <span data-ttu-id="ca315-110">參數</span><span class="sxs-lookup"><span data-stu-id="ca315-110">PARAMETERS</span></span>

### <span data-ttu-id="ca315-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca315-111">-AsJob</span></span>
<span data-ttu-id="ca315-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ca315-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca315-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="ca315-113">-ClusterName</span></span>
<span data-ttu-id="ca315-114">[群集名稱]。</span><span class="sxs-lookup"><span data-stu-id="ca315-114">The cluster name.</span></span>

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

### <span data-ttu-id="ca315-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca315-115">-DefaultProfile</span></span>
<span data-ttu-id="ca315-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca315-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca315-117">-KeyName</span><span class="sxs-lookup"><span data-stu-id="ca315-117">-KeyName</span></span>
<span data-ttu-id="ca315-118">索引鍵名稱</span><span class="sxs-lookup"><span data-stu-id="ca315-118">Key Name</span></span>

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

### <span data-ttu-id="ca315-119">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="ca315-119">-KeyVaultUri</span></span>
<span data-ttu-id="ca315-120">必須針對此 keyvault 啟用主要保存庫 Uri、[清除保護] 和 [虛刪除]</span><span class="sxs-lookup"><span data-stu-id="ca315-120">Key Vault Uri, "Purge Protection" and "Soft Delete" have to be enabled for this keyvault</span></span>

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

### <span data-ttu-id="ca315-121">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="ca315-121">-KeyVersion</span></span>
<span data-ttu-id="ca315-122">金鑰版本</span><span class="sxs-lookup"><span data-stu-id="ca315-122">Key Version</span></span>

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

### <span data-ttu-id="ca315-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca315-123">-ResourceGroupName</span></span>
<span data-ttu-id="ca315-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca315-124">The resource group name.</span></span>

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

### <span data-ttu-id="ca315-125">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="ca315-125">-SkuCapacity</span></span>
<span data-ttu-id="ca315-126">Sku 容量</span><span class="sxs-lookup"><span data-stu-id="ca315-126">Sku Capacity</span></span>

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

### <span data-ttu-id="ca315-127">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ca315-127">-SkuName</span></span>
<span data-ttu-id="ca315-128">Sku 名稱，現在只能是「CapacityReservation」</span><span class="sxs-lookup"><span data-stu-id="ca315-128">Sku Name, now can be 'CapacityReservation' only</span></span>

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

### <span data-ttu-id="ca315-129">-標記</span><span class="sxs-lookup"><span data-stu-id="ca315-129">-Tags</span></span>
<span data-ttu-id="ca315-130">群集的標籤</span><span class="sxs-lookup"><span data-stu-id="ca315-130">Tags of the cluster</span></span>

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

### <span data-ttu-id="ca315-131">-確認</span><span class="sxs-lookup"><span data-stu-id="ca315-131">-Confirm</span></span>
<span data-ttu-id="ca315-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ca315-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca315-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca315-133">-WhatIf</span></span>
<span data-ttu-id="ca315-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca315-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca315-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca315-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca315-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca315-136">CommonParameters</span></span>
<span data-ttu-id="ca315-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca315-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca315-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ca315-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca315-139">輸入</span><span class="sxs-lookup"><span data-stu-id="ca315-139">INPUTS</span></span>

### <span data-ttu-id="ca315-140">System.object</span><span class="sxs-lookup"><span data-stu-id="ca315-140">System.String</span></span>

## <span data-ttu-id="ca315-141">輸出</span><span class="sxs-lookup"><span data-stu-id="ca315-141">OUTPUTS</span></span>

### <span data-ttu-id="ca315-142">PSLinkedService 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="ca315-142">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="ca315-143">筆記</span><span class="sxs-lookup"><span data-stu-id="ca315-143">NOTES</span></span>

## <span data-ttu-id="ca315-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca315-144">RELATED LINKS</span></span>
