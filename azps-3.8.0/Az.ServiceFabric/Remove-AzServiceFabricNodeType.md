---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricNodeType.md
ms.openlocfilehash: bc21812003ca7e71b9f7fa726aea766e924d2519
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957613"
---
# <span data-ttu-id="63ecf-101">Remove-AzServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="63ecf-101">Remove-AzServiceFabricNodeType</span></span>

## <span data-ttu-id="63ecf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="63ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="63ecf-103">從群集中移除完整的節點類型。</span><span class="sxs-lookup"><span data-stu-id="63ecf-103">Remove a complete node type from a cluster.</span></span>

## <span data-ttu-id="63ecf-104">句法</span><span class="sxs-lookup"><span data-stu-id="63ecf-104">SYNTAX</span></span>

```
Remove-AzServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63ecf-105">說明</span><span class="sxs-lookup"><span data-stu-id="63ecf-105">DESCRIPTION</span></span>
<span data-ttu-id="63ecf-106">使用 [ **移除-AzServiceFabricNodeType** ] 從群集中移除特定節點類型的所有節點及節點類型。</span><span class="sxs-lookup"><span data-stu-id="63ecf-106">Use the **Remove-AzServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="63ecf-107">此命令無法用於刪除主要節點類型。</span><span class="sxs-lookup"><span data-stu-id="63ecf-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="63ecf-108">示例</span><span class="sxs-lookup"><span data-stu-id="63ecf-108">EXAMPLES</span></span>

### <span data-ttu-id="63ecf-109">範例1</span><span class="sxs-lookup"><span data-stu-id="63ecf-109">Example 1</span></span>
```powershell
PS c:> Remove-AzServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="63ecf-110">這個命令會從群集中移除 NodeType "nt1"。</span><span class="sxs-lookup"><span data-stu-id="63ecf-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="63ecf-111">參數</span><span class="sxs-lookup"><span data-stu-id="63ecf-111">PARAMETERS</span></span>

### <span data-ttu-id="63ecf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63ecf-112">-DefaultProfile</span></span>
<span data-ttu-id="63ecf-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="63ecf-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63ecf-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="63ecf-114">-Name</span></span>
<span data-ttu-id="63ecf-115">指定群集的名稱</span><span class="sxs-lookup"><span data-stu-id="63ecf-115">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="63ecf-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="63ecf-116">-NodeType</span></span>
<span data-ttu-id="63ecf-117">節點類型名稱</span><span class="sxs-lookup"><span data-stu-id="63ecf-117">The node type name</span></span>

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

### <span data-ttu-id="63ecf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63ecf-118">-ResourceGroupName</span></span>
<span data-ttu-id="63ecf-119">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="63ecf-119">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="63ecf-120">-確認</span><span class="sxs-lookup"><span data-stu-id="63ecf-120">-Confirm</span></span>
<span data-ttu-id="63ecf-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="63ecf-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63ecf-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63ecf-122">-WhatIf</span></span>
<span data-ttu-id="63ecf-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="63ecf-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63ecf-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="63ecf-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63ecf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63ecf-125">CommonParameters</span></span>
<span data-ttu-id="63ecf-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="63ecf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63ecf-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="63ecf-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63ecf-128">輸入</span><span class="sxs-lookup"><span data-stu-id="63ecf-128">INPUTS</span></span>

### <span data-ttu-id="63ecf-129">System.object</span><span class="sxs-lookup"><span data-stu-id="63ecf-129">System.String</span></span>

## <span data-ttu-id="63ecf-130">輸出</span><span class="sxs-lookup"><span data-stu-id="63ecf-130">OUTPUTS</span></span>

### <span data-ttu-id="63ecf-131">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="63ecf-131">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="63ecf-132">筆記</span><span class="sxs-lookup"><span data-stu-id="63ecf-132">NOTES</span></span>

## <span data-ttu-id="63ecf-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="63ecf-133">RELATED LINKS</span></span>
