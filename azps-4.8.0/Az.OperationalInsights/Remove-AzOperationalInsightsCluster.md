---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsCluster.md
ms.openlocfilehash: 4bcc62d3b5bd52382c5d02eb3761c51af27c1ca3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135475"
---
# <span data-ttu-id="57b6c-101">Remove-AzOperationalInsightsCluster</span><span class="sxs-lookup"><span data-stu-id="57b6c-101">Remove-AzOperationalInsightsCluster</span></span>

## <span data-ttu-id="57b6c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="57b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="57b6c-103">刪除群集</span><span class="sxs-lookup"><span data-stu-id="57b6c-103">Delete cluster</span></span>

## <span data-ttu-id="57b6c-104">句法</span><span class="sxs-lookup"><span data-stu-id="57b6c-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsCluster [-ResourceGroupName] <String> [-ClusterName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57b6c-105">說明</span><span class="sxs-lookup"><span data-stu-id="57b6c-105">DESCRIPTION</span></span>
<span data-ttu-id="57b6c-106">刪除群集，只適用于配件狀態為 "Succeeded" 的群集</span><span class="sxs-lookup"><span data-stu-id="57b6c-106">Delete cluster, only apply to clusters with provisioning state "Succeeded"</span></span>

## <span data-ttu-id="57b6c-107">示例</span><span class="sxs-lookup"><span data-stu-id="57b6c-107">EXAMPLES</span></span>

### <span data-ttu-id="57b6c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="57b6c-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsCluster -ResourceGroupName {rg-name} -ClusterName {cluster-name}

true
```

<span data-ttu-id="57b6c-109">刪除群集</span><span class="sxs-lookup"><span data-stu-id="57b6c-109">Delete cluster</span></span>

## <span data-ttu-id="57b6c-110">參數</span><span class="sxs-lookup"><span data-stu-id="57b6c-110">PARAMETERS</span></span>

### <span data-ttu-id="57b6c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57b6c-111">-AsJob</span></span>
<span data-ttu-id="57b6c-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="57b6c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57b6c-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="57b6c-113">-ClusterName</span></span>
<span data-ttu-id="57b6c-114">[群集名稱]。</span><span class="sxs-lookup"><span data-stu-id="57b6c-114">The cluster name.</span></span>

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

### <span data-ttu-id="57b6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57b6c-115">-DefaultProfile</span></span>
<span data-ttu-id="57b6c-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="57b6c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57b6c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57b6c-117">-ResourceGroupName</span></span>
<span data-ttu-id="57b6c-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="57b6c-118">The resource group name.</span></span>

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

### <span data-ttu-id="57b6c-119">-確認</span><span class="sxs-lookup"><span data-stu-id="57b6c-119">-Confirm</span></span>
<span data-ttu-id="57b6c-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="57b6c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57b6c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57b6c-121">-WhatIf</span></span>
<span data-ttu-id="57b6c-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="57b6c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57b6c-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="57b6c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57b6c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57b6c-124">CommonParameters</span></span>
<span data-ttu-id="57b6c-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="57b6c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57b6c-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="57b6c-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57b6c-127">輸入</span><span class="sxs-lookup"><span data-stu-id="57b6c-127">INPUTS</span></span>

### <span data-ttu-id="57b6c-128">System.object</span><span class="sxs-lookup"><span data-stu-id="57b6c-128">System.String</span></span>

## <span data-ttu-id="57b6c-129">輸出</span><span class="sxs-lookup"><span data-stu-id="57b6c-129">OUTPUTS</span></span>

### <span data-ttu-id="57b6c-130">System.object</span><span class="sxs-lookup"><span data-stu-id="57b6c-130">System.Boolean</span></span>

## <span data-ttu-id="57b6c-131">筆記</span><span class="sxs-lookup"><span data-stu-id="57b6c-131">NOTES</span></span>

## <span data-ttu-id="57b6c-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="57b6c-132">RELATED LINKS</span></span>