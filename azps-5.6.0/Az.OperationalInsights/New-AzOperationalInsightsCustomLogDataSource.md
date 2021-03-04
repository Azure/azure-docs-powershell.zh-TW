---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: e923d413b889583578efb0ac81f9eb6aeadf72fa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908374"
---
# <span data-ttu-id="8e9e2-101">New-AzOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="8e9e2-101">New-AzOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="8e9e2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8e9e2-102">SYNOPSIS</span></span>
<span data-ttu-id="8e9e2-103">定義自訂記錄集合策略。</span><span class="sxs-lookup"><span data-stu-id="8e9e2-103">Defines a custom log collection policy.</span></span>

## <span data-ttu-id="8e9e2-104">語法</span><span class="sxs-lookup"><span data-stu-id="8e9e2-104">SYNTAX</span></span>

### <span data-ttu-id="8e9e2-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="8e9e2-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e9e2-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="8e9e2-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e9e2-107">描述</span><span class="sxs-lookup"><span data-stu-id="8e9e2-107">DESCRIPTION</span></span>
<span data-ttu-id="8e9e2-108">**New-AzOperationalInsightsCustomLogDataSource** Cmdlet 會定義自訂記錄集合原則。</span><span class="sxs-lookup"><span data-stu-id="8e9e2-108">The **New-AzOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="8e9e2-109">例子</span><span class="sxs-lookup"><span data-stu-id="8e9e2-109">EXAMPLES</span></span>

## <span data-ttu-id="8e9e2-110">參數</span><span class="sxs-lookup"><span data-stu-id="8e9e2-110">PARAMETERS</span></span>

### <span data-ttu-id="8e9e2-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="8e9e2-111">-CustomLogRawJson</span></span>
<span data-ttu-id="8e9e2-112">指定自訂集合策略做為 JSON 字串 (JavaScript) 標記法。</span><span class="sxs-lookup"><span data-stu-id="8e9e2-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

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

### <span data-ttu-id="8e9e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e9e2-113">-DefaultProfile</span></span>
<span data-ttu-id="8e9e2-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8e9e2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e9e2-115">-強制</span><span class="sxs-lookup"><span data-stu-id="8e9e2-115">-Force</span></span>
<span data-ttu-id="8e9e2-116">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="8e9e2-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8e9e2-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="8e9e2-117">-Name</span></span>
<span data-ttu-id="8e9e2-118">指定資料來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e9e2-118">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="8e9e2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e9e2-119">-ResourceGroupName</span></span>
<span data-ttu-id="8e9e2-120">指定包含電腦的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8e9e2-120">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="8e9e2-121">-工作區</span><span class="sxs-lookup"><span data-stu-id="8e9e2-121">-Workspace</span></span>
<span data-ttu-id="8e9e2-122">指定此 Cmdlet 在哪個工作區中操作。</span><span class="sxs-lookup"><span data-stu-id="8e9e2-122">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8e9e2-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8e9e2-123">-WorkspaceName</span></span>
<span data-ttu-id="8e9e2-124">指定此 Cmdlet 操作之工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="8e9e2-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="8e9e2-125">-確認</span><span class="sxs-lookup"><span data-stu-id="8e9e2-125">-Confirm</span></span>
<span data-ttu-id="8e9e2-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8e9e2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e9e2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e9e2-127">-WhatIf</span></span>
<span data-ttu-id="8e9e2-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8e9e2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e9e2-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e9e2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e9e2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e9e2-130">CommonParameters</span></span>
<span data-ttu-id="8e9e2-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8e9e2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e9e2-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8e9e2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e9e2-133">輸入</span><span class="sxs-lookup"><span data-stu-id="8e9e2-133">INPUTS</span></span>

### <span data-ttu-id="8e9e2-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="8e9e2-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="8e9e2-135">System.String</span><span class="sxs-lookup"><span data-stu-id="8e9e2-135">System.String</span></span>

## <span data-ttu-id="8e9e2-136">輸出</span><span class="sxs-lookup"><span data-stu-id="8e9e2-136">OUTPUTS</span></span>

### <span data-ttu-id="8e9e2-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="8e9e2-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="8e9e2-138">筆記</span><span class="sxs-lookup"><span data-stu-id="8e9e2-138">NOTES</span></span>

## <span data-ttu-id="8e9e2-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e9e2-139">RELATED LINKS</span></span>

[<span data-ttu-id="8e9e2-140">Disable-AzOperationalInsightsTomLogCollection</span><span class="sxs-lookup"><span data-stu-id="8e9e2-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="8e9e2-141">Enable-AzOperationalInsightsTomLogCollection</span><span class="sxs-lookup"><span data-stu-id="8e9e2-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


