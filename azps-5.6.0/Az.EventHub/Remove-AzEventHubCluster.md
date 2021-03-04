---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
ms.openlocfilehash: 7ba6a5f95c1cc37f7cdef7d8ead7a2514927e089
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912402"
---
# <span data-ttu-id="d6cb0-101">Remove-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="d6cb0-101">Remove-AzEventHubCluster</span></span>

## <span data-ttu-id="d6cb0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d6cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="d6cb0-103">從 ResourceGroup 刪除指定的 Dedicated Eventhub 群</span><span class="sxs-lookup"><span data-stu-id="d6cb0-103">Deletes the specified Dedicated Eventhub Cluster from the ResourceGroup</span></span>

## <span data-ttu-id="d6cb0-104">語法</span><span class="sxs-lookup"><span data-stu-id="d6cb0-104">SYNTAX</span></span>

### <span data-ttu-id="d6cb0-105">ClusterPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d6cb0-105">ClusterPropertiesSet (Default)</span></span>
```
Remove-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6cb0-106">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d6cb0-106">ClusterInputObjectSet</span></span>
```
Remove-AzEventHubCluster [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6cb0-107">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6cb0-107">ClusterResourceIdParameterSet</span></span>
```
Remove-AzEventHubCluster [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6cb0-108">描述</span><span class="sxs-lookup"><span data-stu-id="d6cb0-108">DESCRIPTION</span></span>
<span data-ttu-id="d6cb0-109">Cmdlet Remove-AzEventHubCluster從指定資源組刪除指定專屬的 eventhub Cluster 名稱</span><span class="sxs-lookup"><span data-stu-id="d6cb0-109">The Remove-AzEventHubCluster cmdlet deletes the given dedicated eventhub Cluster name from the given resourcegroup</span></span>

## <span data-ttu-id="d6cb0-110">例子</span><span class="sxs-lookup"><span data-stu-id="d6cb0-110">EXAMPLES</span></span>

### <span data-ttu-id="d6cb0-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="d6cb0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557
```

<span data-ttu-id="d6cb0-112">從資源組刪除 Eventhub-Cluster-5557 RSG-Cluster27651群</span><span class="sxs-lookup"><span data-stu-id="d6cb0-112">Deletes Eventhub-Cluster-5557 Cluster from RSG-Cluster27651 resourcegroup</span></span>

## <span data-ttu-id="d6cb0-113">參數</span><span class="sxs-lookup"><span data-stu-id="d6cb0-113">PARAMETERS</span></span>

### <span data-ttu-id="d6cb0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d6cb0-114">-AsJob</span></span>
<span data-ttu-id="d6cb0-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d6cb0-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6cb0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6cb0-116">-DefaultProfile</span></span>
<span data-ttu-id="d6cb0-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d6cb0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6cb0-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6cb0-118">-InputObject</span></span>
<span data-ttu-id="d6cb0-119">Cluster 物件</span><span class="sxs-lookup"><span data-stu-id="d6cb0-119">Cluster Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6cb0-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="d6cb0-120">-Name</span></span>
<span data-ttu-id="d6cb0-121">組名</span><span class="sxs-lookup"><span data-stu-id="d6cb0-121">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6cb0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6cb0-122">-PassThru</span></span>
<span data-ttu-id="d6cb0-123">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="d6cb0-123">{{ Fill PassThru Description }}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6cb0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6cb0-124">-ResourceGroupName</span></span>
<span data-ttu-id="d6cb0-125">資源組名</span><span class="sxs-lookup"><span data-stu-id="d6cb0-125">Resource Group Name</span></span>

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

### <span data-ttu-id="d6cb0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6cb0-126">-ResourceId</span></span>
<span data-ttu-id="d6cb0-127">組群資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d6cb0-127">Cluster Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6cb0-128">-確認</span><span class="sxs-lookup"><span data-stu-id="d6cb0-128">-Confirm</span></span>
<span data-ttu-id="d6cb0-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d6cb0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6cb0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6cb0-130">-WhatIf</span></span>
<span data-ttu-id="d6cb0-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d6cb0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6cb0-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d6cb0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6cb0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6cb0-133">CommonParameters</span></span>
<span data-ttu-id="d6cb0-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d6cb0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6cb0-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6cb0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6cb0-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d6cb0-136">INPUTS</span></span>

### <span data-ttu-id="d6cb0-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d6cb0-137">System.String</span></span>

### <span data-ttu-id="d6cb0-138">Microsoft.Azure.Commands.EventHub.models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="d6cb0-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="d6cb0-139">輸出</span><span class="sxs-lookup"><span data-stu-id="d6cb0-139">OUTPUTS</span></span>

### <span data-ttu-id="d6cb0-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d6cb0-140">System.Boolean</span></span>

## <span data-ttu-id="d6cb0-141">筆記</span><span class="sxs-lookup"><span data-stu-id="d6cb0-141">NOTES</span></span>

## <span data-ttu-id="d6cb0-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6cb0-142">RELATED LINKS</span></span>
