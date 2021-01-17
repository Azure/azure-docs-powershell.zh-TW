---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: c62dcefc2a4cfabc908c45454f3907c2da060f6c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98450036"
---
# <span data-ttu-id="dbb0f-101">Remove-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="dbb0f-101">Remove-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="dbb0f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dbb0f-102">SYNOPSIS</span></span>
<span data-ttu-id="dbb0f-103">取消連結工作區的服務</span><span class="sxs-lookup"><span data-stu-id="dbb0f-103">Unlink service for workspace</span></span>

## <span data-ttu-id="dbb0f-104">句法</span><span class="sxs-lookup"><span data-stu-id="dbb0f-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dbb0f-105">說明</span><span class="sxs-lookup"><span data-stu-id="dbb0f-105">DESCRIPTION</span></span>
<span data-ttu-id="dbb0f-106">取消連結工作區的服務</span><span class="sxs-lookup"><span data-stu-id="dbb0f-106">Unlink service for workspace</span></span>

## <span data-ttu-id="dbb0f-107">示例</span><span class="sxs-lookup"><span data-stu-id="dbb0f-107">EXAMPLES</span></span>

### <span data-ttu-id="dbb0f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="dbb0f-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

true
```

<span data-ttu-id="dbb0f-109">取消連結工作區的連結服務</span><span class="sxs-lookup"><span data-stu-id="dbb0f-109">Unlink linked service for workspace</span></span>

## <span data-ttu-id="dbb0f-110">參數</span><span class="sxs-lookup"><span data-stu-id="dbb0f-110">PARAMETERS</span></span>

### <span data-ttu-id="dbb0f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dbb0f-111">-AsJob</span></span>
<span data-ttu-id="dbb0f-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="dbb0f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dbb0f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbb0f-113">-DefaultProfile</span></span>
<span data-ttu-id="dbb0f-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dbb0f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbb0f-115">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="dbb0f-115">-LinkedServiceName</span></span>
<span data-ttu-id="dbb0f-116">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="dbb0f-116">The Workspace name.</span></span>

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

### <span data-ttu-id="dbb0f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbb0f-117">-ResourceGroupName</span></span>
<span data-ttu-id="dbb0f-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dbb0f-118">The resource group name.</span></span>

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

### <span data-ttu-id="dbb0f-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dbb0f-119">-WorkspaceName</span></span>
<span data-ttu-id="dbb0f-120">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="dbb0f-120">The Workspace name.</span></span>

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

### <span data-ttu-id="dbb0f-121">-確認</span><span class="sxs-lookup"><span data-stu-id="dbb0f-121">-Confirm</span></span>
<span data-ttu-id="dbb0f-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="dbb0f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbb0f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbb0f-123">-WhatIf</span></span>
<span data-ttu-id="dbb0f-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="dbb0f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbb0f-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="dbb0f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbb0f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbb0f-126">CommonParameters</span></span>
<span data-ttu-id="dbb0f-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dbb0f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbb0f-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="dbb0f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbb0f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="dbb0f-129">INPUTS</span></span>

### <span data-ttu-id="dbb0f-130">System.object</span><span class="sxs-lookup"><span data-stu-id="dbb0f-130">System.String</span></span>

## <span data-ttu-id="dbb0f-131">輸出</span><span class="sxs-lookup"><span data-stu-id="dbb0f-131">OUTPUTS</span></span>

### <span data-ttu-id="dbb0f-132">System.object</span><span class="sxs-lookup"><span data-stu-id="dbb0f-132">System.Boolean</span></span>

## <span data-ttu-id="dbb0f-133">筆記</span><span class="sxs-lookup"><span data-stu-id="dbb0f-133">NOTES</span></span>

## <span data-ttu-id="dbb0f-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="dbb0f-134">RELATED LINKS</span></span>
