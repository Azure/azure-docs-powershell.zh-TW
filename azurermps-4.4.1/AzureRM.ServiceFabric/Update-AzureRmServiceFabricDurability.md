---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: b056e5328c24270df6a95e33b079e7b907f29fa3
ms.sourcegitcommit: 608289d079b819df2b8d1a2f7935cc500367a312
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "101685033"
---
# <span data-ttu-id="1ca5c-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="1ca5c-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="1ca5c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1ca5c-102">SYNOPSIS</span></span>
<span data-ttu-id="1ca5c-103">更新該組集中節點類型的節點層級或 VmSKU。</span><span class="sxs-lookup"><span data-stu-id="1ca5c-103">Update the durability tier or VmSku of a node type in the cluster.</span></span> <span data-ttu-id="1ca5c-104">它也將會更新相關聯虛擬機器縮放集上的 Service Fabric VM 擴充功能層級。</span><span class="sxs-lookup"><span data-stu-id="1ca5c-104">It will also update the durability tier in the Service Fabric VM extension on the associated Virtual Machine Scale Set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1ca5c-105">語法</span><span class="sxs-lookup"><span data-stu-id="1ca5c-105">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ca5c-106">描述</span><span class="sxs-lookup"><span data-stu-id="1ca5c-106">DESCRIPTION</span></span>
<span data-ttu-id="1ca5c-107">使用 **Update-AzureRmServiceFabricDurability** 來更新組群的不更新或 SKU。</span><span class="sxs-lookup"><span data-stu-id="1ca5c-107">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="1ca5c-108">例子</span><span class="sxs-lookup"><span data-stu-id="1ca5c-108">EXAMPLES</span></span>

### <span data-ttu-id="1ca5c-109">範例 1</span><span class="sxs-lookup"><span data-stu-id="1ca5c-109">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="1ca5c-110">此命令將 NodeType 'nt1' 的層級變更為銀牌。</span><span class="sxs-lookup"><span data-stu-id="1ca5c-110">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="1ca5c-111">參數</span><span class="sxs-lookup"><span data-stu-id="1ca5c-111">PARAMETERS</span></span>

### <span data-ttu-id="1ca5c-112">-LevelyLevel</span><span class="sxs-lookup"><span data-stu-id="1ca5c-112">-DurabilityLevel</span></span>
<span data-ttu-id="1ca5c-113">指定高度。</span><span class="sxs-lookup"><span data-stu-id="1ca5c-113">Specify durability level.</span></span>

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

### <span data-ttu-id="1ca5c-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="1ca5c-114">-Name</span></span>
<span data-ttu-id="1ca5c-115">指定組名。</span><span class="sxs-lookup"><span data-stu-id="1ca5c-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="1ca5c-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="1ca5c-116">-NodeType</span></span>
<span data-ttu-id="1ca5c-117">指定服務結構節點類型名稱。</span><span class="sxs-lookup"><span data-stu-id="1ca5c-117">Specify Service Fabric node type name.</span></span>

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

### <span data-ttu-id="1ca5c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ca5c-118">-ResourceGroupName</span></span>
<span data-ttu-id="1ca5c-119">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1ca5c-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1ca5c-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="1ca5c-120">-Sku</span></span>
<span data-ttu-id="1ca5c-121">指定節點類型的 SKU。</span><span class="sxs-lookup"><span data-stu-id="1ca5c-121">Specify the SKU of the node type.</span></span>

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

### <span data-ttu-id="1ca5c-122">-確認</span><span class="sxs-lookup"><span data-stu-id="1ca5c-122">-Confirm</span></span>
<span data-ttu-id="1ca5c-123">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1ca5c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ca5c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ca5c-124">-WhatIf</span></span>
<span data-ttu-id="1ca5c-125">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1ca5c-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ca5c-126">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ca5c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ca5c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ca5c-127">-DefaultProfile</span></span>
<span data-ttu-id="1ca5c-128">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ca5c-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ca5c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ca5c-129">CommonParameters</span></span>
<span data-ttu-id="1ca5c-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1ca5c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ca5c-131">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1ca5c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ca5c-132">輸入</span><span class="sxs-lookup"><span data-stu-id="1ca5c-132">INPUTS</span></span>

### <span data-ttu-id="1ca5c-133">Microsoft.Azure.Commands.ServiceFabric.models.LevelyLevel</span><span class="sxs-lookup"><span data-stu-id="1ca5c-133">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="1ca5c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1ca5c-134">System.String</span></span>

## <span data-ttu-id="1ca5c-135">輸出</span><span class="sxs-lookup"><span data-stu-id="1ca5c-135">OUTPUTS</span></span>

### <span data-ttu-id="1ca5c-136">Microsoft.Azure.Commands.ServiceFabric.models.PsCluster</span><span class="sxs-lookup"><span data-stu-id="1ca5c-136">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="1ca5c-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1ca5c-137">NOTES</span></span>

## <span data-ttu-id="1ca5c-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ca5c-138">RELATED LINKS</span></span>

