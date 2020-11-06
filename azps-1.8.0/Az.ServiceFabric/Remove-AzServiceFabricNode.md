---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNode.md
ms.openlocfilehash: 22aa963f772a87b97a0a64ccdaef5ad6ef004696
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620556"
---
# <span data-ttu-id="6ca38-101">Remove-AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="6ca38-101">Remove-AzServiceFabricNode</span></span>

## <span data-ttu-id="6ca38-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ca38-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca38-103">從群集中移除特定節點類型的節點。</span><span class="sxs-lookup"><span data-stu-id="6ca38-103">Remove nodes from the specific node type from a cluster.</span></span>

## <span data-ttu-id="6ca38-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ca38-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNode -NumberOfNodesToRemove <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ca38-105">說明</span><span class="sxs-lookup"><span data-stu-id="6ca38-105">DESCRIPTION</span></span>
<span data-ttu-id="6ca38-106">使用 [ **移除-AzServiceFabricNode** ] 從群集中移除特定節點類型的節點。</span><span class="sxs-lookup"><span data-stu-id="6ca38-106">Use **Remove-AzServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="6ca38-107">移除只會在符合群集健康情況指標時進行。</span><span class="sxs-lookup"><span data-stu-id="6ca38-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="6ca38-108">示例</span><span class="sxs-lookup"><span data-stu-id="6ca38-108">EXAMPLES</span></span>

### <span data-ttu-id="6ca38-109">範例1</span><span class="sxs-lookup"><span data-stu-id="6ca38-109">Example 1</span></span>
```
PS c:> Remove-AzServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="6ca38-110">這個命令會從 NodeType "nt1" 移除2個節點。</span><span class="sxs-lookup"><span data-stu-id="6ca38-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="6ca38-111">參數</span><span class="sxs-lookup"><span data-stu-id="6ca38-111">PARAMETERS</span></span>

### <span data-ttu-id="6ca38-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca38-112">-DefaultProfile</span></span>
<span data-ttu-id="6ca38-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ca38-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ca38-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="6ca38-114">-Name</span></span>
<span data-ttu-id="6ca38-115">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ca38-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="6ca38-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="6ca38-116">-NodeType</span></span>
<span data-ttu-id="6ca38-117">節點類型名稱。</span><span class="sxs-lookup"><span data-stu-id="6ca38-117">Node type name.</span></span>

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

### <span data-ttu-id="6ca38-118">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="6ca38-118">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="6ca38-119">要移除的節點數。</span><span class="sxs-lookup"><span data-stu-id="6ca38-119">Number of nodes to remove.</span></span>

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

### <span data-ttu-id="6ca38-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ca38-120">-ResourceGroupName</span></span>
<span data-ttu-id="6ca38-121">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ca38-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6ca38-122">-確認</span><span class="sxs-lookup"><span data-stu-id="6ca38-122">-Confirm</span></span>
<span data-ttu-id="6ca38-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6ca38-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ca38-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ca38-124">-WhatIf</span></span>
<span data-ttu-id="6ca38-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6ca38-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ca38-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6ca38-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ca38-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca38-127">CommonParameters</span></span>
<span data-ttu-id="6ca38-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ca38-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca38-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ca38-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca38-130">輸入</span><span class="sxs-lookup"><span data-stu-id="6ca38-130">INPUTS</span></span>

### <span data-ttu-id="6ca38-131">System.object</span><span class="sxs-lookup"><span data-stu-id="6ca38-131">System.Int32</span></span>

### <span data-ttu-id="6ca38-132">System.object</span><span class="sxs-lookup"><span data-stu-id="6ca38-132">System.String</span></span>

## <span data-ttu-id="6ca38-133">輸出</span><span class="sxs-lookup"><span data-stu-id="6ca38-133">OUTPUTS</span></span>

### <span data-ttu-id="6ca38-134">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="6ca38-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="6ca38-135">筆記</span><span class="sxs-lookup"><span data-stu-id="6ca38-135">NOTES</span></span>

## <span data-ttu-id="6ca38-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ca38-136">RELATED LINKS</span></span>

[<span data-ttu-id="6ca38-137">附加 AzServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="6ca38-137">Add-AzServiceFabricNode</span></span>](./Add-AzServiceFabricNode.md) 
