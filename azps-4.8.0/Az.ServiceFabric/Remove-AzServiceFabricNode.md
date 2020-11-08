---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: 3580315755792aaaddf3b10e185413254784a3d7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129892"
---
# <span data-ttu-id="ab3ac-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="ab3ac-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="ab3ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ab3ac-102">SYNOPSIS</span></span>
<span data-ttu-id="ab3ac-103">從群集中移除特定節點類型的節點。</span><span class="sxs-lookup"><span data-stu-id="ab3ac-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="ab3ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="ab3ac-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab3ac-105">說明</span><span class="sxs-lookup"><span data-stu-id="ab3ac-105">DESCRIPTION</span></span>
<span data-ttu-id="ab3ac-106">使用 [ **移除-AzServiceFabricNode** ] 從群集中移除特定節點類型的節點。</span><span class="sxs-lookup"><span data-stu-id="ab3ac-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="ab3ac-107">移除只會在符合群集健康情況指標時進行。</span><span class="sxs-lookup"><span data-stu-id="ab3ac-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="ab3ac-108">示例</span><span class="sxs-lookup"><span data-stu-id="ab3ac-108">EXAMPLES</span></span>

### <span data-ttu-id="ab3ac-109">範例1</span><span class="sxs-lookup"><span data-stu-id="ab3ac-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="ab3ac-110">這個命令會從 NodeType "nt1" 移除2個節點。</span><span class="sxs-lookup"><span data-stu-id="ab3ac-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="ab3ac-111">參數</span><span class="sxs-lookup"><span data-stu-id="ab3ac-111">PARAMETERS</span></span>

### <span data-ttu-id="ab3ac-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab3ac-112">-DefaultProfile</span></span>
<span data-ttu-id="ab3ac-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ab3ac-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab3ac-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="ab3ac-114">-Name</span></span>
<span data-ttu-id="ab3ac-115">指定群集的名稱</span><span class="sxs-lookup"><span data-stu-id="ab3ac-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="ab3ac-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="ab3ac-116">-NodeType</span></span>
<span data-ttu-id="ab3ac-117">節點類型名稱</span><span class="sxs-lookup"><span data-stu-id="ab3ac-117">Node type name</span></span>

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

### <span data-ttu-id="ab3ac-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="ab3ac-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="ab3ac-119">要新增的節點數</span><span class="sxs-lookup"><span data-stu-id="ab3ac-119">The number of nodes to add</span></span>

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

### <span data-ttu-id="ab3ac-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab3ac-120">-ResourceGroupName</span></span>
<span data-ttu-id="ab3ac-121">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ab3ac-121">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ab3ac-122">-確認</span><span class="sxs-lookup"><span data-stu-id="ab3ac-122">-Confirm</span></span>
<span data-ttu-id="ab3ac-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ab3ac-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab3ac-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab3ac-124">-WhatIf</span></span>
<span data-ttu-id="ab3ac-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ab3ac-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab3ac-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ab3ac-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab3ac-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab3ac-127">CommonParameters</span></span>
<span data-ttu-id="ab3ac-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ab3ac-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab3ac-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ab3ac-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab3ac-130">輸入</span><span class="sxs-lookup"><span data-stu-id="ab3ac-130">INPUTS</span></span>

### <span data-ttu-id="ab3ac-131">System.object</span><span class="sxs-lookup"><span data-stu-id="ab3ac-131">System.Int32</span></span>

### <span data-ttu-id="ab3ac-132">System.object</span><span class="sxs-lookup"><span data-stu-id="ab3ac-132">System.String</span></span>

## <span data-ttu-id="ab3ac-133">輸出</span><span class="sxs-lookup"><span data-stu-id="ab3ac-133">OUTPUTS</span></span>

### <span data-ttu-id="ab3ac-134">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="ab3ac-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="ab3ac-135">筆記</span><span class="sxs-lookup"><span data-stu-id="ab3ac-135">NOTES</span></span>

## <span data-ttu-id="ab3ac-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="ab3ac-136">RELATED LINKS</span></span>

[<span data-ttu-id="ab3ac-137">附加 AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="ab3ac-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md)
