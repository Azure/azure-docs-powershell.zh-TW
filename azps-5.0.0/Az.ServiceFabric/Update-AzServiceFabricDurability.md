---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricDurability.md
ms.openlocfilehash: 1a406ad937a545c9b2599966909809c7552ad7db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141051"
---
# <span data-ttu-id="50384-101">Update-AzServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="50384-101">Update-AzServiceFabricDurability</span></span>

## <span data-ttu-id="50384-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50384-102">SYNOPSIS</span></span>
<span data-ttu-id="50384-103">更新群集中節點類型的持久性層或 VmSku。</span><span class="sxs-lookup"><span data-stu-id="50384-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

## <span data-ttu-id="50384-104">句法</span><span class="sxs-lookup"><span data-stu-id="50384-104">SYNTAX</span></span>

```
Update-AzServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50384-105">說明</span><span class="sxs-lookup"><span data-stu-id="50384-105">DESCRIPTION</span></span>
<span data-ttu-id="50384-106">使用 **AzServiceFabricDurability** 更新群集的持續性或 SKU。</span><span class="sxs-lookup"><span data-stu-id="50384-106">Use **Update-AzServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="50384-107">示例</span><span class="sxs-lookup"><span data-stu-id="50384-107">EXAMPLES</span></span>

### <span data-ttu-id="50384-108">範例1</span><span class="sxs-lookup"><span data-stu-id="50384-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="50384-109">這個命令會將 NodeType "nt1" 的持久性層變更為銀色。</span><span class="sxs-lookup"><span data-stu-id="50384-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="50384-110">參數</span><span class="sxs-lookup"><span data-stu-id="50384-110">PARAMETERS</span></span>

### <span data-ttu-id="50384-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50384-111">-DefaultProfile</span></span>
<span data-ttu-id="50384-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="50384-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50384-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="50384-113">-DurabilityLevel</span></span>
<span data-ttu-id="50384-114">指定持續性等級。</span><span class="sxs-lookup"><span data-stu-id="50384-114">Specify durability level.</span></span>

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

### <span data-ttu-id="50384-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="50384-115">-Name</span></span>
<span data-ttu-id="50384-116">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="50384-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="50384-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="50384-117">-NodeType</span></span>
<span data-ttu-id="50384-118">指定服務結構節點類型名稱。</span><span class="sxs-lookup"><span data-stu-id="50384-118">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="50384-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50384-119">-ResourceGroupName</span></span>
<span data-ttu-id="50384-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="50384-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="50384-121">-Sku</span><span class="sxs-lookup"><span data-stu-id="50384-121">-Sku</span></span>
<span data-ttu-id="50384-122">指定節點類型的 SKU。</span><span class="sxs-lookup"><span data-stu-id="50384-122">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="50384-123">-確認</span><span class="sxs-lookup"><span data-stu-id="50384-123">-Confirm</span></span>
<span data-ttu-id="50384-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="50384-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50384-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50384-125">-WhatIf</span></span>
<span data-ttu-id="50384-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="50384-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50384-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50384-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50384-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50384-128">CommonParameters</span></span>
<span data-ttu-id="50384-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50384-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50384-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="50384-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50384-131">輸入</span><span class="sxs-lookup"><span data-stu-id="50384-131">INPUTS</span></span>

### <span data-ttu-id="50384-132">System.object</span><span class="sxs-lookup"><span data-stu-id="50384-132">System.String</span></span>

### <span data-ttu-id="50384-133">DurabilityLevel 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="50384-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>

## <span data-ttu-id="50384-134">輸出</span><span class="sxs-lookup"><span data-stu-id="50384-134">OUTPUTS</span></span>

### <span data-ttu-id="50384-135">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="50384-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="50384-136">筆記</span><span class="sxs-lookup"><span data-stu-id="50384-136">NOTES</span></span>

## <span data-ttu-id="50384-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="50384-137">RELATED LINKS</span></span>
