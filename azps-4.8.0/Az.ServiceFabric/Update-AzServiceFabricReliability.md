---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/update-azservicefabricreliability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Update-AzServiceFabricReliability.md
ms.openlocfilehash: a63bcfe0f807f36ffae5c10e644322b1fb612325
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129238"
---
# <span data-ttu-id="4e6b8-101">Update-AzServiceFabricReliability</span><span class="sxs-lookup"><span data-stu-id="4e6b8-101">Update-AzServiceFabricReliability</span></span>

## <span data-ttu-id="4e6b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e6b8-102">SYNOPSIS</span></span>
<span data-ttu-id="4e6b8-103">在群集中更新主要節點類型的可靠性層級。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-103">Update the reliability tier of the primary node type in a cluster.</span></span>

## <span data-ttu-id="4e6b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e6b8-104">SYNTAX</span></span>

```
Update-AzServiceFabricReliability [-ResourceGroupName] <String> [-Name] <String>
 -ReliabilityLevel <ReliabilityLevel> [-AutoAddNode] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e6b8-105">說明</span><span class="sxs-lookup"><span data-stu-id="4e6b8-105">DESCRIPTION</span></span>
<span data-ttu-id="4e6b8-106">在群集中使用 **更新-AzServiceFabricReliability** 更新主要節點類型的可靠性。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-106">Use **Update-AzServiceFabricReliability** to update reliability of the primary node type in a cluster.</span></span>

## <span data-ttu-id="4e6b8-107">示例</span><span class="sxs-lookup"><span data-stu-id="4e6b8-107">EXAMPLES</span></span>

### <span data-ttu-id="4e6b8-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4e6b8-108">Example 1</span></span>
```
PS c:> Update-AzServiceFabricReliability -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -ReliabilityLevel Silver
```

<span data-ttu-id="4e6b8-109">這個命令會將主要節點類型的可靠性層級變更為銀色。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-109">This command changes the reliability tier of the primary node type to silver.</span></span>

## <span data-ttu-id="4e6b8-110">參數</span><span class="sxs-lookup"><span data-stu-id="4e6b8-110">PARAMETERS</span></span>

### <span data-ttu-id="4e6b8-111">-AutoAddNode</span><span class="sxs-lookup"><span data-stu-id="4e6b8-111">-AutoAddNode</span></span>
<span data-ttu-id="4e6b8-112">在變更可靠性時自動新增節點計數</span><span class="sxs-lookup"><span data-stu-id="4e6b8-112">Add node count automatically when changing reliability</span></span>

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

### <span data-ttu-id="4e6b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e6b8-113">-DefaultProfile</span></span>
<span data-ttu-id="4e6b8-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e6b8-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e6b8-115">-Name</span></span>
<span data-ttu-id="4e6b8-116">指定群集的名稱</span><span class="sxs-lookup"><span data-stu-id="4e6b8-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="4e6b8-117">-ReliabilityLevel</span><span class="sxs-lookup"><span data-stu-id="4e6b8-117">-ReliabilityLevel</span></span>
<span data-ttu-id="4e6b8-118">可靠性層級</span><span class="sxs-lookup"><span data-stu-id="4e6b8-118">Reliability tier</span></span>

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

### <span data-ttu-id="4e6b8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e6b8-119">-ResourceGroupName</span></span>
<span data-ttu-id="4e6b8-120">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-120">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="4e6b8-121">-確認</span><span class="sxs-lookup"><span data-stu-id="4e6b8-121">-Confirm</span></span>
<span data-ttu-id="4e6b8-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e6b8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e6b8-123">-WhatIf</span></span>
<span data-ttu-id="4e6b8-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e6b8-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e6b8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e6b8-126">CommonParameters</span></span>
<span data-ttu-id="4e6b8-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e6b8-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e6b8-129">輸入</span><span class="sxs-lookup"><span data-stu-id="4e6b8-129">INPUTS</span></span>

### <span data-ttu-id="4e6b8-130">System.object</span><span class="sxs-lookup"><span data-stu-id="4e6b8-130">System.String</span></span>

### <span data-ttu-id="4e6b8-131">ReliabilityLevel 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-131">Microsoft.Azure.Commands.ServiceFabric.Models.ReliabilityLevel</span></span>

### <span data-ttu-id="4e6b8-132">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="4e6b8-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4e6b8-133">輸出</span><span class="sxs-lookup"><span data-stu-id="4e6b8-133">OUTPUTS</span></span>

### <span data-ttu-id="4e6b8-134">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="4e6b8-134">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="4e6b8-135">筆記</span><span class="sxs-lookup"><span data-stu-id="4e6b8-135">NOTES</span></span>

## <span data-ttu-id="4e6b8-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e6b8-136">RELATED LINKS</span></span>
