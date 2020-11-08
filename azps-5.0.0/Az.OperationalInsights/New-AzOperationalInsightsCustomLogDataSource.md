---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A08AF7C-1E18-40A1-B21E-12F94823D304
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightscustomlogdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsCustomLogDataSource.md
ms.openlocfilehash: ba33d02ec8c47c91865cc2d0f5549e5f446ca2c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138677"
---
# <span data-ttu-id="e850c-101">New-AzOperationalInsightsCustomLogDataSource</span><span class="sxs-lookup"><span data-stu-id="e850c-101">New-AzOperationalInsightsCustomLogDataSource</span></span>

## <span data-ttu-id="e850c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e850c-102">SYNOPSIS</span></span>
<span data-ttu-id="e850c-103">定義自訂的日誌收集原則。</span><span class="sxs-lookup"><span data-stu-id="e850c-103">Defines a custom log collection policy.</span></span>

## <span data-ttu-id="e850c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e850c-104">SYNTAX</span></span>

### <span data-ttu-id="e850c-105">ByWorkspaceName (預設) </span><span class="sxs-lookup"><span data-stu-id="e850c-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e850c-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="e850c-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsCustomLogDataSource [-Workspace] <PSWorkspace> [-Name] <String>
 [-CustomLogRawJson] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e850c-107">說明</span><span class="sxs-lookup"><span data-stu-id="e850c-107">DESCRIPTION</span></span>
<span data-ttu-id="e850c-108">**新的-AzOperationalInsightsCustomLogDataSource** Cmdlet 定義自訂的記錄集合原則。</span><span class="sxs-lookup"><span data-stu-id="e850c-108">The **New-AzOperationalInsightsCustomLogDataSource** cmdlet defines a custom log collection policy.</span></span>

## <span data-ttu-id="e850c-109">示例</span><span class="sxs-lookup"><span data-stu-id="e850c-109">EXAMPLES</span></span>

## <span data-ttu-id="e850c-110">參數</span><span class="sxs-lookup"><span data-stu-id="e850c-110">PARAMETERS</span></span>

### <span data-ttu-id="e850c-111">-CustomLogRawJson</span><span class="sxs-lookup"><span data-stu-id="e850c-111">-CustomLogRawJson</span></span>
<span data-ttu-id="e850c-112">將自訂集合原則指定為原始 JavaScript 物件符號 (JSON) 字串。</span><span class="sxs-lookup"><span data-stu-id="e850c-112">Specifies the custom collection policy as a raw JavaScript Object Notation (JSON) string.</span></span>

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

### <span data-ttu-id="e850c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e850c-113">-DefaultProfile</span></span>
<span data-ttu-id="e850c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e850c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e850c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e850c-115">-Force</span></span>
<span data-ttu-id="e850c-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e850c-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e850c-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="e850c-117">-Name</span></span>
<span data-ttu-id="e850c-118">指定資料來源的名稱。</span><span class="sxs-lookup"><span data-stu-id="e850c-118">Specifies a name for the data source.</span></span>

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

### <span data-ttu-id="e850c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e850c-119">-ResourceGroupName</span></span>
<span data-ttu-id="e850c-120">指定包含電腦之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e850c-120">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="e850c-121">-工作區</span><span class="sxs-lookup"><span data-stu-id="e850c-121">-Workspace</span></span>
<span data-ttu-id="e850c-122">指定這個 Cmdlet 在其中運作的工作區。</span><span class="sxs-lookup"><span data-stu-id="e850c-122">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e850c-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e850c-123">-WorkspaceName</span></span>
<span data-ttu-id="e850c-124">指定此 Cmdlet 作用中的工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="e850c-124">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="e850c-125">-確認</span><span class="sxs-lookup"><span data-stu-id="e850c-125">-Confirm</span></span>
<span data-ttu-id="e850c-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e850c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e850c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e850c-127">-WhatIf</span></span>
<span data-ttu-id="e850c-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e850c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e850c-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e850c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e850c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e850c-130">CommonParameters</span></span>
<span data-ttu-id="e850c-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e850c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e850c-132">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e850c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e850c-133">輸入</span><span class="sxs-lookup"><span data-stu-id="e850c-133">INPUTS</span></span>

### <span data-ttu-id="e850c-134">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="e850c-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="e850c-135">System.object</span><span class="sxs-lookup"><span data-stu-id="e850c-135">System.String</span></span>

## <span data-ttu-id="e850c-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e850c-136">OUTPUTS</span></span>

### <span data-ttu-id="e850c-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="e850c-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="e850c-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e850c-138">NOTES</span></span>

## <span data-ttu-id="e850c-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e850c-139">RELATED LINKS</span></span>

[<span data-ttu-id="e850c-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="e850c-140">Disable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzOperationalInsightsLinuxCustomLogCollection.md)

[<span data-ttu-id="e850c-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="e850c-141">Enable-AzOperationalInsightsLinuxCustomLogCollection</span></span>](./Enable-AzOperationalInsightsLinuxCustomLogCollection.md)

