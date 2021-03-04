---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: b2cb61ff6b80cb6e0325f006d063d7e0a8971a4f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911586"
---
# <span data-ttu-id="4babc-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="4babc-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="4babc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4babc-102">SYNOPSIS</span></span>
<span data-ttu-id="4babc-103">刪除組</span><span class="sxs-lookup"><span data-stu-id="4babc-103">Delete cluster</span></span>

## <span data-ttu-id="4babc-104">語法</span><span class="sxs-lookup"><span data-stu-id="4babc-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4babc-105">描述</span><span class="sxs-lookup"><span data-stu-id="4babc-105">DESCRIPTION</span></span>
<span data-ttu-id="4babc-106">刪除集區，僅適用于布備狀態為「已成功」的集區</span><span class="sxs-lookup"><span data-stu-id="4babc-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="4babc-107">例子</span><span class="sxs-lookup"><span data-stu-id="4babc-107">EXAMPLES</span></span>

### <span data-ttu-id="4babc-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="4babc-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="4babc-109">刪除集區</span><span class="sxs-lookup"><span data-stu-id="4babc-109">Delete cluster</span></span>

## <span data-ttu-id="4babc-110">參數</span><span class="sxs-lookup"><span data-stu-id="4babc-110">PARAMETERS</span></span>

### <span data-ttu-id="4babc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4babc-111">-AsJob</span></span>
<span data-ttu-id="4babc-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4babc-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4babc-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4babc-113">-ClusterName</span></span>
<span data-ttu-id="4babc-114">組名。</span><span class="sxs-lookup"><span data-stu-id="4babc-114">The cluster name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4babc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4babc-115">-DefaultProfile</span></span>
<span data-ttu-id="4babc-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4babc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4babc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4babc-117">-ResourceGroupName</span></span>
<span data-ttu-id="4babc-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="4babc-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4babc-119">-確認</span><span class="sxs-lookup"><span data-stu-id="4babc-119">-Confirm</span></span>
<span data-ttu-id="4babc-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4babc-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4babc-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4babc-121">-WhatIf</span></span>
<span data-ttu-id="4babc-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4babc-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4babc-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4babc-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4babc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4babc-124">CommonParameters</span></span>
<span data-ttu-id="4babc-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4babc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4babc-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4babc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4babc-127">輸入</span><span class="sxs-lookup"><span data-stu-id="4babc-127">INPUTS</span></span>

### <span data-ttu-id="4babc-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4babc-128">System.String</span></span>

## <span data-ttu-id="4babc-129">輸出</span><span class="sxs-lookup"><span data-stu-id="4babc-129">OUTPUTS</span></span>

### <span data-ttu-id="4babc-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4babc-130">System.Boolean</span></span>

## <span data-ttu-id="4babc-131">筆記</span><span class="sxs-lookup"><span data-stu-id="4babc-131">NOTES</span></span>

## <span data-ttu-id="4babc-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="4babc-132">RELATED LINKS</span></span>
