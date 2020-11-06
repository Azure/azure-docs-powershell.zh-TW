---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricNode.md
ms.openlocfilehash: cbf23af4c98e8174091b467e6e05ed5de6ae20c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447972"
---
# <span data-ttu-id="645ba-101">Remove-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="645ba-101">Remove-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="645ba-102">摘要</span><span class="sxs-lookup"><span data-stu-id="645ba-102">SYNOPSIS</span></span>
<span data-ttu-id="645ba-103">從群集中移除特定節點類型的節點。</span><span class="sxs-lookup"><span data-stu-id="645ba-103">Remove nodes from the specific node type from a cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="645ba-104">句法</span><span class="sxs-lookup"><span data-stu-id="645ba-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricNode [-ResourceGroupName] <String> [-Name] <String> -NodeType <String>
 -NumberOfNodesToRemove <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="645ba-105">說明</span><span class="sxs-lookup"><span data-stu-id="645ba-105">DESCRIPTION</span></span>
<span data-ttu-id="645ba-106">使用 [ **移除-AzureRmServiceFabricNode** ] 從群集中移除特定節點類型的節點。</span><span class="sxs-lookup"><span data-stu-id="645ba-106">Use **Remove-AzureRmServiceFabricNode** to remove nodes from a specific node type from a cluster.</span></span> <span data-ttu-id="645ba-107">移除只會在符合群集健康情況指標時進行。</span><span class="sxs-lookup"><span data-stu-id="645ba-107">The removal proceeds only if it meets cluster health metrics.</span></span>

## <span data-ttu-id="645ba-108">示例</span><span class="sxs-lookup"><span data-stu-id="645ba-108">EXAMPLES</span></span>

### <span data-ttu-id="645ba-109">範例1</span><span class="sxs-lookup"><span data-stu-id="645ba-109">Example 1</span></span>
```
PS c:> Remove-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NodeTypeName 'nt1' -NumberOfNodesToRemove 2
```

<span data-ttu-id="645ba-110">這個命令會從 NodeType "nt1" 移除2個節點。</span><span class="sxs-lookup"><span data-stu-id="645ba-110">This command will remove 2 nodes from the NodeType 'nt1'.</span></span>

## <span data-ttu-id="645ba-111">參數</span><span class="sxs-lookup"><span data-stu-id="645ba-111">PARAMETERS</span></span>

### <span data-ttu-id="645ba-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="645ba-112">-Name</span></span>
<span data-ttu-id="645ba-113">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="645ba-113">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="645ba-114">-NodeType</span><span class="sxs-lookup"><span data-stu-id="645ba-114">-NodeType</span></span>
<span data-ttu-id="645ba-115">節點類型名稱。</span><span class="sxs-lookup"><span data-stu-id="645ba-115">Node type name.</span></span>

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

### <span data-ttu-id="645ba-116">-NumberOfNodesToRemove</span><span class="sxs-lookup"><span data-stu-id="645ba-116">-NumberOfNodesToRemove</span></span>
<span data-ttu-id="645ba-117">要移除的節點數。</span><span class="sxs-lookup"><span data-stu-id="645ba-117">Number of nodes to remove.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Number

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="645ba-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="645ba-118">-ResourceGroupName</span></span>
<span data-ttu-id="645ba-119">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="645ba-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="645ba-120">-確認</span><span class="sxs-lookup"><span data-stu-id="645ba-120">-Confirm</span></span>
<span data-ttu-id="645ba-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="645ba-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="645ba-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="645ba-122">-WhatIf</span></span>
<span data-ttu-id="645ba-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="645ba-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="645ba-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="645ba-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="645ba-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="645ba-125">-DefaultProfile</span></span>
<span data-ttu-id="645ba-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="645ba-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="645ba-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="645ba-127">CommonParameters</span></span>
<span data-ttu-id="645ba-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="645ba-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="645ba-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="645ba-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="645ba-130">輸入</span><span class="sxs-lookup"><span data-stu-id="645ba-130">INPUTS</span></span>

### <span data-ttu-id="645ba-131">System.object</span><span class="sxs-lookup"><span data-stu-id="645ba-131">System.Int32</span></span>
<span data-ttu-id="645ba-132">System.object</span><span class="sxs-lookup"><span data-stu-id="645ba-132">System.String</span></span>

## <span data-ttu-id="645ba-133">輸出</span><span class="sxs-lookup"><span data-stu-id="645ba-133">OUTPUTS</span></span>

### <span data-ttu-id="645ba-134">System.object</span><span class="sxs-lookup"><span data-stu-id="645ba-134">System.Object</span></span>

## <span data-ttu-id="645ba-135">筆記</span><span class="sxs-lookup"><span data-stu-id="645ba-135">NOTES</span></span>

## <span data-ttu-id="645ba-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="645ba-136">RELATED LINKS</span></span>

[<span data-ttu-id="645ba-137">附加 AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="645ba-137">Add-AzureRmServiceFabricNode</span></span>](./Add-AzureRmServiceFabricNode.md) 
