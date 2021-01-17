---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: f9bf63a65642e62e7f0416f0f053ef62277fa9bf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98450035"
---
# <span data-ttu-id="bcc43-101">Remove-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="bcc43-101">Remove-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="bcc43-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bcc43-102">SYNOPSIS</span></span>
<span data-ttu-id="bcc43-103">從工作區移除已儲存的搜尋。</span><span class="sxs-lookup"><span data-stu-id="bcc43-103">Removes a saved search from the workspace.</span></span>

## <span data-ttu-id="bcc43-104">句法</span><span class="sxs-lookup"><span data-stu-id="bcc43-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcc43-105">說明</span><span class="sxs-lookup"><span data-stu-id="bcc43-105">DESCRIPTION</span></span>
<span data-ttu-id="bcc43-106">**AzOperationalInsightsSavedSearch** Cmdlet 會從工作區移除已儲存的搜尋。</span><span class="sxs-lookup"><span data-stu-id="bcc43-106">The **Remove-AzOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="bcc43-107">示例</span><span class="sxs-lookup"><span data-stu-id="bcc43-107">EXAMPLES</span></span>

### <span data-ttu-id="bcc43-108">範例1：移除已儲存的搜尋</span><span class="sxs-lookup"><span data-stu-id="bcc43-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="bcc43-109">這個命令會從工作區移除已儲存的搜尋。</span><span class="sxs-lookup"><span data-stu-id="bcc43-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="bcc43-110">參數</span><span class="sxs-lookup"><span data-stu-id="bcc43-110">PARAMETERS</span></span>

### <span data-ttu-id="bcc43-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcc43-111">-DefaultProfile</span></span>
<span data-ttu-id="bcc43-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bcc43-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcc43-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcc43-113">-ResourceGroupName</span></span>
<span data-ttu-id="bcc43-114">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="bcc43-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="bcc43-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="bcc43-115">-SavedSearchId</span></span>
<span data-ttu-id="bcc43-116">指定已儲存的搜尋識別碼。</span><span class="sxs-lookup"><span data-stu-id="bcc43-116">Specifies the saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc43-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bcc43-117">-WorkspaceName</span></span>
<span data-ttu-id="bcc43-118">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="bcc43-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcc43-119">-確認</span><span class="sxs-lookup"><span data-stu-id="bcc43-119">-Confirm</span></span>
<span data-ttu-id="bcc43-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bcc43-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc43-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcc43-121">-WhatIf</span></span>
<span data-ttu-id="bcc43-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bcc43-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcc43-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bcc43-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcc43-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcc43-124">CommonParameters</span></span>
<span data-ttu-id="bcc43-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bcc43-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcc43-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bcc43-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcc43-127">輸入</span><span class="sxs-lookup"><span data-stu-id="bcc43-127">INPUTS</span></span>

### <span data-ttu-id="bcc43-128">System.object</span><span class="sxs-lookup"><span data-stu-id="bcc43-128">System.String</span></span>

## <span data-ttu-id="bcc43-129">輸出</span><span class="sxs-lookup"><span data-stu-id="bcc43-129">OUTPUTS</span></span>

### <span data-ttu-id="bcc43-130">System.void</span><span class="sxs-lookup"><span data-stu-id="bcc43-130">System.Void</span></span>

## <span data-ttu-id="bcc43-131">筆記</span><span class="sxs-lookup"><span data-stu-id="bcc43-131">NOTES</span></span>

## <span data-ttu-id="bcc43-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="bcc43-132">RELATED LINKS</span></span>

[<span data-ttu-id="bcc43-133">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bcc43-133">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


