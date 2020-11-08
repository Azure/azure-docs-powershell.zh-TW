---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 95B54065-B6CC-4D10-A747-28CE3F412ABF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/disable-azoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 71a0089b4f593032404b71f17ba432486f5498d7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94135487"
---
# <span data-ttu-id="d62b1-101">Disable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="d62b1-101">Disable-AzOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="d62b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d62b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d62b1-103">停止從電腦收集 IIS 記錄。</span><span class="sxs-lookup"><span data-stu-id="d62b1-103">Stops collection of IIS logs from computers.</span></span>

## <span data-ttu-id="d62b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="d62b1-104">SYNTAX</span></span>

### <span data-ttu-id="d62b1-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="d62b1-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d62b1-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d62b1-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d62b1-107">說明</span><span class="sxs-lookup"><span data-stu-id="d62b1-107">DESCRIPTION</span></span>
<span data-ttu-id="d62b1-108">**Disable AzOperationalInsightsIISLogCollection** Cmdlet 會停止收集網際網路資訊服務 (IIS) 記錄從工作區中已連接的電腦。</span><span class="sxs-lookup"><span data-stu-id="d62b1-108">The **Disable-AzOperationalInsightsIISLogCollection** cmdlet stops collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="d62b1-109">示例</span><span class="sxs-lookup"><span data-stu-id="d62b1-109">EXAMPLES</span></span>

## <span data-ttu-id="d62b1-110">參數</span><span class="sxs-lookup"><span data-stu-id="d62b1-110">PARAMETERS</span></span>

### <span data-ttu-id="d62b1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d62b1-111">-DefaultProfile</span></span>
<span data-ttu-id="d62b1-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d62b1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d62b1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d62b1-113">-ResourceGroupName</span></span>
<span data-ttu-id="d62b1-114">指定包含電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d62b1-114">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="d62b1-115">-工作區</span><span class="sxs-lookup"><span data-stu-id="d62b1-115">-Workspace</span></span>
<span data-ttu-id="d62b1-116">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="d62b1-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d62b1-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d62b1-117">-WorkspaceName</span></span>
<span data-ttu-id="d62b1-118">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="d62b1-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="d62b1-119">-確認</span><span class="sxs-lookup"><span data-stu-id="d62b1-119">-Confirm</span></span>
<span data-ttu-id="d62b1-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d62b1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d62b1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d62b1-121">-WhatIf</span></span>
<span data-ttu-id="d62b1-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d62b1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d62b1-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d62b1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d62b1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d62b1-124">CommonParameters</span></span>
<span data-ttu-id="d62b1-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d62b1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d62b1-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d62b1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d62b1-127">輸入</span><span class="sxs-lookup"><span data-stu-id="d62b1-127">INPUTS</span></span>

### <span data-ttu-id="d62b1-128">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="d62b1-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="d62b1-129">System.object</span><span class="sxs-lookup"><span data-stu-id="d62b1-129">System.String</span></span>

## <span data-ttu-id="d62b1-130">輸出</span><span class="sxs-lookup"><span data-stu-id="d62b1-130">OUTPUTS</span></span>

### <span data-ttu-id="d62b1-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="d62b1-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="d62b1-132">筆記</span><span class="sxs-lookup"><span data-stu-id="d62b1-132">NOTES</span></span>
* <span data-ttu-id="d62b1-133">關鍵字： azure，azurerm，arm，資源，管理，管理員，作業，洞察力</span><span class="sxs-lookup"><span data-stu-id="d62b1-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="d62b1-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="d62b1-134">RELATED LINKS</span></span>

[<span data-ttu-id="d62b1-135">Enable-AzOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="d62b1-135">Enable-AzOperationalInsightsIISLogCollection</span></span>](./Enable-AzOperationalInsightsIISLogCollection.md)


