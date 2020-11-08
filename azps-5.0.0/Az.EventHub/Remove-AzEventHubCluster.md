---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
ms.openlocfilehash: e67d70f91e523cd46755035abe951682b1764cbc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136904"
---
# <span data-ttu-id="cc835-101">Remove-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="cc835-101">Remove-AzEventHubCluster</span></span>

## <span data-ttu-id="cc835-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cc835-102">SYNOPSIS</span></span>
<span data-ttu-id="cc835-103">從 ResourceGroup 中刪除指定的專用 Eventhub 群集</span><span class="sxs-lookup"><span data-stu-id="cc835-103">Deletes the specified Dedicated Eventhub Cluster from the ResourceGroup</span></span>

## <span data-ttu-id="cc835-104">句法</span><span class="sxs-lookup"><span data-stu-id="cc835-104">SYNTAX</span></span>

### <span data-ttu-id="cc835-105">ClusterPropertiesSet (預設) </span><span class="sxs-lookup"><span data-stu-id="cc835-105">ClusterPropertiesSet (Default)</span></span>
```
Remove-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc835-106">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cc835-106">ClusterInputObjectSet</span></span>
```
Remove-AzEventHubCluster [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc835-107">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc835-107">ClusterResourceIdParameterSet</span></span>
```
Remove-AzEventHubCluster [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc835-108">說明</span><span class="sxs-lookup"><span data-stu-id="cc835-108">DESCRIPTION</span></span>
<span data-ttu-id="cc835-109">Remove-AzEventHubCluster Cmdlet 會從指定的 resourcegroup 刪除指定的專用 eventhub 群集名稱</span><span class="sxs-lookup"><span data-stu-id="cc835-109">The Remove-AzEventHubCluster cmdlet deletes the given dedicated eventhub Cluster name from the given resourcegroup</span></span>

## <span data-ttu-id="cc835-110">示例</span><span class="sxs-lookup"><span data-stu-id="cc835-110">EXAMPLES</span></span>

### <span data-ttu-id="cc835-111">範例1</span><span class="sxs-lookup"><span data-stu-id="cc835-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557
```

<span data-ttu-id="cc835-112">從 RSG-Cluster27651 resourcegroup 刪除 Eventhub-群集-5557 群集</span><span class="sxs-lookup"><span data-stu-id="cc835-112">Deletes Eventhub-Cluster-5557 Cluster from RSG-Cluster27651 resourcegroup</span></span>

## <span data-ttu-id="cc835-113">參數</span><span class="sxs-lookup"><span data-stu-id="cc835-113">PARAMETERS</span></span>

### <span data-ttu-id="cc835-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc835-114">-AsJob</span></span>
<span data-ttu-id="cc835-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="cc835-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc835-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc835-116">-DefaultProfile</span></span>
<span data-ttu-id="cc835-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cc835-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc835-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc835-118">-InputObject</span></span>
<span data-ttu-id="cc835-119">群集物件</span><span class="sxs-lookup"><span data-stu-id="cc835-119">Cluster Object</span></span>

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

### <span data-ttu-id="cc835-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="cc835-120">-Name</span></span>
<span data-ttu-id="cc835-121">群集名稱</span><span class="sxs-lookup"><span data-stu-id="cc835-121">Cluster Name</span></span>

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

### <span data-ttu-id="cc835-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc835-122">-PassThru</span></span>
<span data-ttu-id="cc835-123">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="cc835-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="cc835-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc835-124">-ResourceGroupName</span></span>
<span data-ttu-id="cc835-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="cc835-125">Resource Group Name</span></span>

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

### <span data-ttu-id="cc835-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc835-126">-ResourceId</span></span>
<span data-ttu-id="cc835-127">群集資源識別碼</span><span class="sxs-lookup"><span data-stu-id="cc835-127">Cluster Resource Id</span></span>

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

### <span data-ttu-id="cc835-128">-確認</span><span class="sxs-lookup"><span data-stu-id="cc835-128">-Confirm</span></span>
<span data-ttu-id="cc835-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cc835-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc835-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc835-130">-WhatIf</span></span>
<span data-ttu-id="cc835-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc835-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc835-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc835-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc835-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc835-133">CommonParameters</span></span>
<span data-ttu-id="cc835-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cc835-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc835-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cc835-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc835-136">輸入</span><span class="sxs-lookup"><span data-stu-id="cc835-136">INPUTS</span></span>

### <span data-ttu-id="cc835-137">System.object</span><span class="sxs-lookup"><span data-stu-id="cc835-137">System.String</span></span>

### <span data-ttu-id="cc835-138">PSEventHubAttributes 的 [.]</span><span class="sxs-lookup"><span data-stu-id="cc835-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="cc835-139">輸出</span><span class="sxs-lookup"><span data-stu-id="cc835-139">OUTPUTS</span></span>

### <span data-ttu-id="cc835-140">System.object</span><span class="sxs-lookup"><span data-stu-id="cc835-140">System.Boolean</span></span>

## <span data-ttu-id="cc835-141">筆記</span><span class="sxs-lookup"><span data-stu-id="cc835-141">NOTES</span></span>

## <span data-ttu-id="cc835-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc835-142">RELATED LINKS</span></span>
