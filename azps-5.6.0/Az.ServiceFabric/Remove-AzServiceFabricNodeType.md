---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: 8d0bd6f046bbff99d93b0ed5dc7385d8ec772811
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915810"
---
# <span data-ttu-id="bb99a-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="bb99a-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="bb99a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bb99a-102">SYNOPSIS</span></span>
<span data-ttu-id="bb99a-103">從一個組移除完整的節點類型。</span><span class="sxs-lookup"><span data-stu-id="bb99a-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="bb99a-104">語法</span><span class="sxs-lookup"><span data-stu-id="bb99a-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb99a-105">描述</span><span class="sxs-lookup"><span data-stu-id="bb99a-105">DESCRIPTION</span></span>
<span data-ttu-id="bb99a-106">使用 **Remove-AzServiceFabricNodeType** 從特定節點類型移除所有節點，以及從一個集區移除節點類型。</span><span class="sxs-lookup"><span data-stu-id="bb99a-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="bb99a-107">此命令無法用來刪除主要節點類型。</span><span class="sxs-lookup"><span data-stu-id="bb99a-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="bb99a-108">例子</span><span class="sxs-lookup"><span data-stu-id="bb99a-108">EXAMPLES</span></span>

### <span data-ttu-id="bb99a-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="bb99a-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="bb99a-110">此命令會從組群移除 NodeType 'nt1'。</span><span class="sxs-lookup"><span data-stu-id="bb99a-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="bb99a-111">參數</span><span class="sxs-lookup"><span data-stu-id="bb99a-111">PARAMETERS</span></span>

### <span data-ttu-id="bb99a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb99a-112">-DefaultProfile</span></span>
<span data-ttu-id="bb99a-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bb99a-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb99a-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="bb99a-114">-Name</span></span>
<span data-ttu-id="bb99a-115">指定組名</span><span class="sxs-lookup"><span data-stu-id="bb99a-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="bb99a-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="bb99a-116">-NodeType</span></span>
<span data-ttu-id="bb99a-117">節點類型名稱</span><span class="sxs-lookup"><span data-stu-id="bb99a-117">The node type name</span></span>

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

### <span data-ttu-id="bb99a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb99a-118">-ResourceGroupName</span></span>
<span data-ttu-id="bb99a-119">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb99a-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="bb99a-120">-確認</span><span class="sxs-lookup"><span data-stu-id="bb99a-120">-Confirm</span></span>
<span data-ttu-id="bb99a-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="bb99a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb99a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb99a-122">-WhatIf</span></span>
<span data-ttu-id="bb99a-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bb99a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb99a-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bb99a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb99a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb99a-125">CommonParameters</span></span>
<span data-ttu-id="bb99a-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bb99a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb99a-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb99a-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb99a-128">輸入</span><span class="sxs-lookup"><span data-stu-id="bb99a-128">INPUTS</span></span>

### <span data-ttu-id="bb99a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="bb99a-129">System.String</span></span>

## <span data-ttu-id="bb99a-130">輸出</span><span class="sxs-lookup"><span data-stu-id="bb99a-130">OUTPUTS</span></span>

### <span data-ttu-id="bb99a-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="bb99a-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="bb99a-132">筆記</span><span class="sxs-lookup"><span data-stu-id="bb99a-132">NOTES</span></span>

## <span data-ttu-id="bb99a-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb99a-133">RELATED LINKS</span></span>
