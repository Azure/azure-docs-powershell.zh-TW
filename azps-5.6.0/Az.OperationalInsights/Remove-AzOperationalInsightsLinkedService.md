---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 8a78fc36e13360babc43b512dccee80550b3fbf9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911581"
---
# <span data-ttu-id="1ccde-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="1ccde-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="1ccde-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1ccde-102">SYNOPSIS</span></span>
<span data-ttu-id="1ccde-103">取消工作區服務連結</span><span class="sxs-lookup"><span data-stu-id="1ccde-103">Unlink service for workspace</span></span>

## <span data-ttu-id="1ccde-104">語法</span><span class="sxs-lookup"><span data-stu-id="1ccde-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ccde-105">描述</span><span class="sxs-lookup"><span data-stu-id="1ccde-105">DESCRIPTION</span></span>
<span data-ttu-id="1ccde-106">取消工作區服務連結</span><span class="sxs-lookup"><span data-stu-id="1ccde-106">Unlink service for workspace</span></span>

## <span data-ttu-id="1ccde-107">例子</span><span class="sxs-lookup"><span data-stu-id="1ccde-107">EXAMPLES</span></span>

### <span data-ttu-id="1ccde-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="1ccde-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="1ccde-109">取消連結工作區的連結服務</span><span class="sxs-lookup"><span data-stu-id="1ccde-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="1ccde-110">參數</span><span class="sxs-lookup"><span data-stu-id="1ccde-110">PARAMETERS</span></span>

### <span data-ttu-id="1ccde-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ccde-111">-AsJob</span></span>
<span data-ttu-id="1ccde-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1ccde-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ccde-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ccde-113">-DefaultProfile</span></span>
<span data-ttu-id="1ccde-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ccde-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ccde-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="1ccde-115">-LinkedServiceName</span></span>
<span data-ttu-id="1ccde-116">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="1ccde-116">The Workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ccde-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ccde-117">-ResourceGroupName</span></span>
<span data-ttu-id="1ccde-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="1ccde-118">The resource group name.</span></span>

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

### <span data-ttu-id="1ccde-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1ccde-119">-WorkspaceName</span></span>
<span data-ttu-id="1ccde-120">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="1ccde-120">The Workspace name.</span></span>

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

### <span data-ttu-id="1ccde-121">-確認</span><span class="sxs-lookup"><span data-stu-id="1ccde-121">-Confirm</span></span>
<span data-ttu-id="1ccde-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1ccde-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ccde-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ccde-123">-WhatIf</span></span>
<span data-ttu-id="1ccde-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1ccde-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ccde-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ccde-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ccde-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ccde-126">CommonParameters</span></span>
<span data-ttu-id="1ccde-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1ccde-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ccde-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ccde-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ccde-129">輸入</span><span class="sxs-lookup"><span data-stu-id="1ccde-129">INPUTS</span></span>

### <span data-ttu-id="1ccde-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1ccde-130">System.String</span></span>

## <span data-ttu-id="1ccde-131">輸出</span><span class="sxs-lookup"><span data-stu-id="1ccde-131">OUTPUTS</span></span>

### <span data-ttu-id="1ccde-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1ccde-132">System.Boolean</span></span>

## <span data-ttu-id="1ccde-133">筆記</span><span class="sxs-lookup"><span data-stu-id="1ccde-133">NOTES</span></span>

## <span data-ttu-id="1ccde-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ccde-134">RELATED LINKS</span></span>
