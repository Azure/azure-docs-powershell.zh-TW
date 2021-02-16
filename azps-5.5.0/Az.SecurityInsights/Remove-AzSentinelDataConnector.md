---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelDataConnector.md
ms.openlocfilehash: 19e9dd843cd428a65b371ae933d00c58233de35b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139867"
---
# <span data-ttu-id="d9008-101">Remove-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="d9008-101">Remove-AzSentinelDataConnector</span></span>

## <span data-ttu-id="d9008-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d9008-102">SYNOPSIS</span></span>
<span data-ttu-id="d9008-103">移除資料連線器。</span><span class="sxs-lookup"><span data-stu-id="d9008-103">Remove a Data Connector.</span></span>

## <span data-ttu-id="d9008-104">句法</span><span class="sxs-lookup"><span data-stu-id="d9008-104">SYNTAX</span></span>

### <span data-ttu-id="d9008-105">DataConnectorId (預設) </span><span class="sxs-lookup"><span data-stu-id="d9008-105">DataConnectorId (Default)</span></span>
```
Remove-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9008-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d9008-106">InputObject</span></span>
```
Remove-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9008-107">說明</span><span class="sxs-lookup"><span data-stu-id="d9008-107">DESCRIPTION</span></span>
<span data-ttu-id="d9008-108">**AzSentinelDataConnector** Cmdlet 會將資料連線器從指定的工作區永久刪除。</span><span class="sxs-lookup"><span data-stu-id="d9008-108">The **Remove-AzSentinelDataConnector** cmdlet permanently deletes a Data Connector from a specified workspace.</span></span>
<span data-ttu-id="d9008-109">您可以使用管線運算子傳遞 **DataConnector** 物件，或者也可以指定所需的參數。</span><span class="sxs-lookup"><span data-stu-id="d9008-109">You can pass an **DataConnector** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="d9008-110">您可以使用 Confirm 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d9008-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="d9008-111">示例</span><span class="sxs-lookup"><span data-stu-id="d9008-111">EXAMPLES</span></span>

### <span data-ttu-id="d9008-112">範例1</span><span class="sxs-lookup"><span data-stu-id="d9008-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId"
```

<span data-ttu-id="d9008-113">這個命令會從工作區移除 DataConnector。</span><span class="sxs-lookup"><span data-stu-id="d9008-113">This command removes the DataConnector from the workspace.</span></span>

## <span data-ttu-id="d9008-114">參數</span><span class="sxs-lookup"><span data-stu-id="d9008-114">PARAMETERS</span></span>

### <span data-ttu-id="d9008-115">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="d9008-115">-DataConnectorId</span></span>
<span data-ttu-id="d9008-116">資料連線器識別碼。</span><span class="sxs-lookup"><span data-stu-id="d9008-116">Data Connector Id.</span></span>

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

### <span data-ttu-id="d9008-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9008-117">-DefaultProfile</span></span>
<span data-ttu-id="d9008-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d9008-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9008-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9008-119">-InputObject</span></span>
<span data-ttu-id="d9008-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="d9008-120">InputObject.</span></span>

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

### <span data-ttu-id="d9008-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9008-121">-PassThru</span></span>
<span data-ttu-id="d9008-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="d9008-122">PassThru</span></span>

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

### <span data-ttu-id="d9008-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9008-123">-ResourceGroupName</span></span>
<span data-ttu-id="d9008-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d9008-124">Resource group name.</span></span>

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

### <span data-ttu-id="d9008-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d9008-125">-WorkspaceName</span></span>
<span data-ttu-id="d9008-126">工作區名稱。</span><span class="sxs-lookup"><span data-stu-id="d9008-126">Workspace Name.</span></span>

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

### <span data-ttu-id="d9008-127">-確認</span><span class="sxs-lookup"><span data-stu-id="d9008-127">-Confirm</span></span>
<span data-ttu-id="d9008-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d9008-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9008-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9008-129">-WhatIf</span></span>
<span data-ttu-id="d9008-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d9008-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9008-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d9008-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9008-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9008-132">CommonParameters</span></span>
<span data-ttu-id="d9008-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d9008-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9008-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d9008-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9008-135">輸入</span><span class="sxs-lookup"><span data-stu-id="d9008-135">INPUTS</span></span>

### <span data-ttu-id="d9008-136">System.object</span><span class="sxs-lookup"><span data-stu-id="d9008-136">System.String</span></span>
### <span data-ttu-id="d9008-137">SecurityInsights DataConnectors. PSSentinelDataConnector （）</span><span class="sxs-lookup"><span data-stu-id="d9008-137">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="d9008-138">輸出</span><span class="sxs-lookup"><span data-stu-id="d9008-138">OUTPUTS</span></span>

### <span data-ttu-id="d9008-139">SecurityInsights DataConnectors. PSSentinelDataConnector （）</span><span class="sxs-lookup"><span data-stu-id="d9008-139">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="d9008-140">筆記</span><span class="sxs-lookup"><span data-stu-id="d9008-140">NOTES</span></span>

## <span data-ttu-id="d9008-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="d9008-141">RELATED LINKS</span></span>
