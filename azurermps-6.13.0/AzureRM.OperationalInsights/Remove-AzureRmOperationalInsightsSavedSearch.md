---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: a438a84a25e100539f485b5d3a7012f03ee355a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450185"
---
# <span data-ttu-id="af58e-101">Remove-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="af58e-101">Remove-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="af58e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af58e-102">SYNOPSIS</span></span>
<span data-ttu-id="af58e-103">從工作區移除已儲存的搜尋。</span><span class="sxs-lookup"><span data-stu-id="af58e-103">Removes a saved search from the workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af58e-104">句法</span><span class="sxs-lookup"><span data-stu-id="af58e-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af58e-105">說明</span><span class="sxs-lookup"><span data-stu-id="af58e-105">DESCRIPTION</span></span>
<span data-ttu-id="af58e-106">**AzureRmOperationalInsightsSavedSearch** Cmdlet 會從工作區移除已儲存的搜尋。</span><span class="sxs-lookup"><span data-stu-id="af58e-106">The **Remove-AzureRmOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="af58e-107">示例</span><span class="sxs-lookup"><span data-stu-id="af58e-107">EXAMPLES</span></span>

### <span data-ttu-id="af58e-108">範例1：移除已儲存的搜尋</span><span class="sxs-lookup"><span data-stu-id="af58e-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="af58e-109">這個命令會從工作區移除已儲存的搜尋。</span><span class="sxs-lookup"><span data-stu-id="af58e-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="af58e-110">參數</span><span class="sxs-lookup"><span data-stu-id="af58e-110">PARAMETERS</span></span>

### <span data-ttu-id="af58e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af58e-111">-DefaultProfile</span></span>
<span data-ttu-id="af58e-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="af58e-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="af58e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af58e-113">-ResourceGroupName</span></span>
<span data-ttu-id="af58e-114">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="af58e-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="af58e-115">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="af58e-115">-SavedSearchId</span></span>
<span data-ttu-id="af58e-116">指定已儲存的搜尋識別碼。</span><span class="sxs-lookup"><span data-stu-id="af58e-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="af58e-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="af58e-117">-WorkspaceName</span></span>
<span data-ttu-id="af58e-118">指定工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="af58e-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="af58e-119">-確認</span><span class="sxs-lookup"><span data-stu-id="af58e-119">-Confirm</span></span>
<span data-ttu-id="af58e-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="af58e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af58e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af58e-121">-WhatIf</span></span>
<span data-ttu-id="af58e-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="af58e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af58e-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="af58e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af58e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af58e-124">CommonParameters</span></span>
<span data-ttu-id="af58e-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af58e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af58e-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="af58e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af58e-127">輸入</span><span class="sxs-lookup"><span data-stu-id="af58e-127">INPUTS</span></span>

### <span data-ttu-id="af58e-128">System.object</span><span class="sxs-lookup"><span data-stu-id="af58e-128">System.String</span></span>

## <span data-ttu-id="af58e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="af58e-129">OUTPUTS</span></span>

### <span data-ttu-id="af58e-130">System.void</span><span class="sxs-lookup"><span data-stu-id="af58e-130">System.Void</span></span>

## <span data-ttu-id="af58e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="af58e-131">NOTES</span></span>

## <span data-ttu-id="af58e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="af58e-132">RELATED LINKS</span></span>

[<span data-ttu-id="af58e-133">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="af58e-133">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


