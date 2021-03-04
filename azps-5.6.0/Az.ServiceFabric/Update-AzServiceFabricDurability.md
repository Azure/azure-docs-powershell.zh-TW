---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 40ac27339faf2915ccc88c3bbd5f0a39581af743
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902809"
---
# <span data-ttu-id="c6fad-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="c6fad-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="c6fad-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c6fad-102">SYNOPSIS</span></span>
<span data-ttu-id="c6fad-103">更新該組集中節點類型的節點層級或 VmSKU。</span><span class="sxs-lookup"><span data-stu-id="c6fad-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="c6fad-104">語法</span><span class="sxs-lookup"><span data-stu-id="c6fad-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6fad-105">描述</span><span class="sxs-lookup"><span data-stu-id="c6fad-105">DESCRIPTION</span></span>
<span data-ttu-id="c6fad-106">使用 **Update-AzServiceFabricDurability** 來更新組群的部署或 SKU。</span><span class="sxs-lookup"><span data-stu-id="c6fad-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="c6fad-107">例子</span><span class="sxs-lookup"><span data-stu-id="c6fad-107">EXAMPLES</span></span>

### <span data-ttu-id="c6fad-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="c6fad-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="c6fad-109">此命令將 NodeType 'nt1' 的層級變更為銀牌。</span><span class="sxs-lookup"><span data-stu-id="c6fad-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="c6fad-110">參數</span><span class="sxs-lookup"><span data-stu-id="c6fad-110">PARAMETERS</span></span>

### <span data-ttu-id="c6fad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6fad-111">-DefaultProfile</span></span>
<span data-ttu-id="c6fad-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6fad-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6fad-113">-LevelyLevel</span><span class="sxs-lookup"><span data-stu-id="c6fad-113">-DurabilityLevel</span></span>
<span data-ttu-id="c6fad-114">指定高度。</span><span class="sxs-lookup"><span data-stu-id="c6fad-114">Specify durability level.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: Bronze, Silver, Gold

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6fad-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6fad-115">-Name</span></span>
<span data-ttu-id="c6fad-116">指定組名。</span><span class="sxs-lookup"><span data-stu-id="c6fad-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c6fad-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="c6fad-117">-NodeType</span></span>
<span data-ttu-id="c6fad-118">指定服務結構節點類型名稱。</span><span class="sxs-lookup"><span data-stu-id="c6fad-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="c6fad-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6fad-119">-ResourceGroupName</span></span>
<span data-ttu-id="c6fad-120">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6fad-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c6fad-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="c6fad-121">-Sku</span></span>
<span data-ttu-id="c6fad-122">指定節點類型的 SKU。</span><span class="sxs-lookup"><span data-stu-id="c6fad-122">Specify the SKU of the node type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6fad-123">-確認</span><span class="sxs-lookup"><span data-stu-id="c6fad-123">-Confirm</span></span>
<span data-ttu-id="c6fad-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c6fad-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6fad-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6fad-125">-WhatIf</span></span>
<span data-ttu-id="c6fad-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6fad-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6fad-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6fad-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6fad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6fad-128">CommonParameters</span></span>
<span data-ttu-id="c6fad-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c6fad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6fad-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6fad-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6fad-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c6fad-131">INPUTS</span></span>

### <span data-ttu-id="c6fad-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c6fad-132">System.String</span></span>

### <span data-ttu-id="c6fad-133">Microsoft.Azure.Commands.ServiceFabric.models.LevelyLevel</span><span class="sxs-lookup"><span data-stu-id="c6fad-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="c6fad-134">輸出</span><span class="sxs-lookup"><span data-stu-id="c6fad-134">OUTPUTS</span></span>

### <span data-ttu-id="c6fad-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="c6fad-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="c6fad-136">筆記</span><span class="sxs-lookup"><span data-stu-id="c6fad-136">NOTES</span></span>

## <span data-ttu-id="c6fad-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6fad-137">RELATED LINKS</span></span>
