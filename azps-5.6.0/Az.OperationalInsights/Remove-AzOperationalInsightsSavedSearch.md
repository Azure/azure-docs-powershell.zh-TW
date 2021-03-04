---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 02dded0f03b1ba7bd0936e364b229864e0955022
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911558"
---
# <span data-ttu-id="2fbb0-101">Remove-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="2fbb0-101">Remove-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="2fbb0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2fbb0-102">SYNOPSIS</span></span>
<span data-ttu-id="2fbb0-103">從工作區移除已儲存的搜尋。</span><span class="sxs-lookup"><span data-stu-id="2fbb0-103">Removes a saved search from the workspace.</span></span>

## <span data-ttu-id="2fbb0-104">語法</span><span class="sxs-lookup"><span data-stu-id="2fbb0-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fbb0-105">描述</span><span class="sxs-lookup"><span data-stu-id="2fbb0-105">DESCRIPTION</span></span>
<span data-ttu-id="2fbb0-106">**Remove-AzOperationalInsightsSavedSearch** Cmdlet 會從工作區移除已儲存的搜尋。</span><span class="sxs-lookup"><span data-stu-id="2fbb0-106">The **Remove-AzOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="2fbb0-107">例子</span><span class="sxs-lookup"><span data-stu-id="2fbb0-107">EXAMPLES</span></span>

### <span data-ttu-id="2fbb0-108">範例 1：移除儲存的搜尋</span><span class="sxs-lookup"><span data-stu-id="2fbb0-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="2fbb0-109">此命令會從工作區移除已儲存的搜尋。</span><span class="sxs-lookup"><span data-stu-id="2fbb0-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="2fbb0-110">參數</span><span class="sxs-lookup"><span data-stu-id="2fbb0-110">PARAMETERS</span></span>

### <span data-ttu-id="2fbb0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fbb0-111">-DefaultProfile</span></span>
<span data-ttu-id="2fbb0-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="2fbb0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fbb0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fbb0-113">-ResourceGroupName</span></span>
<span data-ttu-id="2fbb0-114">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="2fbb0-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="2fbb0-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="2fbb0-115">-SavedSearchId</span></span>
<span data-ttu-id="2fbb0-116">指定儲存的搜尋識別碼。</span><span class="sxs-lookup"><span data-stu-id="2fbb0-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="2fbb0-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2fbb0-117">-WorkspaceName</span></span>
<span data-ttu-id="2fbb0-118">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="2fbb0-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="2fbb0-119">-確認</span><span class="sxs-lookup"><span data-stu-id="2fbb0-119">-Confirm</span></span>
<span data-ttu-id="2fbb0-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2fbb0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fbb0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fbb0-121">-WhatIf</span></span>
<span data-ttu-id="2fbb0-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2fbb0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fbb0-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2fbb0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fbb0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fbb0-124">CommonParameters</span></span>
<span data-ttu-id="2fbb0-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2fbb0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fbb0-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2fbb0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fbb0-127">輸入</span><span class="sxs-lookup"><span data-stu-id="2fbb0-127">INPUTS</span></span>

### <span data-ttu-id="2fbb0-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2fbb0-128">System.String</span></span>

## <span data-ttu-id="2fbb0-129">輸出</span><span class="sxs-lookup"><span data-stu-id="2fbb0-129">OUTPUTS</span></span>

### <span data-ttu-id="2fbb0-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="2fbb0-130">System.Void</span></span>

## <span data-ttu-id="2fbb0-131">筆記</span><span class="sxs-lookup"><span data-stu-id="2fbb0-131">NOTES</span></span>

## <span data-ttu-id="2fbb0-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="2fbb0-132">RELATED LINKS</span></span>

[<span data-ttu-id="2fbb0-133">Azure 營運深入資訊 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2fbb0-133">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


