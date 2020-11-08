---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubCluster.md
ms.openlocfilehash: 3e78e302aafb3e59293f04ade7035e5b4ebbd84c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140515"
---
# <span data-ttu-id="6c3e9-101">Set-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="6c3e9-101">Set-AzEventHubCluster</span></span>

## <span data-ttu-id="6c3e9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6c3e9-102">SYNOPSIS</span></span>
<span data-ttu-id="6c3e9-103">更新指定群集的標籤</span><span class="sxs-lookup"><span data-stu-id="6c3e9-103">Updates the Tag for the given Cluster</span></span>

## <span data-ttu-id="6c3e9-104">句法</span><span class="sxs-lookup"><span data-stu-id="6c3e9-104">SYNTAX</span></span>

### <span data-ttu-id="6c3e9-105">ClusterPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6c3e9-105">ClusterPropertiesSet (Default)</span></span>
```
Set-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-Capacity <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c3e9-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c3e9-106">ClusterResourceIdParameterSet</span></span>
```
Set-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c3e9-107">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6c3e9-107">ClusterInputObjectSet</span></span>
```
Set-AzEventHubCluster [-InputObject] <PSEventHubClusterAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c3e9-108">說明</span><span class="sxs-lookup"><span data-stu-id="6c3e9-108">DESCRIPTION</span></span>
<span data-ttu-id="6c3e9-109">Set-AzEventHubCluster Cmdlet 會更新指定群集的標記</span><span class="sxs-lookup"><span data-stu-id="6c3e9-109">The Set-AzEventHubCluster cmdlet updates tags of the given cluster</span></span>

## <span data-ttu-id="6c3e9-110">示例</span><span class="sxs-lookup"><span data-stu-id="6c3e9-110">EXAMPLES</span></span>

### <span data-ttu-id="6c3e9-111">範例1</span><span class="sxs-lookup"><span data-stu-id="6c3e9-111">Example 1</span></span>
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

<span data-ttu-id="6c3e9-112">更新指定群集的標籤。</span><span class="sxs-lookup"><span data-stu-id="6c3e9-112">Updates tags of the given cluster.</span></span> 

## <span data-ttu-id="6c3e9-113">參數</span><span class="sxs-lookup"><span data-stu-id="6c3e9-113">PARAMETERS</span></span>

### <span data-ttu-id="6c3e9-114">-容量</span><span class="sxs-lookup"><span data-stu-id="6c3e9-114">-Capacity</span></span>
<span data-ttu-id="6c3e9-115">群集容量 (CU) ，curerntrly，允許值 = 1</span><span class="sxs-lookup"><span data-stu-id="6c3e9-115">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="6c3e9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c3e9-116">-DefaultProfile</span></span>
<span data-ttu-id="6c3e9-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6c3e9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c3e9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c3e9-118">-InputObject</span></span>
<span data-ttu-id="6c3e9-119">群集名稱</span><span class="sxs-lookup"><span data-stu-id="6c3e9-119">Cluster Name</span></span>

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

### <span data-ttu-id="6c3e9-120">-位置</span><span class="sxs-lookup"><span data-stu-id="6c3e9-120">-Location</span></span>
<span data-ttu-id="6c3e9-121">群集的位置</span><span class="sxs-lookup"><span data-stu-id="6c3e9-121">Location of Cluster</span></span>

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

### <span data-ttu-id="6c3e9-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="6c3e9-122">-Name</span></span>
<span data-ttu-id="6c3e9-123">群集名稱</span><span class="sxs-lookup"><span data-stu-id="6c3e9-123">Cluster Name</span></span>

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

### <span data-ttu-id="6c3e9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c3e9-124">-ResourceGroupName</span></span>
<span data-ttu-id="6c3e9-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="6c3e9-125">Resource Group Name</span></span>

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

### <span data-ttu-id="6c3e9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c3e9-126">-ResourceId</span></span>
<span data-ttu-id="6c3e9-127">群集的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6c3e9-127">Resource ID of Cluster</span></span>

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

### <span data-ttu-id="6c3e9-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="6c3e9-128">-Tag</span></span>
<span data-ttu-id="6c3e9-129">代表群集之資源標記的 Hashtables</span><span class="sxs-lookup"><span data-stu-id="6c3e9-129">Hashtables which represents resource Tag for Clusters</span></span>

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

### <span data-ttu-id="6c3e9-130">-確認</span><span class="sxs-lookup"><span data-stu-id="6c3e9-130">-Confirm</span></span>
<span data-ttu-id="6c3e9-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6c3e9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c3e9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c3e9-132">-WhatIf</span></span>
<span data-ttu-id="6c3e9-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6c3e9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c3e9-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c3e9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c3e9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c3e9-135">CommonParameters</span></span>
<span data-ttu-id="6c3e9-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6c3e9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c3e9-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="6c3e9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c3e9-138">輸入</span><span class="sxs-lookup"><span data-stu-id="6c3e9-138">INPUTS</span></span>

### <span data-ttu-id="6c3e9-139">System.object</span><span class="sxs-lookup"><span data-stu-id="6c3e9-139">System.String</span></span>

### <span data-ttu-id="6c3e9-140">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="6c3e9-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="6c3e9-141">PSEventHubClusterAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="6c3e9-141">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

### <span data-ttu-id="6c3e9-142">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6c3e9-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6c3e9-143">輸出</span><span class="sxs-lookup"><span data-stu-id="6c3e9-143">OUTPUTS</span></span>

### <span data-ttu-id="6c3e9-144">PSEventHubClusterAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="6c3e9-144">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="6c3e9-145">筆記</span><span class="sxs-lookup"><span data-stu-id="6c3e9-145">NOTES</span></span>

## <span data-ttu-id="6c3e9-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c3e9-146">RELATED LINKS</span></span>