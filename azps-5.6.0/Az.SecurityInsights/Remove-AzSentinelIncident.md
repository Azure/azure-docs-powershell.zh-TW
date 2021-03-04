---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
ms.openlocfilehash: 80badb2e73aa00fd9a221c20372ab42499c1cb0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906397"
---
# <span data-ttu-id="9cfd4-101">Remove-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="9cfd4-101">Remove-AzSentinelIncident</span></span>

## <span data-ttu-id="9cfd4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9cfd4-102">SYNOPSIS</span></span>
<span data-ttu-id="9cfd4-103">刪除事件。</span><span class="sxs-lookup"><span data-stu-id="9cfd4-103">Delete an Incident.</span></span>

## <span data-ttu-id="9cfd4-104">語法</span><span class="sxs-lookup"><span data-stu-id="9cfd4-104">SYNTAX</span></span>

### <span data-ttu-id="9cfd4-105">IncidentId (預設) </span><span class="sxs-lookup"><span data-stu-id="9cfd4-105">IncidentId (Default)</span></span>
```
Remove-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cfd4-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9cfd4-106">InputObject</span></span>
```
Remove-AzSentinelIncident -InputObject <PSSentinelIncident> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cfd4-107">描述</span><span class="sxs-lookup"><span data-stu-id="9cfd4-107">DESCRIPTION</span></span>
<span data-ttu-id="9cfd4-108">**Remove-AzSentinelIncident** Cmdlet 會永久刪除指定工作區中的事件。</span><span class="sxs-lookup"><span data-stu-id="9cfd4-108">The **Remove-AzSentinelIncident** cmdlet permanently deletes a Incident from a specified workspace.</span></span>
<span data-ttu-id="9cfd4-109">您可以使用管線運算子傳遞 **事件** 物件，或者您也可以指定所需的參數。</span><span class="sxs-lookup"><span data-stu-id="9cfd4-109">You can pass an **Incident** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="9cfd4-110">您可以使用確認參數$ConfirmPreference Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9cfd4-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="9cfd4-111">例子</span><span class="sxs-lookup"><span data-stu-id="9cfd4-111">EXAMPLES</span></span>

### <span data-ttu-id="9cfd4-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="9cfd4-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="9cfd4-113">此命令會從工作區移除事件。</span><span class="sxs-lookup"><span data-stu-id="9cfd4-113">This command removes the Incident from the workspace.</span></span>

## <span data-ttu-id="9cfd4-114">參數</span><span class="sxs-lookup"><span data-stu-id="9cfd4-114">PARAMETERS</span></span>

### <span data-ttu-id="9cfd4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cfd4-115">-DefaultProfile</span></span>
<span data-ttu-id="9cfd4-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9cfd4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cfd4-117">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="9cfd4-117">-IncidentId</span></span>
<span data-ttu-id="9cfd4-118">事件識別碼。</span><span class="sxs-lookup"><span data-stu-id="9cfd4-118">Incident Id.</span></span>

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

### <span data-ttu-id="9cfd4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9cfd4-119">-InputObject</span></span>
<span data-ttu-id="9cfd4-120">InputObject。</span><span class="sxs-lookup"><span data-stu-id="9cfd4-120">InputObject.</span></span>

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

### <span data-ttu-id="9cfd4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9cfd4-121">-PassThru</span></span>
<span data-ttu-id="9cfd4-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="9cfd4-122">PassThru</span></span>

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

### <span data-ttu-id="9cfd4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cfd4-123">-ResourceGroupName</span></span>
<span data-ttu-id="9cfd4-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="9cfd4-124">Resource group name.</span></span>

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

### <span data-ttu-id="9cfd4-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9cfd4-125">-WorkspaceName</span></span>
<span data-ttu-id="9cfd4-126">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="9cfd4-126">Workspace Name.</span></span>

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

### <span data-ttu-id="9cfd4-127">-確認</span><span class="sxs-lookup"><span data-stu-id="9cfd4-127">-Confirm</span></span>
<span data-ttu-id="9cfd4-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9cfd4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cfd4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cfd4-129">-WhatIf</span></span>
<span data-ttu-id="9cfd4-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9cfd4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cfd4-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9cfd4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cfd4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cfd4-132">CommonParameters</span></span>
<span data-ttu-id="9cfd4-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9cfd4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cfd4-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9cfd4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cfd4-135">輸入</span><span class="sxs-lookup"><span data-stu-id="9cfd4-135">INPUTS</span></span>

### <span data-ttu-id="9cfd4-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9cfd4-136">System.String</span></span>
### <span data-ttu-id="9cfd4-137">Microsoft.Azure.Commands.SecurityInsights.models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="9cfd4-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="9cfd4-138">輸出</span><span class="sxs-lookup"><span data-stu-id="9cfd4-138">OUTPUTS</span></span>

### <span data-ttu-id="9cfd4-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9cfd4-139">System.Boolean</span></span>
## <span data-ttu-id="9cfd4-140">筆記</span><span class="sxs-lookup"><span data-stu-id="9cfd4-140">NOTES</span></span>

## <span data-ttu-id="9cfd4-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="9cfd4-141">RELATED LINKS</span></span>
