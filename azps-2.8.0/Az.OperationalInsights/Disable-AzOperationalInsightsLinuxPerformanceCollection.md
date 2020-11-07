---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 47AFBAC7-8818-4788-B685-7AB4DCD6C2DE
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 0a39dae7ebdc6cc2c1fcc1b77ceb9b5d8e330d66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791784"
---
# <span data-ttu-id="07790-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="07790-101">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="07790-102">摘要</span><span class="sxs-lookup"><span data-stu-id="07790-102">SYNOPSIS</span></span>
<span data-ttu-id="07790-103">停止從 Linux 電腦收集效能計數器。</span><span class="sxs-lookup"><span data-stu-id="07790-103">Stops collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="07790-104">句法</span><span class="sxs-lookup"><span data-stu-id="07790-104">SYNTAX</span></span>

### <span data-ttu-id="07790-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="07790-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07790-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="07790-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07790-107">說明</span><span class="sxs-lookup"><span data-stu-id="07790-107">DESCRIPTION</span></span>
<span data-ttu-id="07790-108">**Disable AzOperationalInsightsLinuxPerformanceCollection** Cmdlet 會在工作區中停止已連接的 Linux 電腦的效能計數器收集。</span><span class="sxs-lookup"><span data-stu-id="07790-108">The **Disable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet stops collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="07790-109">示例</span><span class="sxs-lookup"><span data-stu-id="07790-109">EXAMPLES</span></span>

## <span data-ttu-id="07790-110">參數</span><span class="sxs-lookup"><span data-stu-id="07790-110">PARAMETERS</span></span>

### <span data-ttu-id="07790-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07790-111">-DefaultProfile</span></span>
<span data-ttu-id="07790-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="07790-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07790-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07790-113">-ResourceGroupName</span></span>
<span data-ttu-id="07790-114">指定包含 Linux 電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="07790-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="07790-115">-工作區</span><span class="sxs-lookup"><span data-stu-id="07790-115">-Workspace</span></span>
<span data-ttu-id="07790-116">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="07790-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="07790-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="07790-117">-WorkspaceName</span></span>
<span data-ttu-id="07790-118">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="07790-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="07790-119">-確認</span><span class="sxs-lookup"><span data-stu-id="07790-119">-Confirm</span></span>
<span data-ttu-id="07790-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="07790-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07790-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07790-121">-WhatIf</span></span>
<span data-ttu-id="07790-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="07790-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07790-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07790-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07790-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07790-124">CommonParameters</span></span>
<span data-ttu-id="07790-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="07790-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07790-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="07790-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07790-127">輸入</span><span class="sxs-lookup"><span data-stu-id="07790-127">INPUTS</span></span>

### <span data-ttu-id="07790-128">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="07790-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="07790-129">System.object</span><span class="sxs-lookup"><span data-stu-id="07790-129">System.String</span></span>

## <span data-ttu-id="07790-130">輸出</span><span class="sxs-lookup"><span data-stu-id="07790-130">OUTPUTS</span></span>

### <span data-ttu-id="07790-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="07790-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="07790-132">筆記</span><span class="sxs-lookup"><span data-stu-id="07790-132">NOTES</span></span>
* <span data-ttu-id="07790-133">關鍵字： azure，azurerm，arm，資源，管理，管理員，作業，洞察力</span><span class="sxs-lookup"><span data-stu-id="07790-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="07790-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="07790-134">RELATED LINKS</span></span>

[<span data-ttu-id="07790-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="07790-135">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Enable-AzOperationalInsightsLinuxPerformanceCollection.md)

[<span data-ttu-id="07790-136">新-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="07790-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


