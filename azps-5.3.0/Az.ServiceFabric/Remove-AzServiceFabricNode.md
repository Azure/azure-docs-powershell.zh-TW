---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: fd38b68c8133cbc498bbc50ffea84b48e58198a9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448172"
---
# <span data-ttu-id="50886-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="50886-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="50886-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50886-102">SYNOPSIS</span></span>
<span data-ttu-id="50886-103">從群集中移除特定節點類型的節點。</span><span class="sxs-lookup"><span data-stu-id="50886-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="50886-104">句法</span><span class="sxs-lookup"><span data-stu-id="50886-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50886-105">說明</span><span class="sxs-lookup"><span data-stu-id="50886-105">DESCRIPTION</span></span>
<span data-ttu-id="50886-106">使用 [ **移除-AzServiceFabricNode** ] 從群集中移除特定節點類型的節點。</span><span class="sxs-lookup"><span data-stu-id="50886-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="50886-107">移除只會在符合群集健康情況指標時進行。</span><span class="sxs-lookup"><span data-stu-id="50886-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="50886-108">示例</span><span class="sxs-lookup"><span data-stu-id="50886-108">EXAMPLES</span></span>

### <span data-ttu-id="50886-109">範例1</span><span class="sxs-lookup"><span data-stu-id="50886-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeType 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="50886-110">這個命令會從 NodeType "nt1" 移除2個節點。</span><span class="sxs-lookup"><span data-stu-id="50886-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="50886-111">參數</span><span class="sxs-lookup"><span data-stu-id="50886-111">PARAMETERS</span></span>

### <span data-ttu-id="50886-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50886-112">-DefaultProfile</span></span>
<span data-ttu-id="50886-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="50886-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50886-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="50886-114">-Name</span></span>
<span data-ttu-id="50886-115">指定群集的名稱</span><span class="sxs-lookup"><span data-stu-id="50886-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="50886-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="50886-116">-NodeType</span></span>
<span data-ttu-id="50886-117">節點類型名稱</span><span class="sxs-lookup"><span data-stu-id="50886-117">Node type name</span></span>

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

### <span data-ttu-id="50886-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="50886-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="50886-119">要新增的節點數</span><span class="sxs-lookup"><span data-stu-id="50886-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="50886-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50886-120">-ResourceGroupName</span></span>
<span data-ttu-id="50886-121">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="50886-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="50886-122">-確認</span><span class="sxs-lookup"><span data-stu-id="50886-122">-Confirm</span></span>
<span data-ttu-id="50886-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="50886-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50886-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50886-124">-WhatIf</span></span>
<span data-ttu-id="50886-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="50886-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50886-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50886-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50886-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50886-127">CommonParameters</span></span>
<span data-ttu-id="50886-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50886-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50886-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="50886-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50886-130">輸入</span><span class="sxs-lookup"><span data-stu-id="50886-130">INPUTS</span></span>

### <span data-ttu-id="50886-131">System.object</span><span class="sxs-lookup"><span data-stu-id="50886-131">System.Int32</span></span>

### <span data-ttu-id="50886-132">System.object</span><span class="sxs-lookup"><span data-stu-id="50886-132">System.String</span></span>

## <span data-ttu-id="50886-133">輸出</span><span class="sxs-lookup"><span data-stu-id="50886-133">OUTPUTS</span></span>

### <span data-ttu-id="50886-134">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="50886-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="50886-135">筆記</span><span class="sxs-lookup"><span data-stu-id="50886-135">NOTES</span></span>

## <span data-ttu-id="50886-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="50886-136">RELATED LINKS</span></span>

[<span data-ttu-id="50886-137">附加 AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="50886-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)
