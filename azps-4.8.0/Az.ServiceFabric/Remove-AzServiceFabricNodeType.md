---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: 172a0a2eae2b50c99b3540b654b9490cc8ac6e51
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127320"
---
# <span data-ttu-id="17f31-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="17f31-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="17f31-102">摘要</span><span class="sxs-lookup"><span data-stu-id="17f31-102">SYNOPSIS</span></span>
<span data-ttu-id="17f31-103">從群集中移除完整的節點類型。</span><span class="sxs-lookup"><span data-stu-id="17f31-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="17f31-104">句法</span><span class="sxs-lookup"><span data-stu-id="17f31-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17f31-105">說明</span><span class="sxs-lookup"><span data-stu-id="17f31-105">DESCRIPTION</span></span>
<span data-ttu-id="17f31-106">使用 [ **移除-AzServiceFabricNodeType** ] 從群集中移除特定節點類型的所有節點及節點類型。</span><span class="sxs-lookup"><span data-stu-id="17f31-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="17f31-107">此命令無法用於刪除主要節點類型。</span><span class="sxs-lookup"><span data-stu-id="17f31-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="17f31-108">示例</span><span class="sxs-lookup"><span data-stu-id="17f31-108">EXAMPLES</span></span>

### <span data-ttu-id="17f31-109">範例1</span><span class="sxs-lookup"><span data-stu-id="17f31-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="17f31-110">這個命令會從群集中移除 NodeType "nt1"。</span><span class="sxs-lookup"><span data-stu-id="17f31-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="17f31-111">參數</span><span class="sxs-lookup"><span data-stu-id="17f31-111">PARAMETERS</span></span>

### <span data-ttu-id="17f31-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17f31-112">-DefaultProfile</span></span>
<span data-ttu-id="17f31-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="17f31-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17f31-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="17f31-114">-Name</span></span>
<span data-ttu-id="17f31-115">指定群集的名稱</span><span class="sxs-lookup"><span data-stu-id="17f31-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="17f31-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="17f31-116">-NodeType</span></span>
<span data-ttu-id="17f31-117">節點類型名稱</span><span class="sxs-lookup"><span data-stu-id="17f31-117">The node type name</span></span>

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

### <span data-ttu-id="17f31-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17f31-118">-ResourceGroupName</span></span>
<span data-ttu-id="17f31-119">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="17f31-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="17f31-120">-確認</span><span class="sxs-lookup"><span data-stu-id="17f31-120">-Confirm</span></span>
<span data-ttu-id="17f31-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="17f31-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17f31-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17f31-122">-WhatIf</span></span>
<span data-ttu-id="17f31-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="17f31-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17f31-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="17f31-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17f31-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17f31-125">CommonParameters</span></span>
<span data-ttu-id="17f31-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="17f31-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17f31-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="17f31-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17f31-128">輸入</span><span class="sxs-lookup"><span data-stu-id="17f31-128">INPUTS</span></span>

### <span data-ttu-id="17f31-129">System.object</span><span class="sxs-lookup"><span data-stu-id="17f31-129">System.String</span></span>

## <span data-ttu-id="17f31-130">輸出</span><span class="sxs-lookup"><span data-stu-id="17f31-130">OUTPUTS</span></span>

### <span data-ttu-id="17f31-131">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="17f31-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="17f31-132">筆記</span><span class="sxs-lookup"><span data-stu-id="17f31-132">NOTES</span></span>

## <span data-ttu-id="17f31-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="17f31-133">RELATED LINKS</span></span>
