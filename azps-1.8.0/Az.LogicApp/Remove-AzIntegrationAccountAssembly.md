---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: ce3a3ae24a1064e036bc66e0fa7bfdaa6c74e0c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787077"
---
# <span data-ttu-id="316a8-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="316a8-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="316a8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="316a8-102">SYNOPSIS</span></span>
<span data-ttu-id="316a8-103">移除整合帳戶元件。</span><span class="sxs-lookup"><span data-stu-id="316a8-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="316a8-104">句法</span><span class="sxs-lookup"><span data-stu-id="316a8-104">SYNTAX</span></span>

### <span data-ttu-id="316a8-105">ByIntegrationAccount (預設) </span><span class="sxs-lookup"><span data-stu-id="316a8-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="316a8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="316a8-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="316a8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="316a8-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="316a8-108">說明</span><span class="sxs-lookup"><span data-stu-id="316a8-108">DESCRIPTION</span></span>
<span data-ttu-id="316a8-109">**AzIntegrationAccountAssembly** Cmdlet 會將元件從整合帳戶中移除。</span><span class="sxs-lookup"><span data-stu-id="316a8-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="316a8-110">示例</span><span class="sxs-lookup"><span data-stu-id="316a8-110">EXAMPLES</span></span>

### <span data-ttu-id="316a8-111">範例1：使用參數移除元件</span><span class="sxs-lookup"><span data-stu-id="316a8-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="316a8-112">移除集成帳戶 "sampleIntegrationAccount" 中名為 "sampleAssembly" 的元件。</span><span class="sxs-lookup"><span data-stu-id="316a8-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="316a8-113">參數</span><span class="sxs-lookup"><span data-stu-id="316a8-113">PARAMETERS</span></span>

### <span data-ttu-id="316a8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="316a8-114">-DefaultProfile</span></span>
<span data-ttu-id="316a8-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="316a8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="316a8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="316a8-116">-InputObject</span></span>
<span data-ttu-id="316a8-117">整合帳戶元件。</span><span class="sxs-lookup"><span data-stu-id="316a8-117">An integration account assembly.</span></span>

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

### <span data-ttu-id="316a8-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="316a8-118">-Name</span></span>
<span data-ttu-id="316a8-119">整合帳戶元件名稱。</span><span class="sxs-lookup"><span data-stu-id="316a8-119">The integration account assembly name.</span></span>

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

### <span data-ttu-id="316a8-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="316a8-120">-ParentName</span></span>
<span data-ttu-id="316a8-121">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="316a8-121">The integration account name.</span></span>

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

### <span data-ttu-id="316a8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="316a8-122">-PassThru</span></span>
<span data-ttu-id="316a8-123">傳回命令是否成功。</span><span class="sxs-lookup"><span data-stu-id="316a8-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="316a8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="316a8-124">-ResourceGroupName</span></span>
<span data-ttu-id="316a8-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="316a8-125">The resource group name.</span></span>

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

### <span data-ttu-id="316a8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="316a8-126">-ResourceId</span></span>
<span data-ttu-id="316a8-127">整合帳戶元件名稱資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="316a8-127">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="316a8-128">-確認</span><span class="sxs-lookup"><span data-stu-id="316a8-128">-Confirm</span></span>
<span data-ttu-id="316a8-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="316a8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="316a8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="316a8-130">-WhatIf</span></span>
<span data-ttu-id="316a8-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="316a8-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="316a8-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="316a8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="316a8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="316a8-133">CommonParameters</span></span>
<span data-ttu-id="316a8-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="316a8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="316a8-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="316a8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="316a8-136">輸入</span><span class="sxs-lookup"><span data-stu-id="316a8-136">INPUTS</span></span>

### <span data-ttu-id="316a8-137">PSIntegrationAccountAssembly 中的 LogicApp。</span><span class="sxs-lookup"><span data-stu-id="316a8-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="316a8-138">System.object</span><span class="sxs-lookup"><span data-stu-id="316a8-138">System.String</span></span>

## <span data-ttu-id="316a8-139">輸出</span><span class="sxs-lookup"><span data-stu-id="316a8-139">OUTPUTS</span></span>

### <span data-ttu-id="316a8-140">System.object</span><span class="sxs-lookup"><span data-stu-id="316a8-140">System.Boolean</span></span>

## <span data-ttu-id="316a8-141">筆記</span><span class="sxs-lookup"><span data-stu-id="316a8-141">NOTES</span></span>

## <span data-ttu-id="316a8-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="316a8-142">RELATED LINKS</span></span>
