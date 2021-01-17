---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
ms.openlocfilehash: faf2c40bc43c1b42861bc93d2398d4d26731c112
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448523"
---
# <span data-ttu-id="c4fd1-101">Remove-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="c4fd1-101">Remove-AzSentinelIncident</span></span>

## <span data-ttu-id="c4fd1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4fd1-102">SYNOPSIS</span></span>
<span data-ttu-id="c4fd1-103">刪除事件。</span><span class="sxs-lookup"><span data-stu-id="c4fd1-103">Delete an Incident.</span></span>

## <span data-ttu-id="c4fd1-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4fd1-104">SYNTAX</span></span>

### <span data-ttu-id="c4fd1-105">IncidentId (預設) </span><span class="sxs-lookup"><span data-stu-id="c4fd1-105">IncidentId (Default)</span></span>
```
Remove-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4fd1-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c4fd1-106">InputObject</span></span>
```
Remove-AzSentinelIncident -InputObject <PSSentinelIncident> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4fd1-107">說明</span><span class="sxs-lookup"><span data-stu-id="c4fd1-107">DESCRIPTION</span></span>
<span data-ttu-id="c4fd1-108">**AzSentinelIncident** Cmdlet 會從指定的工作區永久刪除事件。</span><span class="sxs-lookup"><span data-stu-id="c4fd1-108">The **Remove-AzSentinelIncident** cmdlet permanently deletes a Incident from a specified workspace.</span></span>
<span data-ttu-id="c4fd1-109">您可以使用管線運算子傳遞 **Incident** 物件，或者也可以指定所需的參數。</span><span class="sxs-lookup"><span data-stu-id="c4fd1-109">You can pass an **Incident** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="c4fd1-110">您可以使用 Confirm 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c4fd1-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="c4fd1-111">示例</span><span class="sxs-lookup"><span data-stu-id="c4fd1-111">EXAMPLES</span></span>

### <span data-ttu-id="c4fd1-112">範例1</span><span class="sxs-lookup"><span data-stu-id="c4fd1-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="c4fd1-113">這個命令會將事件從工作區移除。</span><span class="sxs-lookup"><span data-stu-id="c4fd1-113">This command removes the Incident from the workspace.</span></span>

## <span data-ttu-id="c4fd1-114">參數</span><span class="sxs-lookup"><span data-stu-id="c4fd1-114">PARAMETERS</span></span>

### <span data-ttu-id="c4fd1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4fd1-115">-DefaultProfile</span></span>
<span data-ttu-id="c4fd1-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4fd1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4fd1-117">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="c4fd1-117">-IncidentId</span></span>
<span data-ttu-id="c4fd1-118">事件 Id。</span><span class="sxs-lookup"><span data-stu-id="c4fd1-118">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fd1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4fd1-119">-InputObject</span></span>
<span data-ttu-id="c4fd1-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="c4fd1-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fd1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4fd1-121">-PassThru</span></span>
<span data-ttu-id="c4fd1-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="c4fd1-122">PassThru</span></span>

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

### <span data-ttu-id="c4fd1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4fd1-123">-ResourceGroupName</span></span>
<span data-ttu-id="c4fd1-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c4fd1-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fd1-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c4fd1-125">-WorkspaceName</span></span>
<span data-ttu-id="c4fd1-126">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="c4fd1-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4fd1-127">-確認</span><span class="sxs-lookup"><span data-stu-id="c4fd1-127">-Confirm</span></span>
<span data-ttu-id="c4fd1-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c4fd1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4fd1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4fd1-129">-WhatIf</span></span>
<span data-ttu-id="c4fd1-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c4fd1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4fd1-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c4fd1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4fd1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4fd1-132">CommonParameters</span></span>
<span data-ttu-id="c4fd1-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c4fd1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4fd1-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c4fd1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4fd1-135">輸入</span><span class="sxs-lookup"><span data-stu-id="c4fd1-135">INPUTS</span></span>

### <span data-ttu-id="c4fd1-136">System.object</span><span class="sxs-lookup"><span data-stu-id="c4fd1-136">System.String</span></span>
### <span data-ttu-id="c4fd1-137">PSSentinelIncident （SecurityInsights）的命令。</span><span class="sxs-lookup"><span data-stu-id="c4fd1-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="c4fd1-138">輸出</span><span class="sxs-lookup"><span data-stu-id="c4fd1-138">OUTPUTS</span></span>

### <span data-ttu-id="c4fd1-139">System.object</span><span class="sxs-lookup"><span data-stu-id="c4fd1-139">System.Boolean</span></span>
## <span data-ttu-id="c4fd1-140">筆記</span><span class="sxs-lookup"><span data-stu-id="c4fd1-140">NOTES</span></span>

## <span data-ttu-id="c4fd1-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4fd1-141">RELATED LINKS</span></span>
