---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
ms.openlocfilehash: 3fb0030d6475ab3fb41f78ab1dc1a54870ed2f8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914002"
---
# <span data-ttu-id="256d7-101">Set-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="256d7-101">Set-AzEventHubCluster</span></span>

## <span data-ttu-id="256d7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="256d7-102">SYNOPSIS</span></span>
<span data-ttu-id="256d7-103">更新給定組群的標記</span><span class="sxs-lookup"><span data-stu-id="256d7-103">Updates the Tag for the given Cluster</span></span>

## <span data-ttu-id="256d7-104">語法</span><span class="sxs-lookup"><span data-stu-id="256d7-104">SYNTAX</span></span>

### <span data-ttu-id="256d7-105">ClusterPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="256d7-105">ClusterPropertiesSet (Default)</span></span>
```
Set-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-Capacity <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="256d7-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="256d7-106">ClusterResourceIdParameterSet</span></span>
```
Set-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="256d7-107">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="256d7-107">ClusterInputObjectSet</span></span>
```
Set-AzEventHubCluster [-InputObject] <PSEventHubClusterAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="256d7-108">描述</span><span class="sxs-lookup"><span data-stu-id="256d7-108">DESCRIPTION</span></span>
<span data-ttu-id="256d7-109">此Set-AzEventHubCluster Cmdlet 會更新所給予之組群的標籤</span><span class="sxs-lookup"><span data-stu-id="256d7-109">The Set-AzEventHubCluster cmdlet updates tags of the given cluster</span></span>

## <span data-ttu-id="256d7-110">例子</span><span class="sxs-lookup"><span data-stu-id="256d7-110">EXAMPLES</span></span>

### <span data-ttu-id="256d7-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="256d7-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Tag @{"ClusterTag3" = "Tag3"; "ClusterTag4" = "Tag4";}

Id        : /subscriptions/{SubID}/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag3, Tag3], [ClusterTag4, Tag4]}
```

<span data-ttu-id="256d7-112">更新給定組群的標記。</span><span class="sxs-lookup"><span data-stu-id="256d7-112">Updates tags of the given cluster.</span></span> 

## <span data-ttu-id="256d7-113">參數</span><span class="sxs-lookup"><span data-stu-id="256d7-113">PARAMETERS</span></span>

### <span data-ttu-id="256d7-114">-容量</span><span class="sxs-lookup"><span data-stu-id="256d7-114">-Capacity</span></span>
<span data-ttu-id="256d7-115">Cluster Capacity (CU) ，) ， allowed value = 1</span><span class="sxs-lookup"><span data-stu-id="256d7-115">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="256d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="256d7-116">-DefaultProfile</span></span>
<span data-ttu-id="256d7-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="256d7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="256d7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="256d7-118">-InputObject</span></span>
<span data-ttu-id="256d7-119">組名</span><span class="sxs-lookup"><span data-stu-id="256d7-119">Cluster Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="256d7-120">-位置</span><span class="sxs-lookup"><span data-stu-id="256d7-120">-Location</span></span>
<span data-ttu-id="256d7-121">組群位置</span><span class="sxs-lookup"><span data-stu-id="256d7-121">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="256d7-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="256d7-122">-Name</span></span>
<span data-ttu-id="256d7-123">組名</span><span class="sxs-lookup"><span data-stu-id="256d7-123">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="256d7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="256d7-124">-ResourceGroupName</span></span>
<span data-ttu-id="256d7-125">資源組名</span><span class="sxs-lookup"><span data-stu-id="256d7-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="256d7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="256d7-126">-ResourceId</span></span>
<span data-ttu-id="256d7-127">組群的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="256d7-127">Resource ID of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="256d7-128">-標記</span><span class="sxs-lookup"><span data-stu-id="256d7-128">-Tag</span></span>
<span data-ttu-id="256d7-129">代表組群資源標記的雜湊表</span><span class="sxs-lookup"><span data-stu-id="256d7-129">Hashtables which represents resource Tag for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet, ClusterResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="256d7-130">-確認</span><span class="sxs-lookup"><span data-stu-id="256d7-130">-Confirm</span></span>
<span data-ttu-id="256d7-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="256d7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="256d7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="256d7-132">-WhatIf</span></span>
<span data-ttu-id="256d7-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="256d7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="256d7-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="256d7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="256d7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="256d7-135">CommonParameters</span></span>
<span data-ttu-id="256d7-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="256d7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="256d7-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="256d7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="256d7-138">輸入</span><span class="sxs-lookup"><span data-stu-id="256d7-138">INPUTS</span></span>

### <span data-ttu-id="256d7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="256d7-139">System.String</span></span>

### <span data-ttu-id="256d7-140">System.Nullable'1[[System.Int32， mscorlib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="256d7-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="256d7-141">Microsoft.Azure.Commands.EventHub.models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="256d7-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

### <span data-ttu-id="256d7-142">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="256d7-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="256d7-143">輸出</span><span class="sxs-lookup"><span data-stu-id="256d7-143">OUTPUTS</span></span>

### <span data-ttu-id="256d7-144">Microsoft.Azure.Commands.EventHub.models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="256d7-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="256d7-145">筆記</span><span class="sxs-lookup"><span data-stu-id="256d7-145">NOTES</span></span>

## <span data-ttu-id="256d7-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="256d7-146">RELATED LINKS</span></span>
