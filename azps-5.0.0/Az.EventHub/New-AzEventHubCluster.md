---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
ms.openlocfilehash: 2783b2c35cdae6afb2e0e73cd966dc2ddfa3e70c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140124"
---
# <span data-ttu-id="57f2d-101">New-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="57f2d-101">New-AzEventHubCluster</span></span>

## <span data-ttu-id="57f2d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="57f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="57f2d-103">建立新的專用 eventhub 群集</span><span class="sxs-lookup"><span data-stu-id="57f2d-103">Creates a new dedicated eventhub cluster</span></span>

## <span data-ttu-id="57f2d-104">句法</span><span class="sxs-lookup"><span data-stu-id="57f2d-104">SYNTAX</span></span>

### <span data-ttu-id="57f2d-105">ClusterPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="57f2d-105">ClusterPropertiesSet (Default)</span></span>
```
New-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Capacity <Int32>]
 [-Tag <Hashtable>] [[-ResourceId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57f2d-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57f2d-106">ClusterResourceIdParameterSet</span></span>
```
New-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57f2d-107">說明</span><span class="sxs-lookup"><span data-stu-id="57f2d-107">DESCRIPTION</span></span>
<span data-ttu-id="57f2d-108">New-AzEventHubCluster Cmdlet 會在指定的資源群組中建立專用的 eventhub 群集</span><span class="sxs-lookup"><span data-stu-id="57f2d-108">The New-AzEventHubCluster cmdlet creates the dedicated eventhub cluster in the given resource group</span></span>

## <span data-ttu-id="57f2d-109">示例</span><span class="sxs-lookup"><span data-stu-id="57f2d-109">EXAMPLES</span></span>

### <span data-ttu-id="57f2d-110">範例1</span><span class="sxs-lookup"><span data-stu-id="57f2d-110">Example 1</span></span>
```powershell
PS C:\>  New-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Location southcentralus -Capacity 1

Id        : /subscriptions/SubId/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag1, Tag1], [ClusterTag2, Tag2]}

```

<span data-ttu-id="57f2d-111">在 resourcegroup "RSG-Cluster27651" 中建立「Eventhub-Cluster-5557」專用群集，並將位置 southcentralus 和容量設為1</span><span class="sxs-lookup"><span data-stu-id="57f2d-111">Creates 'Eventhub-Cluster-5557' dedicated cluster in resourcegroup 'RSG-Cluster27651' with Location southcentralus and Capacity as 1</span></span>

## <span data-ttu-id="57f2d-112">參數</span><span class="sxs-lookup"><span data-stu-id="57f2d-112">PARAMETERS</span></span>

### <span data-ttu-id="57f2d-113">-容量</span><span class="sxs-lookup"><span data-stu-id="57f2d-113">-Capacity</span></span>
<span data-ttu-id="57f2d-114">群集容量 (CU) ，curerntrly，允許值 = 1</span><span class="sxs-lookup"><span data-stu-id="57f2d-114">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="57f2d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57f2d-115">-DefaultProfile</span></span>
<span data-ttu-id="57f2d-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="57f2d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57f2d-117">-位置</span><span class="sxs-lookup"><span data-stu-id="57f2d-117">-Location</span></span>
<span data-ttu-id="57f2d-118">群集的位置</span><span class="sxs-lookup"><span data-stu-id="57f2d-118">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f2d-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="57f2d-119">-Name</span></span>
<span data-ttu-id="57f2d-120">群集名稱</span><span class="sxs-lookup"><span data-stu-id="57f2d-120">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f2d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57f2d-121">-ResourceGroupName</span></span>
<span data-ttu-id="57f2d-122">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="57f2d-122">Resource Group Name</span></span>

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

### <span data-ttu-id="57f2d-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57f2d-123">-ResourceId</span></span>
<span data-ttu-id="57f2d-124">群集的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="57f2d-124">Resource ID of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="57f2d-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="57f2d-125">-Tag</span></span>
<span data-ttu-id="57f2d-126">代表群集之資源標記的 Hashtables</span><span class="sxs-lookup"><span data-stu-id="57f2d-126">Hashtables which represents resource Tags for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f2d-127">-確認</span><span class="sxs-lookup"><span data-stu-id="57f2d-127">-Confirm</span></span>
<span data-ttu-id="57f2d-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="57f2d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57f2d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57f2d-129">-WhatIf</span></span>
<span data-ttu-id="57f2d-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="57f2d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57f2d-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57f2d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57f2d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f2d-132">CommonParameters</span></span>
<span data-ttu-id="57f2d-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="57f2d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f2d-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="57f2d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f2d-135">輸入</span><span class="sxs-lookup"><span data-stu-id="57f2d-135">INPUTS</span></span>

### <span data-ttu-id="57f2d-136">System.object</span><span class="sxs-lookup"><span data-stu-id="57f2d-136">System.String</span></span>

### <span data-ttu-id="57f2d-137">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="57f2d-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="57f2d-138">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="57f2d-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="57f2d-139">輸出</span><span class="sxs-lookup"><span data-stu-id="57f2d-139">OUTPUTS</span></span>

### <span data-ttu-id="57f2d-140">PSEventHubClusterAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="57f2d-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="57f2d-141">筆記</span><span class="sxs-lookup"><span data-stu-id="57f2d-141">NOTES</span></span>

## <span data-ttu-id="57f2d-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="57f2d-142">RELATED LINKS</span></span>
