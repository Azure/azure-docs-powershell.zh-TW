---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 66DD5919-B6B7-4FE5-B45B-937013549882
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: 2a007a2695141d0772afeb025644f8a3dbf4efb4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913777"
---
# <span data-ttu-id="df9b0-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="df9b0-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="df9b0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="df9b0-102">SYNOPSIS</span></span>
<span data-ttu-id="df9b0-103">從 Linux 電腦開始收集 syslog 資料。</span><span class="sxs-lookup"><span data-stu-id="df9b0-103">Starts collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="df9b0-104">語法</span><span class="sxs-lookup"><span data-stu-id="df9b0-104">SYNTAX</span></span>

### <span data-ttu-id="df9b0-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="df9b0-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df9b0-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="df9b0-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df9b0-107">描述</span><span class="sxs-lookup"><span data-stu-id="df9b0-107">DESCRIPTION</span></span>
<span data-ttu-id="df9b0-108">**Enable-AzOperationalInsights WorkspaceSyslogCollection** Cmdlet 會開始從工作區中連接的 Linux 電腦收集 syslog 資料。</span><span class="sxs-lookup"><span data-stu-id="df9b0-108">The **Enable-AzOperationalInsightsLinuxSyslogCollection** cmdlet starts collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="df9b0-109">例子</span><span class="sxs-lookup"><span data-stu-id="df9b0-109">EXAMPLES</span></span>

## <span data-ttu-id="df9b0-110">參數</span><span class="sxs-lookup"><span data-stu-id="df9b0-110">PARAMETERS</span></span>

### <span data-ttu-id="df9b0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df9b0-111">-DefaultProfile</span></span>
<span data-ttu-id="df9b0-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="df9b0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df9b0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df9b0-113">-ResourceGroupName</span></span>
<span data-ttu-id="df9b0-114">指定包含 Linux 電腦的資源組名。</span><span class="sxs-lookup"><span data-stu-id="df9b0-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="df9b0-115">-工作區</span><span class="sxs-lookup"><span data-stu-id="df9b0-115">-Workspace</span></span>
<span data-ttu-id="df9b0-116">指定此 Cmdlet 在哪個工作區中操作。</span><span class="sxs-lookup"><span data-stu-id="df9b0-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="df9b0-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="df9b0-117">-WorkspaceName</span></span>
<span data-ttu-id="df9b0-118">指定此 Cmdlet 操作之工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="df9b0-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="df9b0-119">-確認</span><span class="sxs-lookup"><span data-stu-id="df9b0-119">-Confirm</span></span>
<span data-ttu-id="df9b0-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="df9b0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df9b0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df9b0-121">-WhatIf</span></span>
<span data-ttu-id="df9b0-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="df9b0-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df9b0-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="df9b0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df9b0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df9b0-124">CommonParameters</span></span>
<span data-ttu-id="df9b0-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="df9b0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df9b0-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="df9b0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df9b0-127">輸入</span><span class="sxs-lookup"><span data-stu-id="df9b0-127">INPUTS</span></span>

### <span data-ttu-id="df9b0-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="df9b0-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="df9b0-129">System.String</span><span class="sxs-lookup"><span data-stu-id="df9b0-129">System.String</span></span>

## <span data-ttu-id="df9b0-130">輸出</span><span class="sxs-lookup"><span data-stu-id="df9b0-130">OUTPUTS</span></span>

### <span data-ttu-id="df9b0-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="df9b0-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="df9b0-132">筆記</span><span class="sxs-lookup"><span data-stu-id="df9b0-132">NOTES</span></span>
* <span data-ttu-id="df9b0-133">關鍵字：azure、azurerm、arm、資源、管理、主管、營運、深入資訊</span><span class="sxs-lookup"><span data-stu-id="df9b0-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="df9b0-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="df9b0-134">RELATED LINKS</span></span>

[<span data-ttu-id="df9b0-135">Disable-AzOperationalInsights</span><span class="sxs-lookup"><span data-stu-id="df9b0-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="df9b0-136">New-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="df9b0-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


