---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: B4EC9132-8DB9-498D-8B3F-2AB51D8EA03A
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightsazureactivitylogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsAzureActivityLogDataSource.md
ms.openlocfilehash: 900f8de58eaa8118c15a7d3ae1a2d88b0bdf59d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906542"
---
# <span data-ttu-id="13306-101">New-AzOperationalInsightsAzureActivityLogDataSource</span><span class="sxs-lookup"><span data-stu-id="13306-101">New-AzOperationalInsightsAzureActivityLogDataSource</span></span>

## <span data-ttu-id="13306-102">簡介</span><span class="sxs-lookup"><span data-stu-id="13306-102">SYNOPSIS</span></span>
<span data-ttu-id="13306-103">從給定訂閱收集 Azure 活動記錄。</span><span class="sxs-lookup"><span data-stu-id="13306-103">Collect Azure Activity log from given subscription.</span></span>

## <span data-ttu-id="13306-104">語法</span><span class="sxs-lookup"><span data-stu-id="13306-104">SYNTAX</span></span>

### <span data-ttu-id="13306-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="13306-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="13306-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="13306-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsAzureActivityLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-SubscriptionId] <String> [-BackfillStartTime <DateTimeOffset>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13306-107">描述</span><span class="sxs-lookup"><span data-stu-id="13306-107">DESCRIPTION</span></span>
<span data-ttu-id="13306-108">此New-AzOperationalInsightsAzureActivityLogDataSource記錄分析功能，以收集來自給定訂閱的 Azure 活動記錄。</span><span class="sxs-lookup"><span data-stu-id="13306-108">The New-AzOperationalInsightsAzureActivityLogDataSource enable Log Analytics to collect Azure activity log from given subscription.</span></span>

## <span data-ttu-id="13306-109">例子</span><span class="sxs-lookup"><span data-stu-id="13306-109">EXAMPLES</span></span>

### <span data-ttu-id="13306-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="13306-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="13306-111">{{ 在這裡新增範例描述 }}</span><span class="sxs-lookup"><span data-stu-id="13306-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="13306-112">參數</span><span class="sxs-lookup"><span data-stu-id="13306-112">PARAMETERS</span></span>

### <span data-ttu-id="13306-113">-BackfillStartTime</span><span class="sxs-lookup"><span data-stu-id="13306-113">-BackfillStartTime</span></span>
<span data-ttu-id="13306-114">您可以選擇從一周前重新填回記錄。</span><span class="sxs-lookup"><span data-stu-id="13306-114">You can choose to backfill logs from a week ago.</span></span>

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

### <span data-ttu-id="13306-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13306-115">-DefaultProfile</span></span>
<span data-ttu-id="13306-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="13306-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13306-117">-強制</span><span class="sxs-lookup"><span data-stu-id="13306-117">-Force</span></span>
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

### <span data-ttu-id="13306-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="13306-118">-Name</span></span>
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

### <span data-ttu-id="13306-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13306-119">-ResourceGroupName</span></span>
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

### <span data-ttu-id="13306-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13306-120">-SubscriptionId</span></span>
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

### <span data-ttu-id="13306-121">-工作區</span><span class="sxs-lookup"><span data-stu-id="13306-121">-Workspace</span></span>
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

### <span data-ttu-id="13306-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="13306-122">-WorkspaceName</span></span>
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

### <span data-ttu-id="13306-123">-確認</span><span class="sxs-lookup"><span data-stu-id="13306-123">-Confirm</span></span>
<span data-ttu-id="13306-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="13306-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13306-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13306-125">-WhatIf</span></span>
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

### <span data-ttu-id="13306-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13306-126">CommonParameters</span></span>
<span data-ttu-id="13306-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="13306-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13306-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="13306-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13306-129">輸入</span><span class="sxs-lookup"><span data-stu-id="13306-129">INPUTS</span></span>

### <span data-ttu-id="13306-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="13306-130">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="13306-131">System.String</span><span class="sxs-lookup"><span data-stu-id="13306-131">System.String</span></span>

### <span data-ttu-id="13306-132">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="13306-132">System.DateTimeOffset</span></span>

## <span data-ttu-id="13306-133">輸出</span><span class="sxs-lookup"><span data-stu-id="13306-133">OUTPUTS</span></span>

### <span data-ttu-id="13306-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="13306-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="13306-135">筆記</span><span class="sxs-lookup"><span data-stu-id="13306-135">NOTES</span></span>

## <span data-ttu-id="13306-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="13306-136">RELATED LINKS</span></span>
