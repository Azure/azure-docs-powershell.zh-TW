---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/add-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricNode.md
ms.openlocfilehash: 34b55a5da226a3985cb6fe3bede244ee1e054726
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909938"
---
# <span data-ttu-id="e5ea8-101">Add-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="e5ea8-101">Add-AzServiceFabricNode</span></span>

## <span data-ttu-id="e5ea8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e5ea8-102">SYNOPSIS</span></span>
<span data-ttu-id="e5ea8-103">將節點新增到該群中的特定節點類型。</span><span class="sxs-lookup"><span data-stu-id="e5ea8-103">Add nodes to the specific node type in the cluster.</span></span>

## <span data-ttu-id="e5ea8-104">語法</span><span class="sxs-lookup"><span data-stu-id="e5ea8-104">SYNTAX</span></span>

```
Add-AzServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5ea8-105">描述</span><span class="sxs-lookup"><span data-stu-id="e5ea8-105">DESCRIPTION</span></span>
<span data-ttu-id="e5ea8-106">使用 **Add-AzServiceFabricNode** 將節點新增到特定的節點類型。</span><span class="sxs-lookup"><span data-stu-id="e5ea8-106">Use **Add-AzServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="e5ea8-107">您只需要指定要新加入節點類型的節點數目。</span><span class="sxs-lookup"><span data-stu-id="e5ea8-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="e5ea8-108">例子</span><span class="sxs-lookup"><span data-stu-id="e5ea8-108">EXAMPLES</span></span>

### <span data-ttu-id="e5ea8-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="e5ea8-109">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="e5ea8-110">此命令將新增 2 個節點至節點類型 'n1'。</span><span class="sxs-lookup"><span data-stu-id="e5ea8-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="e5ea8-111">參數</span><span class="sxs-lookup"><span data-stu-id="e5ea8-111">PARAMETERS</span></span>

### <span data-ttu-id="e5ea8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5ea8-112">-DefaultProfile</span></span>
<span data-ttu-id="e5ea8-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5ea8-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5ea8-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5ea8-114">-Name</span></span>
<span data-ttu-id="e5ea8-115">指定組名</span><span class="sxs-lookup"><span data-stu-id="e5ea8-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="e5ea8-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="e5ea8-116">-NodeType</span></span>
<span data-ttu-id="e5ea8-117">節點類型名稱</span><span class="sxs-lookup"><span data-stu-id="e5ea8-117">Node type name</span></span>

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

### <span data-ttu-id="e5ea8-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="e5ea8-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="e5ea8-119">要新增的節點數目</span><span class="sxs-lookup"><span data-stu-id="e5ea8-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="e5ea8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5ea8-120">-ResourceGroupName</span></span>
<span data-ttu-id="e5ea8-121">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5ea8-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e5ea8-122">-確認</span><span class="sxs-lookup"><span data-stu-id="e5ea8-122">-Confirm</span></span>
<span data-ttu-id="e5ea8-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e5ea8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5ea8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5ea8-124">-WhatIf</span></span>
<span data-ttu-id="e5ea8-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5ea8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5ea8-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5ea8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5ea8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5ea8-127">CommonParameters</span></span>
<span data-ttu-id="e5ea8-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e5ea8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5ea8-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5ea8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5ea8-130">輸入</span><span class="sxs-lookup"><span data-stu-id="e5ea8-130">INPUTS</span></span>

### <span data-ttu-id="e5ea8-131">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e5ea8-131">System.Int32</span></span>

### <span data-ttu-id="e5ea8-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e5ea8-132">System.String</span></span>

## <span data-ttu-id="e5ea8-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e5ea8-133">OUTPUTS</span></span>

### <span data-ttu-id="e5ea8-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="e5ea8-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="e5ea8-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e5ea8-135">NOTES</span></span>

## <span data-ttu-id="e5ea8-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5ea8-136">RELATED LINKS</span></span>

[<span data-ttu-id="e5ea8-137">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="e5ea8-137">Remove-AzServiceFabricNode</span></span>](./Remove-AzServiceFabricNode.md)
