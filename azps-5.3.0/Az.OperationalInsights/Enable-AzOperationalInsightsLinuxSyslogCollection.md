---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 66DD5919-B6B7-4FE5-B45B-937013549882
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/enable-azoperationalinsightslinuxsyslogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Enable-AzOperationalInsightsLinuxSyslogCollection.md
ms.openlocfilehash: d609ee8910a1dc016365d126b61bc1f4820e977c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98450085"
---
# <span data-ttu-id="f1ca7-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="f1ca7-101">Enable-AzOperationalInsightsLinuxSyslogCollection</span></span>

## <span data-ttu-id="f1ca7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1ca7-102">SYNOPSIS</span></span>
<span data-ttu-id="f1ca7-103">從 Linux 電腦開始收集 syslog 資料。</span><span class="sxs-lookup"><span data-stu-id="f1ca7-103">Starts collection of syslog data from Linux computers.</span></span>

## <span data-ttu-id="f1ca7-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1ca7-104">SYNTAX</span></span>

### <span data-ttu-id="f1ca7-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="f1ca7-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1ca7-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f1ca7-106">ByWorkspaceObject</span></span>
```
Enable-AzOperationalInsightsLinuxSyslogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1ca7-107">說明</span><span class="sxs-lookup"><span data-stu-id="f1ca7-107">DESCRIPTION</span></span>
<span data-ttu-id="f1ca7-108">**AzOperationalInsightsLinuxSyslogCollection** Cmdlet 會在工作區中從連線的 Linux 電腦開始收集 syslog 資料。</span><span class="sxs-lookup"><span data-stu-id="f1ca7-108">The **Enable-AzOperationalInsightsLinuxSyslogCollection** cmdlet starts collection of syslog data from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="f1ca7-109">示例</span><span class="sxs-lookup"><span data-stu-id="f1ca7-109">EXAMPLES</span></span>

## <span data-ttu-id="f1ca7-110">參數</span><span class="sxs-lookup"><span data-stu-id="f1ca7-110">PARAMETERS</span></span>

### <span data-ttu-id="f1ca7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1ca7-111">-DefaultProfile</span></span>
<span data-ttu-id="f1ca7-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f1ca7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1ca7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1ca7-113">-ResourceGroupName</span></span>
<span data-ttu-id="f1ca7-114">指定包含 Linux 電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f1ca7-114">Specifies the name of a resource group that contains Linux computers.</span></span>

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

### <span data-ttu-id="f1ca7-115">-工作區</span><span class="sxs-lookup"><span data-stu-id="f1ca7-115">-Workspace</span></span>
<span data-ttu-id="f1ca7-116">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="f1ca7-116">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f1ca7-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f1ca7-117">-WorkspaceName</span></span>
<span data-ttu-id="f1ca7-118">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="f1ca7-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="f1ca7-119">-確認</span><span class="sxs-lookup"><span data-stu-id="f1ca7-119">-Confirm</span></span>
<span data-ttu-id="f1ca7-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1ca7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1ca7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1ca7-121">-WhatIf</span></span>
<span data-ttu-id="f1ca7-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1ca7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1ca7-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1ca7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1ca7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1ca7-124">CommonParameters</span></span>
<span data-ttu-id="f1ca7-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1ca7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1ca7-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f1ca7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1ca7-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f1ca7-127">INPUTS</span></span>

### <span data-ttu-id="f1ca7-128">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="f1ca7-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="f1ca7-129">System.object</span><span class="sxs-lookup"><span data-stu-id="f1ca7-129">System.String</span></span>

## <span data-ttu-id="f1ca7-130">輸出</span><span class="sxs-lookup"><span data-stu-id="f1ca7-130">OUTPUTS</span></span>

### <span data-ttu-id="f1ca7-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="f1ca7-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="f1ca7-132">筆記</span><span class="sxs-lookup"><span data-stu-id="f1ca7-132">NOTES</span></span>
* <span data-ttu-id="f1ca7-133">關鍵字： azure，azurerm，arm，資源，管理，管理員，作業，洞察力</span><span class="sxs-lookup"><span data-stu-id="f1ca7-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="f1ca7-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1ca7-134">RELATED LINKS</span></span>

[<span data-ttu-id="f1ca7-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span><span class="sxs-lookup"><span data-stu-id="f1ca7-135">Disable-AzOperationalInsightsLinuxSyslogCollection</span></span>](./Disable-AzOperationalInsightsLinuxSyslogCollection.md)

[<span data-ttu-id="f1ca7-136">新-AzOperationalInsightsLinuxSyslogDataSource</span><span class="sxs-lookup"><span data-stu-id="f1ca7-136">New-AzOperationalInsightsLinuxSyslogDataSource</span></span>](./New-AzOperationalInsightsLinuxSyslogDataSource.md)


