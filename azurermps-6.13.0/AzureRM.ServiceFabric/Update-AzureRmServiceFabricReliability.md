---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/update-azurermservicefabricreliability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Update-AzureRmServiceFabricReliability.md
ms.openlocfilehash: 15dfc29703e2d331920a1751bcd6671e77d84171
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449726"
---
# <span data-ttu-id="12019-101">Update-AzureRmServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="12019-101">Update-AzureRmServiceFabricReliability</span></span>

## <span data-ttu-id="12019-102">摘要</span><span class="sxs-lookup"><span data-stu-id="12019-102">SYNOPSIS</span></span>
<span data-ttu-id="12019-103">在群集中更新主要節點類型的可靠性層級。</span><span class="sxs-lookup"><span data-stu-id="12019-103">Update the reliability tier of the primary node type in a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12019-104">句法</span><span class="sxs-lookup"><span data-stu-id="12019-104">SYNTAX</span></span>

```
Update-AzureRmServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12019-105">說明</span><span class="sxs-lookup"><span data-stu-id="12019-105">DESCRIPTION</span></span>
<span data-ttu-id="12019-106">在群集中使用 **更新-AzureRmServiceFabricReliability** 更新主要節點類型的可靠性。</span><span class="sxs-lookup"><span data-stu-id="12019-106">Use **Update-AzureRmServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="12019-107">示例</span><span class="sxs-lookup"><span data-stu-id="12019-107">EXAMPLES</span></span>

### <span data-ttu-id="12019-108">範例1</span><span class="sxs-lookup"><span data-stu-id="12019-108">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="12019-109">這個命令會將主要節點類型的可靠性層級變更為銀色。</span><span class="sxs-lookup"><span data-stu-id="12019-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="12019-110">參數</span><span class="sxs-lookup"><span data-stu-id="12019-110">PARAMETERS</span></span>

### <span data-ttu-id="12019-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="12019-111">-AutoAddNode</span></span>
<span data-ttu-id="12019-112">在變更可靠性時，會自動新增節點計數。</span><span class="sxs-lookup"><span data-stu-id="12019-112">Add node count automatically when changing reliability.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: Auto

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12019-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12019-113">-DefaultProfile</span></span>
<span data-ttu-id="12019-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="12019-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12019-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="12019-115">-Name</span></span>
<span data-ttu-id="12019-116">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="12019-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="12019-117">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="12019-117">-ReliabilityLevel</span></span>
<span data-ttu-id="12019-118">可靠性層級。</span><span class="sxs-lookup"><span data-stu-id="12019-118">Reliability tier.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel
Parameter Sets: (All)
Aliases: Level
Accepted values: None, Bronze, Silver, Gold, Platinum

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12019-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12019-119">-ResourceGroupName</span></span>
<span data-ttu-id="12019-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="12019-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="12019-121">-確認</span><span class="sxs-lookup"><span data-stu-id="12019-121">-Confirm</span></span>
<span data-ttu-id="12019-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="12019-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12019-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12019-123">-WhatIf</span></span>
<span data-ttu-id="12019-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="12019-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12019-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="12019-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12019-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12019-126">CommonParameters</span></span>
<span data-ttu-id="12019-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="12019-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12019-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="12019-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12019-129">輸入</span><span class="sxs-lookup"><span data-stu-id="12019-129">INPUTS</span></span>

### <span data-ttu-id="12019-130">System.object</span><span class="sxs-lookup"><span data-stu-id="12019-130">System.String</span></span>

### <span data-ttu-id="12019-131">ReliabilityLevel 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="12019-131">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>
<span data-ttu-id="12019-132">參數： ReliabilityLevel (ByValue) </span><span class="sxs-lookup"><span data-stu-id="12019-132">Parameters: ReliabilityLevel (ByValue)</span></span>

### <span data-ttu-id="12019-133">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="12019-133">System.Management.Automation.SwitchParameter</span></span>
<span data-ttu-id="12019-134">參數： AutoAddNode (ByValue) </span><span class="sxs-lookup"><span data-stu-id="12019-134">Parameters: AutoAddNode (ByValue)</span></span>

## <span data-ttu-id="12019-135">輸出</span><span class="sxs-lookup"><span data-stu-id="12019-135">OUTPUTS</span></span>

### <span data-ttu-id="12019-136">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="12019-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="12019-137">筆記</span><span class="sxs-lookup"><span data-stu-id="12019-137">NOTES</span></span>

## <span data-ttu-id="12019-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="12019-138">RELATED LINKS</span></span>
