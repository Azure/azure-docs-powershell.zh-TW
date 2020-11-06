---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricdurability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricDurability.md
ms.openlocfilehash: 9c82f0aab38fb5479f5344166a409b9b32f7447c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452043"
---
# <span data-ttu-id="3e931-101">Update-AzureRmServiceFabricDurability</span><span class="sxs-lookup"><span data-stu-id="3e931-101">Update-AzureRmServiceFabricDurability</span></span>

## <span data-ttu-id="3e931-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3e931-102">SYNOPSIS</span></span>
<span data-ttu-id="3e931-103">更新群集中節點類型的持久性層或 VmSku。</span><span class="sxs-lookup"><span data-stu-id="3e931-103">Update the durability tier or VmSku of a node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e931-104">句法</span><span class="sxs-lookup"><span data-stu-id="3e931-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricDurability [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -DurabilityLevel <DurabilityLevel> [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e931-105">說明</span><span class="sxs-lookup"><span data-stu-id="3e931-105">DESCRIPTION</span></span>
<span data-ttu-id="3e931-106">使用 **AzureRmServiceFabricDurability** 更新群集的持續性或 SKU。</span><span class="sxs-lookup"><span data-stu-id="3e931-106">Use **Update-AzureRmServiceFabricDurability** to update durability or SKU of the cluster.</span></span>

## <span data-ttu-id="3e931-107">示例</span><span class="sxs-lookup"><span data-stu-id="3e931-107">EXAMPLES</span></span>

### <span data-ttu-id="3e931-108">範例1</span><span class="sxs-lookup"><span data-stu-id="3e931-108">Example 1</span></span>
```
PS c:> Update-AzureRmServiceFabricDurability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -DurabilityLevel Silver -NodeType nt1
```

<span data-ttu-id="3e931-109">這個命令會將 NodeType "nt1" 的持久性層變更為銀色。</span><span class="sxs-lookup"><span data-stu-id="3e931-109">This command changes durability tier of the NodeType 'nt1' to silver.</span></span>

## <span data-ttu-id="3e931-110">參數</span><span class="sxs-lookup"><span data-stu-id="3e931-110">PARAMETERS</span></span>

### <span data-ttu-id="3e931-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e931-111">-DefaultProfile</span></span>
<span data-ttu-id="3e931-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e931-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e931-113">-DurabilityLevel</span><span class="sxs-lookup"><span data-stu-id="3e931-113">-DurabilityLevel</span></span>
<span data-ttu-id="3e931-114">指定持續性等級。</span><span class="sxs-lookup"><span data-stu-id="3e931-114">Specify durability level.</span></span>

```yaml
Type: DurabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: Bronze, Silver, Gold

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e931-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="3e931-115">-Name</span></span>
<span data-ttu-id="3e931-116">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e931-116">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e931-117">-NodeType</span><span class="sxs-lookup"><span data-stu-id="3e931-117">-NodeType</span></span>
<span data-ttu-id="3e931-118">指定服務結構節點類型名稱。</span><span class="sxs-lookup"><span data-stu-id="3e931-118">Specify Service Fabric node type name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e931-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e931-119">-ResourceGroupName</span></span>
<span data-ttu-id="3e931-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e931-120">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e931-121">-Sku</span><span class="sxs-lookup"><span data-stu-id="3e931-121">-Sku</span></span>
<span data-ttu-id="3e931-122">指定節點類型的 SKU。</span><span class="sxs-lookup"><span data-stu-id="3e931-122">Specify the SKU of the node type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e931-123">-確認</span><span class="sxs-lookup"><span data-stu-id="3e931-123">-Confirm</span></span>
<span data-ttu-id="3e931-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3e931-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e931-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e931-125">-WhatIf</span></span>
<span data-ttu-id="3e931-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3e931-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e931-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3e931-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e931-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e931-128">CommonParameters</span></span>
<span data-ttu-id="3e931-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3e931-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e931-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3e931-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e931-131">輸入</span><span class="sxs-lookup"><span data-stu-id="3e931-131">INPUTS</span></span>

### <span data-ttu-id="3e931-132">DurabilityLevel 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="3e931-132">Microsoft.Azure.Commands.ServiceFabric.Models.DurabilityLevel</span></span>
<span data-ttu-id="3e931-133">System.object</span><span class="sxs-lookup"><span data-stu-id="3e931-133">System.String</span></span>

## <span data-ttu-id="3e931-134">輸出</span><span class="sxs-lookup"><span data-stu-id="3e931-134">OUTPUTS</span></span>

### <span data-ttu-id="3e931-135">PsCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="3e931-135">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="3e931-136">筆記</span><span class="sxs-lookup"><span data-stu-id="3e931-136">NOTES</span></span>

## <span data-ttu-id="3e931-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e931-137">RELATED LINKS</span></span>

