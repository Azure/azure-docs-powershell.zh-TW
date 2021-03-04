---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
ms.openlocfilehash: d9dc64124dd4840227b692e2ef21842a19b4adeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908454"
---
# <span data-ttu-id="6f951-101">Remove-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="6f951-101">Remove-AzSentinelDataConnector</span></span>

## <span data-ttu-id="6f951-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6f951-102">SYNOPSIS</span></span>
<span data-ttu-id="6f951-103">移除資料連線器。</span><span class="sxs-lookup"><span data-stu-id="6f951-103">Remove a Data Connector.</span></span>

## <span data-ttu-id="6f951-104">語法</span><span class="sxs-lookup"><span data-stu-id="6f951-104">SYNTAX</span></span>

### <span data-ttu-id="6f951-105">DataConnectorId (預設) </span><span class="sxs-lookup"><span data-stu-id="6f951-105">DataConnectorId (Default)</span></span>
```
Remove-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f951-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6f951-106">InputObject</span></span>
```
Remove-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f951-107">描述</span><span class="sxs-lookup"><span data-stu-id="6f951-107">DESCRIPTION</span></span>
<span data-ttu-id="6f951-108">**Remove-AzSentinelDataConnector** Cmdlet 會永久刪除指定工作區的資料連線器。</span><span class="sxs-lookup"><span data-stu-id="6f951-108">The **Remove-AzSentinelDataConnector** cmdlet permanently deletes a Data Connector from a specified workspace.</span></span>
<span data-ttu-id="6f951-109">您可以使用管線運算子傳遞 **DataConnector** 物件，或者您也可以指定所需的參數。</span><span class="sxs-lookup"><span data-stu-id="6f951-109">You can pass an **DataConnector** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="6f951-110">您可以使用確認參數$ConfirmPreference Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6f951-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="6f951-111">例子</span><span class="sxs-lookup"><span data-stu-id="6f951-111">EXAMPLES</span></span>

### <span data-ttu-id="6f951-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="6f951-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="6f951-113">此命令會從工作區移除 DataConnector。</span><span class="sxs-lookup"><span data-stu-id="6f951-113">This command removes the DataConnector from the workspace.</span></span>

## <span data-ttu-id="6f951-114">參數</span><span class="sxs-lookup"><span data-stu-id="6f951-114">PARAMETERS</span></span>

### <span data-ttu-id="6f951-115">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="6f951-115">-DataConnectorId</span></span>
<span data-ttu-id="6f951-116">資料連線器識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f951-116">Data Connector Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f951-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f951-117">-DefaultProfile</span></span>
<span data-ttu-id="6f951-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f951-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f951-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f951-119">-InputObject</span></span>
<span data-ttu-id="6f951-120">InputObject。</span><span class="sxs-lookup"><span data-stu-id="6f951-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f951-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6f951-121">-PassThru</span></span>
<span data-ttu-id="6f951-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="6f951-122">PassThru</span></span>

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

### <span data-ttu-id="6f951-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f951-123">-ResourceGroupName</span></span>
<span data-ttu-id="6f951-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="6f951-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f951-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6f951-125">-WorkspaceName</span></span>
<span data-ttu-id="6f951-126">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="6f951-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f951-127">-確認</span><span class="sxs-lookup"><span data-stu-id="6f951-127">-Confirm</span></span>
<span data-ttu-id="6f951-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6f951-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f951-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f951-129">-WhatIf</span></span>
<span data-ttu-id="6f951-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f951-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f951-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f951-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f951-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f951-132">CommonParameters</span></span>
<span data-ttu-id="6f951-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6f951-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f951-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f951-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f951-135">輸入</span><span class="sxs-lookup"><span data-stu-id="6f951-135">INPUTS</span></span>

### <span data-ttu-id="6f951-136">System.String</span><span class="sxs-lookup"><span data-stu-id="6f951-136">System.String</span></span>
### <span data-ttu-id="6f951-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="6f951-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="6f951-138">輸出</span><span class="sxs-lookup"><span data-stu-id="6f951-138">OUTPUTS</span></span>

### <span data-ttu-id="6f951-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="6f951-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="6f951-140">筆記</span><span class="sxs-lookup"><span data-stu-id="6f951-140">NOTES</span></span>

## <span data-ttu-id="6f951-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f951-141">RELATED LINKS</span></span>
