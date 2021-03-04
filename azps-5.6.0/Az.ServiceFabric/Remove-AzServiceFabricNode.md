---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: ba5400a35939a221b19ba144b35b0f2a53f6dbe9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915813"
---
# <span data-ttu-id="529f4-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="529f4-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="529f4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="529f4-102">SYNOPSIS</span></span>
<span data-ttu-id="529f4-103">從一個組移除特定節點類型的節點。</span><span class="sxs-lookup"><span data-stu-id="529f4-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="529f4-104">語法</span><span class="sxs-lookup"><span data-stu-id="529f4-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="529f4-105">描述</span><span class="sxs-lookup"><span data-stu-id="529f4-105">DESCRIPTION</span></span>
<span data-ttu-id="529f4-106">使用 **Remove-AzServiceFabricNode** 從組集中移除特定節點類型的節點。</span><span class="sxs-lookup"><span data-stu-id="529f4-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="529f4-107">只有在符合組群健康狀態計量時，才能繼續進行移除。</span><span class="sxs-lookup"><span data-stu-id="529f4-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="529f4-108">例子</span><span class="sxs-lookup"><span data-stu-id="529f4-108">EXAMPLES</span></span>

### <span data-ttu-id="529f4-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="529f4-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="529f4-110">此命令會從 NodeType 'nt1' 移除 2 個節點。</span><span class="sxs-lookup"><span data-stu-id="529f4-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="529f4-111">參數</span><span class="sxs-lookup"><span data-stu-id="529f4-111">PARAMETERS</span></span>

### <span data-ttu-id="529f4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="529f4-112">-DefaultProfile</span></span>
<span data-ttu-id="529f4-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="529f4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="529f4-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="529f4-114">-Name</span></span>
<span data-ttu-id="529f4-115">指定組名</span><span class="sxs-lookup"><span data-stu-id="529f4-115">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="529f4-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="529f4-116">-NodeType</span></span>
<span data-ttu-id="529f4-117">節點類型名稱</span><span class="sxs-lookup"><span data-stu-id="529f4-117">Node type name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="529f4-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="529f4-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="529f4-119">要新增的節點數目</span><span class="sxs-lookup"><span data-stu-id="529f4-119">The number of nodes to add</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Number

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="529f4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="529f4-120">-ResourceGroupName</span></span>
<span data-ttu-id="529f4-121">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="529f4-121">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="529f4-122">-確認</span><span class="sxs-lookup"><span data-stu-id="529f4-122">-Confirm</span></span>
<span data-ttu-id="529f4-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="529f4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="529f4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="529f4-124">-WhatIf</span></span>
<span data-ttu-id="529f4-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="529f4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="529f4-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="529f4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="529f4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="529f4-127">CommonParameters</span></span>
<span data-ttu-id="529f4-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="529f4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="529f4-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="529f4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="529f4-130">輸入</span><span class="sxs-lookup"><span data-stu-id="529f4-130">INPUTS</span></span>

### <span data-ttu-id="529f4-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="529f4-131">System.Int32</span></span>

### <span data-ttu-id="529f4-132">System.String</span><span class="sxs-lookup"><span data-stu-id="529f4-132">System.String</span></span>

## <span data-ttu-id="529f4-133">輸出</span><span class="sxs-lookup"><span data-stu-id="529f4-133">OUTPUTS</span></span>

### <span data-ttu-id="529f4-134">Microsoft.Azure.Commands.ServiceFabric.models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="529f4-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="529f4-135">筆記</span><span class="sxs-lookup"><span data-stu-id="529f4-135">NOTES</span></span>

## <span data-ttu-id="529f4-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="529f4-136">RELATED LINKS</span></span>

[<span data-ttu-id="529f4-137">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="529f4-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)
