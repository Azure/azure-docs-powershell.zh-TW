---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 0a7bbc6832c5a0c6c871d2a5c35ac9ee86042fd0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621295"
---
# <span data-ttu-id="817bd-101">New-AzOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="817bd-101">New-AzOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="817bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="817bd-102">SYNOPSIS</span></span>
<span data-ttu-id="817bd-103">從指定的訂閱收集 Azure 活動記錄。</span><span class="sxs-lookup"><span data-stu-id="817bd-103">Collect Azure Activity log from given subscription.</span></span>

## <span data-ttu-id="817bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="817bd-104">SYNTAX</span></span>

### <span data-ttu-id="817bd-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="817bd-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="817bd-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="817bd-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="817bd-107">說明</span><span class="sxs-lookup"><span data-stu-id="817bd-107">DESCRIPTION</span></span>
<span data-ttu-id="817bd-108">New-AzOperationalInsightsAzureActivityLogDataSource 啟用 Log Analytics 以從指定的訂閱收集 Azure 活動記錄。</span><span class="sxs-lookup"><span data-stu-id="817bd-108">The New-AzOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="817bd-109">示例</span><span class="sxs-lookup"><span data-stu-id="817bd-109">EXAMPLES</span></span>

### <span data-ttu-id="817bd-110">範例1</span><span class="sxs-lookup"><span data-stu-id="817bd-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="817bd-111">{{在此處新增範例描述}}</span><span class="sxs-lookup"><span data-stu-id="817bd-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="817bd-112">參數</span><span class="sxs-lookup"><span data-stu-id="817bd-112">PARAMETERS</span></span>

### <span data-ttu-id="817bd-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="817bd-113">-BackfillStartTime</span></span>
<span data-ttu-id="817bd-114">您可以選擇從一周之前回填記錄。</span><span class="sxs-lookup"><span data-stu-id="817bd-114">You can choose to backfill logs from a week ago.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="817bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="817bd-115">-DefaultProfile</span></span>
<span data-ttu-id="817bd-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="817bd-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="817bd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="817bd-117">-Force</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="817bd-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="817bd-118">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="817bd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="817bd-119">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="817bd-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="817bd-120">-SubscriptionId</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="817bd-121">-工作區</span><span class="sxs-lookup"><span data-stu-id="817bd-121">-Workspace</span></span>
```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="817bd-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="817bd-122">-WorkspaceName</span></span>
```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="817bd-123">-確認</span><span class="sxs-lookup"><span data-stu-id="817bd-123">-Confirm</span></span>
<span data-ttu-id="817bd-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="817bd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="817bd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="817bd-125">-WhatIf</span></span>
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

### <span data-ttu-id="817bd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="817bd-126">CommonParameters</span></span>
<span data-ttu-id="817bd-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="817bd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="817bd-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="817bd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="817bd-129">輸入</span><span class="sxs-lookup"><span data-stu-id="817bd-129">INPUTS</span></span>

### <span data-ttu-id="817bd-130">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="817bd-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="817bd-131">System.object</span><span class="sxs-lookup"><span data-stu-id="817bd-131">System.String</span></span>

### <span data-ttu-id="817bd-132">System.object</span><span class="sxs-lookup"><span data-stu-id="817bd-132">System.DateTimeOffset</span></span>

## <span data-ttu-id="817bd-133">輸出</span><span class="sxs-lookup"><span data-stu-id="817bd-133">OUTPUTS</span></span>

### <span data-ttu-id="817bd-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="817bd-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="817bd-135">筆記</span><span class="sxs-lookup"><span data-stu-id="817bd-135">NOTES</span></span>

## <span data-ttu-id="817bd-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="817bd-136">RELATED LINKS</span></span>
