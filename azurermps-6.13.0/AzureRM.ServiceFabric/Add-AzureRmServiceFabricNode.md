---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/add-azurermservicefabricnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Add-AzureRmServiceFabricNode.md
ms.openlocfilehash: 687be1ddd20c431e5226fe7f0516cc480e79fce8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623890"
---
# <span data-ttu-id="2ee9e-101">Add-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2ee9e-101">Add-AzureRmServiceFabricNode</span></span>

## <span data-ttu-id="2ee9e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2ee9e-102">SYNOPSIS</span></span>
<span data-ttu-id="2ee9e-103">新增節點至群集中的特定節點類型。</span><span class="sxs-lookup"><span data-stu-id="2ee9e-103">Add nodes to the specific node type in the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ee9e-104">句法</span><span class="sxs-lookup"><span data-stu-id="2ee9e-104">SYNTAX</span></span>

```
Add-AzureRmServiceFabricNode -NumberOfNodesToAdd <Int32> [-ResourceGroupName] <String> [-Name] <String>
 -NodeType <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ee9e-105">說明</span><span class="sxs-lookup"><span data-stu-id="2ee9e-105">DESCRIPTION</span></span>
<span data-ttu-id="2ee9e-106">使用 [ **載入 AzureRmServiceFabricNode** ]，將節點新增至特定的節點類型。</span><span class="sxs-lookup"><span data-stu-id="2ee9e-106">Use **Add-AzureRmServiceFabricNode** to add nodes to the specific node type.</span></span> <span data-ttu-id="2ee9e-107">您只需指定要新增至節點類型的節點數。</span><span class="sxs-lookup"><span data-stu-id="2ee9e-107">You just need to specify the number of nodes you want to add to a node type.</span></span>

## <span data-ttu-id="2ee9e-108">示例</span><span class="sxs-lookup"><span data-stu-id="2ee9e-108">EXAMPLES</span></span>

### <span data-ttu-id="2ee9e-109">範例1</span><span class="sxs-lookup"><span data-stu-id="2ee9e-109">Example 1</span></span>
```
PS c:> Add-AzureRmServiceFabricNode -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -NumberOfNodesToAdd 2 -NodeTypeName 'nt1'
```

<span data-ttu-id="2ee9e-110">這個命令會將2個節點新增至節點類型 ' n1」。</span><span class="sxs-lookup"><span data-stu-id="2ee9e-110">This command will add 2 nodes to the node type 'n1'.</span></span>

## <span data-ttu-id="2ee9e-111">參數</span><span class="sxs-lookup"><span data-stu-id="2ee9e-111">PARAMETERS</span></span>

### <span data-ttu-id="2ee9e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ee9e-112">-DefaultProfile</span></span>
<span data-ttu-id="2ee9e-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2ee9e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ee9e-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="2ee9e-114">-Name</span></span>
<span data-ttu-id="2ee9e-115">指定群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ee9e-115">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="2ee9e-116">-NodeType</span><span class="sxs-lookup"><span data-stu-id="2ee9e-116">-NodeType</span></span>
<span data-ttu-id="2ee9e-117">節點類型名稱。</span><span class="sxs-lookup"><span data-stu-id="2ee9e-117">Node type name.</span></span>

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

### <span data-ttu-id="2ee9e-118">-NumberOfNodesToAdd</span><span class="sxs-lookup"><span data-stu-id="2ee9e-118">-NumberOfNodesToAdd</span></span>
<span data-ttu-id="2ee9e-119">VM 實例編號。</span><span class="sxs-lookup"><span data-stu-id="2ee9e-119">VM instance number.</span></span>

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

### <span data-ttu-id="2ee9e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ee9e-120">-ResourceGroupName</span></span>
<span data-ttu-id="2ee9e-121">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2ee9e-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2ee9e-122">-確認</span><span class="sxs-lookup"><span data-stu-id="2ee9e-122">-Confirm</span></span>
<span data-ttu-id="2ee9e-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2ee9e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ee9e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ee9e-124">-WhatIf</span></span>
<span data-ttu-id="2ee9e-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2ee9e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ee9e-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2ee9e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ee9e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ee9e-127">CommonParameters</span></span>
<span data-ttu-id="2ee9e-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2ee9e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ee9e-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2ee9e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ee9e-130">輸入</span><span class="sxs-lookup"><span data-stu-id="2ee9e-130">INPUTS</span></span>

### <span data-ttu-id="2ee9e-131">System.object</span><span class="sxs-lookup"><span data-stu-id="2ee9e-131">System.Int32</span></span>
<span data-ttu-id="2ee9e-132">參數： NumberOfNodesToAdd (ByValue) </span><span class="sxs-lookup"><span data-stu-id="2ee9e-132">Parameters: NumberOfNodesToAdd (ByValue)</span></span>

### <span data-ttu-id="2ee9e-133">System.object</span><span class="sxs-lookup"><span data-stu-id="2ee9e-133">System.String</span></span>
<span data-ttu-id="2ee9e-134">參數： NodeType (ByValue) </span><span class="sxs-lookup"><span data-stu-id="2ee9e-134">Parameters: NodeType (ByValue)</span></span>

## <span data-ttu-id="2ee9e-135">輸出</span><span class="sxs-lookup"><span data-stu-id="2ee9e-135">OUTPUTS</span></span>

### <span data-ttu-id="2ee9e-136">PSCluster 中的 ServiceFabric。</span><span class="sxs-lookup"><span data-stu-id="2ee9e-136">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="2ee9e-137">筆記</span><span class="sxs-lookup"><span data-stu-id="2ee9e-137">NOTES</span></span>

## <span data-ttu-id="2ee9e-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="2ee9e-138">RELATED LINKS</span></span>

[<span data-ttu-id="2ee9e-139">移除-AzureRmServiceFabricNode</span><span class="sxs-lookup"><span data-stu-id="2ee9e-139">Remove-AzureRmServiceFabricNode</span></span>](./Remove-AzureRmServiceFabricNode.md)
