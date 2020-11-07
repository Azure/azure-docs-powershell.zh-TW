---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 10141D75-B58D-42B0-B0A6-92FF630E534C
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxperformancecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxPerformanceCollection.md
ms.openlocfilehash: 3a914aa970282d5157c9c72de0e328d7b927a238
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796606"
---
# <span data-ttu-id="3e899-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="3e899-101">Enable-AzOperationalInsightsLinuxPerformanceCollection</span></span>

## <span data-ttu-id="3e899-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3e899-102">SYNOPSIS</span></span>
<span data-ttu-id="3e899-103">從 Linux 電腦開始收集效能計數器。</span><span class="sxs-lookup"><span data-stu-id="3e899-103">Starts collection of performance counters from Linux computers.</span></span>

## <span data-ttu-id="3e899-104">句法</span><span class="sxs-lookup"><span data-stu-id="3e899-104">SYNTAX</span></span>

### <span data-ttu-id="3e899-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="3e899-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e899-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3e899-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxPerformanceCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e899-107">說明</span><span class="sxs-lookup"><span data-stu-id="3e899-107">DESCRIPTION</span></span>
<span data-ttu-id="3e899-108">**Enable-AzOperationalInsightsLinuxPerformanceCollection** Cmdlet 會從工作區中相互連接的 Linux 電腦開始收集效能計數器。</span><span class="sxs-lookup"><span data-stu-id="3e899-108">The **Enable-AzOperationalInsightsLinuxPerformanceCollection** cmdlet starts collection of performance counters from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="3e899-109">示例</span><span class="sxs-lookup"><span data-stu-id="3e899-109">EXAMPLES</span></span>

## <span data-ttu-id="3e899-110">參數</span><span class="sxs-lookup"><span data-stu-id="3e899-110">PARAMETERS</span></span>

### <span data-ttu-id="3e899-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e899-111">-DefaultProfile</span></span>
<span data-ttu-id="3e899-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3e899-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e899-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e899-113">-ResourceGroupName</span></span>
<span data-ttu-id="3e899-114">指定包含 Linux 電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e899-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="3e899-115">-工作區</span><span class="sxs-lookup"><span data-stu-id="3e899-115">-Workspace</span></span>
<span data-ttu-id="3e899-116">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="3e899-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3e899-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3e899-117">-WorkspaceName</span></span>
<span data-ttu-id="3e899-118">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="3e899-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3e899-119">-確認</span><span class="sxs-lookup"><span data-stu-id="3e899-119">-Confirm</span></span>
<span data-ttu-id="3e899-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3e899-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e899-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e899-121">-WhatIf</span></span>
<span data-ttu-id="3e899-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3e899-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e899-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3e899-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e899-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e899-124">CommonParameters</span></span>
<span data-ttu-id="3e899-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3e899-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e899-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3e899-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e899-127">輸入</span><span class="sxs-lookup"><span data-stu-id="3e899-127">INPUTS</span></span>

### <span data-ttu-id="3e899-128">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="3e899-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="3e899-129">System.object</span><span class="sxs-lookup"><span data-stu-id="3e899-129">System.String</span></span>

## <span data-ttu-id="3e899-130">輸出</span><span class="sxs-lookup"><span data-stu-id="3e899-130">OUTPUTS</span></span>

### <span data-ttu-id="3e899-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="3e899-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="3e899-132">筆記</span><span class="sxs-lookup"><span data-stu-id="3e899-132">NOTES</span></span>
* <span data-ttu-id="3e899-133">關鍵字： azure，azurerm，arm，資源，管理，管理員，作業，洞察力</span><span class="sxs-lookup"><span data-stu-id="3e899-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="3e899-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e899-134">RELATED LINKS</span></span>

[<span data-ttu-id="3e899-135">Disable-AzOperationalInsightsLinuxPerformanceCollection</span><span class="sxs-lookup"><span data-stu-id="3e899-135">Disable-AzOperationalInsightsLinuxPerformanceCollection</span></span>](./Disable-AzOperationalInsightsLinuxPerformanceCollection.md)


