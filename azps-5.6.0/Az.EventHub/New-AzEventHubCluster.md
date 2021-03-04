---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
ms.openlocfilehash: 4a76d54e4c8a3abda87fb9fd6de1d4439b051112
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903205"
---
# <span data-ttu-id="51277-101">New-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="51277-101">New-AzEventHubCluster</span></span>

## <span data-ttu-id="51277-102">簡介</span><span class="sxs-lookup"><span data-stu-id="51277-102">SYNOPSIS</span></span>
<span data-ttu-id="51277-103">建立新的專用事件中心組</span><span class="sxs-lookup"><span data-stu-id="51277-103">Creates a new dedicated eventhub cluster</span></span>

## <span data-ttu-id="51277-104">語法</span><span class="sxs-lookup"><span data-stu-id="51277-104">SYNTAX</span></span>

### <span data-ttu-id="51277-105">ClusterPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="51277-105">ClusterPropertiesSet (Default)</span></span>
```
New-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Capacity <Int32>]
 [-Tag <Hashtable>] [[-ResourceId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51277-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51277-106">ClusterResourceIdParameterSet</span></span>
```
New-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51277-107">描述</span><span class="sxs-lookup"><span data-stu-id="51277-107">DESCRIPTION</span></span>
<span data-ttu-id="51277-108">Cmdlet New-AzEventHubCluster在給定資源群組中建立專屬的事件中心群組</span><span class="sxs-lookup"><span data-stu-id="51277-108">The New-AzEventHubCluster cmdlet creates the dedicated eventhub cluster in the given resource group</span></span>

## <span data-ttu-id="51277-109">例子</span><span class="sxs-lookup"><span data-stu-id="51277-109">EXAMPLES</span></span>

### <span data-ttu-id="51277-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="51277-110">Example 1</span></span>
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

<span data-ttu-id="51277-111">在資源組 'RSG-Cluster27651' 中建立 'Eventhub-Cluster-5557' 專用組，位置為南中心，容量為 1</span><span class="sxs-lookup"><span data-stu-id="51277-111">Creates 'Eventhub-Cluster-5557' dedicated cluster in resourcegroup 'RSG-Cluster27651' with Location southcentralus and Capacity as 1</span></span>

## <span data-ttu-id="51277-112">參數</span><span class="sxs-lookup"><span data-stu-id="51277-112">PARAMETERS</span></span>

### <span data-ttu-id="51277-113">-容量</span><span class="sxs-lookup"><span data-stu-id="51277-113">-Capacity</span></span>
<span data-ttu-id="51277-114">Cluster Capacity (CU) ，) ， allowed value = 1</span><span class="sxs-lookup"><span data-stu-id="51277-114">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

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

### <span data-ttu-id="51277-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51277-115">-DefaultProfile</span></span>
<span data-ttu-id="51277-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="51277-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51277-117">-位置</span><span class="sxs-lookup"><span data-stu-id="51277-117">-Location</span></span>
<span data-ttu-id="51277-118">組群位置</span><span class="sxs-lookup"><span data-stu-id="51277-118">Location of Cluster</span></span>

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

### <span data-ttu-id="51277-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="51277-119">-Name</span></span>
<span data-ttu-id="51277-120">組名</span><span class="sxs-lookup"><span data-stu-id="51277-120">Cluster Name</span></span>

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

### <span data-ttu-id="51277-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51277-121">-ResourceGroupName</span></span>
<span data-ttu-id="51277-122">資源組名</span><span class="sxs-lookup"><span data-stu-id="51277-122">Resource Group Name</span></span>

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

### <span data-ttu-id="51277-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51277-123">-ResourceId</span></span>
<span data-ttu-id="51277-124">組群的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="51277-124">Resource ID of Cluster</span></span>

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

### <span data-ttu-id="51277-125">-標記</span><span class="sxs-lookup"><span data-stu-id="51277-125">-Tag</span></span>
<span data-ttu-id="51277-126">代表組群資源標記的雜湊表</span><span class="sxs-lookup"><span data-stu-id="51277-126">Hashtables which represents resource Tags for Clusters</span></span>

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

### <span data-ttu-id="51277-127">-確認</span><span class="sxs-lookup"><span data-stu-id="51277-127">-Confirm</span></span>
<span data-ttu-id="51277-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="51277-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51277-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51277-129">-WhatIf</span></span>
<span data-ttu-id="51277-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="51277-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51277-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="51277-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51277-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51277-132">CommonParameters</span></span>
<span data-ttu-id="51277-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="51277-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51277-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51277-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51277-135">輸入</span><span class="sxs-lookup"><span data-stu-id="51277-135">INPUTS</span></span>

### <span data-ttu-id="51277-136">System.String</span><span class="sxs-lookup"><span data-stu-id="51277-136">System.String</span></span>

### <span data-ttu-id="51277-137">System.Nullable'1[[System.Int32， mscorlib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="51277-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="51277-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="51277-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="51277-139">輸出</span><span class="sxs-lookup"><span data-stu-id="51277-139">OUTPUTS</span></span>

### <span data-ttu-id="51277-140">Microsoft.Azure.Commands.EventHub.models.PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="51277-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="51277-141">筆記</span><span class="sxs-lookup"><span data-stu-id="51277-141">NOTES</span></span>

## <span data-ttu-id="51277-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="51277-142">RELATED LINKS</span></span>
