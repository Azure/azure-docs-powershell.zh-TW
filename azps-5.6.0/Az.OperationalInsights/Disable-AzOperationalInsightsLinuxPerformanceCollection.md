---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 47AFBAC7-8818-4788-B685-7AB4DCD6C2DE
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: f5a7a5930adde047fe4b0d2766711050bff9e91d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913798"
---
# <span data-ttu-id="e29a6-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="e29a6-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="e29a6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e29a6-102">SYNOPSIS</span></span>
<span data-ttu-id="e29a6-103">停止收集 Linux 電腦中的效能計數器。</span><span class="sxs-lookup"><span data-stu-id="e29a6-103">Stops collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="e29a6-104">語法</span><span class="sxs-lookup"><span data-stu-id="e29a6-104">SYNTAX</span></span>

### <span data-ttu-id="e29a6-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="e29a6-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e29a6-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e29a6-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e29a6-107">描述</span><span class="sxs-lookup"><span data-stu-id="e29a6-107">DESCRIPTION</span></span>
<span data-ttu-id="e29a6-108">**Disable-AzOperationalInsights WorkspacePerformanceCollection** Cmdlet 會停止工作區中已連接 Linux 電腦之效能計數器的集合。</span><span class="sxs-lookup"><span data-stu-id="e29a6-108">The **Disable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet stops collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="e29a6-109">例子</span><span class="sxs-lookup"><span data-stu-id="e29a6-109">EXAMPLES</span></span>

## <span data-ttu-id="e29a6-110">參數</span><span class="sxs-lookup"><span data-stu-id="e29a6-110">PARAMETERS</span></span>

### <span data-ttu-id="e29a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e29a6-111">-DefaultProfile</span></span>
<span data-ttu-id="e29a6-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e29a6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e29a6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e29a6-113">-ResourceGroupName</span></span>
<span data-ttu-id="e29a6-114">指定包含 Linux 電腦的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e29a6-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="e29a6-115">-工作區</span><span class="sxs-lookup"><span data-stu-id="e29a6-115">-Workspace</span></span>
<span data-ttu-id="e29a6-116">指定此 Cmdlet 在哪個工作區中操作。</span><span class="sxs-lookup"><span data-stu-id="e29a6-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e29a6-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e29a6-117">-WorkspaceName</span></span>
<span data-ttu-id="e29a6-118">指定此 Cmdlet 操作之工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="e29a6-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e29a6-119">-確認</span><span class="sxs-lookup"><span data-stu-id="e29a6-119">-Confirm</span></span>
<span data-ttu-id="e29a6-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e29a6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e29a6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e29a6-121">-WhatIf</span></span>
<span data-ttu-id="e29a6-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e29a6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e29a6-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e29a6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e29a6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e29a6-124">CommonParameters</span></span>
<span data-ttu-id="e29a6-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e29a6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e29a6-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e29a6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e29a6-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e29a6-127">INPUTS</span></span>

### <span data-ttu-id="e29a6-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="e29a6-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="e29a6-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e29a6-129">System.String</span></span>

## <span data-ttu-id="e29a6-130">輸出</span><span class="sxs-lookup"><span data-stu-id="e29a6-130">OUTPUTS</span></span>

### <span data-ttu-id="e29a6-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="e29a6-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e29a6-132">筆記</span><span class="sxs-lookup"><span data-stu-id="e29a6-132">NOTES</span></span>
* <span data-ttu-id="e29a6-133">關鍵字：azure、azurerm、arm、資源、管理、主管、營運、深入資訊</span><span class="sxs-lookup"><span data-stu-id="e29a6-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="e29a6-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="e29a6-134">RELATED LINKS</span></span>

[<span data-ttu-id="e29a6-135">Enable-AzOperationalInsights</span><span class="sxs-lookup"><span data-stu-id="e29a6-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="e29a6-136">New-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="e29a6-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


