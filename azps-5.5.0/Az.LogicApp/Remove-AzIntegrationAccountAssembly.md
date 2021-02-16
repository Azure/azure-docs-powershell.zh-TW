---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 4dceb934f5cf746908c289c7662de0dc3dae09a5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132810"
---
# <span data-ttu-id="450c9-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="450c9-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="450c9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="450c9-102">SYNOPSIS</span></span>
<span data-ttu-id="450c9-103">移除整合帳戶元件。</span><span class="sxs-lookup"><span data-stu-id="450c9-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="450c9-104">句法</span><span class="sxs-lookup"><span data-stu-id="450c9-104">SYNTAX</span></span>

### <span data-ttu-id="450c9-105">ByIntegrationAccount (預設) </span><span class="sxs-lookup"><span data-stu-id="450c9-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="450c9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="450c9-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="450c9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="450c9-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="450c9-108">說明</span><span class="sxs-lookup"><span data-stu-id="450c9-108">DESCRIPTION</span></span>
<span data-ttu-id="450c9-109">**AzIntegrationAccountAssembly** Cmdlet 會將元件從整合帳戶中移除。</span><span class="sxs-lookup"><span data-stu-id="450c9-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="450c9-110">示例</span><span class="sxs-lookup"><span data-stu-id="450c9-110">EXAMPLES</span></span>

### <span data-ttu-id="450c9-111">範例1：使用參數移除元件</span><span class="sxs-lookup"><span data-stu-id="450c9-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="450c9-112">移除集成帳戶 "sampleIntegrationAccount" 中名為 "sampleAssembly" 的元件。</span><span class="sxs-lookup"><span data-stu-id="450c9-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="450c9-113">參數</span><span class="sxs-lookup"><span data-stu-id="450c9-113">PARAMETERS</span></span>

### <span data-ttu-id="450c9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="450c9-114">-DefaultProfile</span></span>
<span data-ttu-id="450c9-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="450c9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="450c9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="450c9-116">-InputObject</span></span>
<span data-ttu-id="450c9-117">整合帳戶元件。</span><span class="sxs-lookup"><span data-stu-id="450c9-117">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="450c9-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="450c9-118">-Name</span></span>
<span data-ttu-id="450c9-119">整合帳戶元件名稱。</span><span class="sxs-lookup"><span data-stu-id="450c9-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="450c9-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="450c9-120">-ParentName</span></span>
<span data-ttu-id="450c9-121">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="450c9-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="450c9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="450c9-122">-PassThru</span></span>
<span data-ttu-id="450c9-123">傳回命令是否成功。</span><span class="sxs-lookup"><span data-stu-id="450c9-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="450c9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="450c9-124">-ResourceGroupName</span></span>
<span data-ttu-id="450c9-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="450c9-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="450c9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="450c9-126">-ResourceId</span></span>
<span data-ttu-id="450c9-127">整合帳戶元件名稱資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="450c9-127">The integration account assembly resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="450c9-128">-確認</span><span class="sxs-lookup"><span data-stu-id="450c9-128">-Confirm</span></span>
<span data-ttu-id="450c9-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="450c9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="450c9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="450c9-130">-WhatIf</span></span>
<span data-ttu-id="450c9-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="450c9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="450c9-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="450c9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="450c9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="450c9-133">CommonParameters</span></span>
<span data-ttu-id="450c9-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="450c9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="450c9-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="450c9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="450c9-136">輸入</span><span class="sxs-lookup"><span data-stu-id="450c9-136">INPUTS</span></span>

### <span data-ttu-id="450c9-137">PSIntegrationAccountAssembly 中的 LogicApp。</span><span class="sxs-lookup"><span data-stu-id="450c9-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="450c9-138">System.object</span><span class="sxs-lookup"><span data-stu-id="450c9-138">System.String</span></span>

## <span data-ttu-id="450c9-139">輸出</span><span class="sxs-lookup"><span data-stu-id="450c9-139">OUTPUTS</span></span>

### <span data-ttu-id="450c9-140">System.object</span><span class="sxs-lookup"><span data-stu-id="450c9-140">System.Boolean</span></span>

## <span data-ttu-id="450c9-141">筆記</span><span class="sxs-lookup"><span data-stu-id="450c9-141">NOTES</span></span>

## <span data-ttu-id="450c9-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="450c9-142">RELATED LINKS</span></span>
