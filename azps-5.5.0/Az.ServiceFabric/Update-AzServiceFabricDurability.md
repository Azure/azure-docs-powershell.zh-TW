---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 1a0da9869ccfdc6b8344240a8367a4c8dfcd2350
ms.sourcegitcommit: 608289d079b819df2b8d1a2f7935cc500367a312
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "101684891"
---
# <span data-ttu-id="2d7a2-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="2d7a2-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="2d7a2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2d7a2-102">SYNOPSIS</span></span>
<span data-ttu-id="2d7a2-103">更新該組集中節點類型的節點層級或 VmSKU。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-103">Update the durability tier or VmSku of a node type in the cluster.</span></span> <span data-ttu-id="2d7a2-104">它也將會更新相關聯虛擬機器縮放集上的 Service Fabric VM 擴充功能層級。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-104">It will also update the durability tier in the Service Fabric VM extension on the associated Virtual Machine Scale Set.</span></span>

## <span data-ttu-id="2d7a2-105">語法</span><span class="sxs-lookup"><span data-stu-id="2d7a2-105">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d7a2-106">描述</span><span class="sxs-lookup"><span data-stu-id="2d7a2-106">DESCRIPTION</span></span>
<span data-ttu-id="2d7a2-107">使用 **Update-AzServiceFabricDurability** 來更新組群的部署或 SKU。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-107">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="2d7a2-108">例子</span><span class="sxs-lookup"><span data-stu-id="2d7a2-108">EXAMPLES</span></span>

### <span data-ttu-id="2d7a2-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="2d7a2-109">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="2d7a2-110">此命令將 NodeType 'nt1' 的層級變更為銀牌。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-110">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="2d7a2-111">參數</span><span class="sxs-lookup"><span data-stu-id="2d7a2-111">PARAMETERS</span></span>

### <span data-ttu-id="2d7a2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d7a2-112">-DefaultProfile</span></span>
<span data-ttu-id="2d7a2-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d7a2-114">-LevelyLevel</span><span class="sxs-lookup"><span data-stu-id="2d7a2-114">-DurabilityLevel</span></span>
<span data-ttu-id="2d7a2-115">指定高度。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-115">Specify durability level.</span></span>

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

### <span data-ttu-id="2d7a2-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="2d7a2-116">-Name</span></span>
<span data-ttu-id="2d7a2-117">指定組名。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2d7a2-118">-NodeType</span><span class="sxs-lookup"><span data-stu-id="2d7a2-118">-NodeType</span></span>
<span data-ttu-id="2d7a2-119">指定服務結構節點類型名稱。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-119">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="2d7a2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d7a2-120">-ResourceGroupName</span></span>
<span data-ttu-id="2d7a2-121">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2d7a2-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="2d7a2-122">-Sku</span></span>
<span data-ttu-id="2d7a2-123">指定節點類型的 SKU。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-123">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="2d7a2-124">-確認</span><span class="sxs-lookup"><span data-stu-id="2d7a2-124">-Confirm</span></span>
<span data-ttu-id="2d7a2-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d7a2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d7a2-126">-WhatIf</span></span>
<span data-ttu-id="2d7a2-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d7a2-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d7a2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d7a2-129">CommonParameters</span></span>
<span data-ttu-id="2d7a2-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2d7a2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d7a2-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d7a2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d7a2-132">輸入</span><span class="sxs-lookup"><span data-stu-id="2d7a2-132">INPUTS</span></span>

### <span data-ttu-id="2d7a2-133">System.String</span><span class="sxs-lookup"><span data-stu-id="2d7a2-133">System.String</span></span>

### <span data-ttu-id="2d7a2-134">Microsoft.Azure.Commands.ServiceFabric.models.LevelyLevel</span><span class="sxs-lookup"><span data-stu-id="2d7a2-134">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="2d7a2-135">輸出</span><span class="sxs-lookup"><span data-stu-id="2d7a2-135">OUTPUTS</span></span>

### <span data-ttu-id="2d7a2-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="2d7a2-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="2d7a2-137">筆記</span><span class="sxs-lookup"><span data-stu-id="2d7a2-137">NOTES</span></span>

## <span data-ttu-id="2d7a2-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="2d7a2-138">RELATED LINKS</span></span>
