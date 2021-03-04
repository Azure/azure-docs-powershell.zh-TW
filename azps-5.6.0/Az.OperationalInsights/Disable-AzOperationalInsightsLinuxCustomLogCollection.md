---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: EF3FE3F1-1C8F-41EB-990E-F2B30BD9D082
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/disable-azoperationalinsightslinuxcustomlogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Disable-AzOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: db1e013fb1d8cdf72841e7b51f29481742d5f023
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913805"
---
# <span data-ttu-id="cc38f-101">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="cc38f-101">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="cc38f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cc38f-102">SYNOPSIS</span></span>
<span data-ttu-id="cc38f-103">停止從 Linux 電腦收集自訂記錄。</span><span class="sxs-lookup"><span data-stu-id="cc38f-103">Stops collection of custom logs from Linux computers.</span></span>

## <span data-ttu-id="cc38f-104">語法</span><span class="sxs-lookup"><span data-stu-id="cc38f-104">SYNTAX</span></span>

### <span data-ttu-id="cc38f-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="cc38f-105">ByWorkspaceName (Default)</span></span>
```
Disable-AzOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc38f-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="cc38f-106">ByWorkspaceObject</span></span>
```
Disable-AzOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc38f-107">描述</span><span class="sxs-lookup"><span data-stu-id="cc38f-107">DESCRIPTION</span></span>
<span data-ttu-id="cc38f-108">**Disable-AzOperationalInsights LinuxCustomLogCollection** Cmdlet 會停止工作區中已連接 Linux 電腦之自訂記錄的集合。</span><span class="sxs-lookup"><span data-stu-id="cc38f-108">The **Disable-AzOperationalInsightsLinuxCustomLogCollection** cmdlet stops collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="cc38f-109">例子</span><span class="sxs-lookup"><span data-stu-id="cc38f-109">EXAMPLES</span></span>

## <span data-ttu-id="cc38f-110">參數</span><span class="sxs-lookup"><span data-stu-id="cc38f-110">PARAMETERS</span></span>

### <span data-ttu-id="cc38f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc38f-111">-DefaultProfile</span></span>
<span data-ttu-id="cc38f-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="cc38f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc38f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc38f-113">-ResourceGroupName</span></span>
<span data-ttu-id="cc38f-114">指定包含 Linux 電腦的資源組名。</span><span class="sxs-lookup"><span data-stu-id="cc38f-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="cc38f-115">-工作區</span><span class="sxs-lookup"><span data-stu-id="cc38f-115">-Workspace</span></span>
<span data-ttu-id="cc38f-116">指定此 Cmdlet 在哪個工作區中操作。</span><span class="sxs-lookup"><span data-stu-id="cc38f-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="cc38f-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cc38f-117">-WorkspaceName</span></span>
<span data-ttu-id="cc38f-118">指定此 Cmdlet 操作之工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="cc38f-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="cc38f-119">-確認</span><span class="sxs-lookup"><span data-stu-id="cc38f-119">-Confirm</span></span>
<span data-ttu-id="cc38f-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="cc38f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc38f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc38f-121">-WhatIf</span></span>
<span data-ttu-id="cc38f-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cc38f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc38f-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cc38f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc38f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc38f-124">CommonParameters</span></span>
<span data-ttu-id="cc38f-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cc38f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc38f-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="cc38f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc38f-127">輸入</span><span class="sxs-lookup"><span data-stu-id="cc38f-127">INPUTS</span></span>

### <span data-ttu-id="cc38f-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="cc38f-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="cc38f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="cc38f-129">System.String</span></span>

## <span data-ttu-id="cc38f-130">輸出</span><span class="sxs-lookup"><span data-stu-id="cc38f-130">OUTPUTS</span></span>

### <span data-ttu-id="cc38f-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="cc38f-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="cc38f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="cc38f-132">NOTES</span></span>
* <span data-ttu-id="cc38f-133">關鍵字：azure、azurerm、arm、資源、管理、主管、營運、深入資訊</span><span class="sxs-lookup"><span data-stu-id="cc38f-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="cc38f-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="cc38f-134">RELATED LINKS</span></span>

[<span data-ttu-id="cc38f-135">Enable-AzOperationalInsightsTomLogCollection</span><span class="sxs-lookup"><span data-stu-id="cc38f-135">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)


