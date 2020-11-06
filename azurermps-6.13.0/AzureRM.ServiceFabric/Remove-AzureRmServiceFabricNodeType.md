---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricnodetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNodeType.md
ms.openlocfilehash: 36cad62f67be4273d363277e52f4dc8d2c91373c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454548"
---
# <span data-ttu-id="55fc2-101">Remove-AzureRmServiceFabricNodeType</span><span class="sxs-lookup"><span data-stu-id="55fc2-101">Remove-AzureRmServiceFabricNodeType</span></span>

## <span data-ttu-id="55fc2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="55fc2-102">SYNOPSIS</span></span>
<span data-ttu-id="55fc2-103">從群集中移除完整的節點類型。</span><span class="sxs-lookup"><span data-stu-id="55fc2-103">Remove a complete node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55fc2-104">句法</span><span class="sxs-lookup"><span data-stu-id="55fc2-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNodeType [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55fc2-105">說明</span><span class="sxs-lookup"><span data-stu-id="55fc2-105">DESCRIPTION</span></span>
<span data-ttu-id="55fc2-106">使用 [ **移除-AzureRmServiceFabricNodeType** ] 從群集中移除特定節點類型的所有節點及節點類型。</span><span class="sxs-lookup"><span data-stu-id="55fc2-106">Use the **Remove-AzureRmServiceFabricNodeType** to remove all nodes from a specific node type and the node type from a cluster.</span></span> <span data-ttu-id="55fc2-107">此命令無法用於刪除主要節點類型。</span><span class="sxs-lookup"><span data-stu-id="55fc2-107">This command cannot be used to delete the primary node type.</span></span>

## <span data-ttu-id="55fc2-108">示例</span><span class="sxs-lookup"><span data-stu-id="55fc2-108">EXAMPLES</span></span>

### <span data-ttu-id="55fc2-109">範例1</span><span class="sxs-lookup"><span data-stu-id="55fc2-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNodeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1'
```

<span data-ttu-id="55fc2-110">這個命令會從群集中移除 NodeType "nt1"。</span><span class="sxs-lookup"><span data-stu-id="55fc2-110">This command will remove NodeType 'nt1' from the cluster.</span></span>

## <span data-ttu-id="55fc2-111">參數</span><span class="sxs-lookup"><span data-stu-id="55fc2-111">PARAMETERS</span></span>

### <span data-ttu-id="55fc2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55fc2-112">-DefaultProfile</span></span>
<span data-ttu-id="55fc2-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="55fc2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55fc2-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="55fc2-114">-Name</span></span>
<span data-ttu-id="55fc2-115">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="55fc2-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="55fc2-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="55fc2-116">-NodeType</span></span>
<span data-ttu-id="55fc2-117">節點類型名稱。</span><span class="sxs-lookup"><span data-stu-id="55fc2-117">The node type name.</span></span>

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

### <span data-ttu-id="55fc2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55fc2-118">-ResourceGroupName</span></span>
<span data-ttu-id="55fc2-119">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="55fc2-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="55fc2-120">-確認</span><span class="sxs-lookup"><span data-stu-id="55fc2-120">-Confirm</span></span>
<span data-ttu-id="55fc2-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="55fc2-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55fc2-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55fc2-122">-WhatIf</span></span>
<span data-ttu-id="55fc2-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="55fc2-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55fc2-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55fc2-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55fc2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55fc2-125">CommonParameters</span></span>
<span data-ttu-id="55fc2-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="55fc2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55fc2-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="55fc2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55fc2-128">輸入</span><span class="sxs-lookup"><span data-stu-id="55fc2-128">INPUTS</span></span>

### <span data-ttu-id="55fc2-129">System.object</span><span class="sxs-lookup"><span data-stu-id="55fc2-129">System.String</span></span>
<span data-ttu-id="55fc2-130">參數： NodeType (ByValue) </span><span class="sxs-lookup"><span data-stu-id="55fc2-130">Parameters: NodeType (ByValue)</span></span>

## <span data-ttu-id="55fc2-131">輸出</span><span class="sxs-lookup"><span data-stu-id="55fc2-131">OUTPUTS</span></span>

### <span data-ttu-id="55fc2-132">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="55fc2-132">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="55fc2-133">筆記</span><span class="sxs-lookup"><span data-stu-id="55fc2-133">NOTES</span></span>

## <span data-ttu-id="55fc2-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="55fc2-134">RELATED LINKS</span></span>
