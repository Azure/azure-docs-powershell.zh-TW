---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: d1c61a611b3e2a90c1aa0b0cd21eebdff99ed04b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905386"
---
# <span data-ttu-id="557f0-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="557f0-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="557f0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="557f0-102">SYNOPSIS</span></span>
<span data-ttu-id="557f0-103">移除整合帳戶元件。</span><span class="sxs-lookup"><span data-stu-id="557f0-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="557f0-104">語法</span><span class="sxs-lookup"><span data-stu-id="557f0-104">SYNTAX</span></span>

### <span data-ttu-id="557f0-105">By方Account (預設) </span><span class="sxs-lookup"><span data-stu-id="557f0-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="557f0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="557f0-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="557f0-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="557f0-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="557f0-108">描述</span><span class="sxs-lookup"><span data-stu-id="557f0-108">DESCRIPTION</span></span>
<span data-ttu-id="557f0-109">**Remove-AzAsseAccountAssembly** Cmdlet 會從整合帳戶移除元件。</span><span class="sxs-lookup"><span data-stu-id="557f0-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="557f0-110">例子</span><span class="sxs-lookup"><span data-stu-id="557f0-110">EXAMPLES</span></span>

### <span data-ttu-id="557f0-111">範例 1：根據參數移除元件</span><span class="sxs-lookup"><span data-stu-id="557f0-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="557f0-112">移除名為「sampleAssembly」的程式集，該元件位於整合帳戶"sampleAsseAccount"。</span><span class="sxs-lookup"><span data-stu-id="557f0-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="557f0-113">參數</span><span class="sxs-lookup"><span data-stu-id="557f0-113">PARAMETERS</span></span>

### <span data-ttu-id="557f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="557f0-114">-DefaultProfile</span></span>
<span data-ttu-id="557f0-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="557f0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="557f0-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="557f0-116">-InputObject</span></span>
<span data-ttu-id="557f0-117">整合帳戶元件。</span><span class="sxs-lookup"><span data-stu-id="557f0-117">An integration account assembly.</span></span>

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

### <span data-ttu-id="557f0-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="557f0-118">-Name</span></span>
<span data-ttu-id="557f0-119">整合帳戶元件名稱。</span><span class="sxs-lookup"><span data-stu-id="557f0-119">The integration account assembly name.</span></span>

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

### <span data-ttu-id="557f0-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="557f0-120">-ParentName</span></span>
<span data-ttu-id="557f0-121">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="557f0-121">The integration account name.</span></span>

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

### <span data-ttu-id="557f0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="557f0-122">-PassThru</span></span>
<span data-ttu-id="557f0-123">返回命令是否成功。</span><span class="sxs-lookup"><span data-stu-id="557f0-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="557f0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="557f0-124">-ResourceGroupName</span></span>
<span data-ttu-id="557f0-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="557f0-125">The resource group name.</span></span>

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

### <span data-ttu-id="557f0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="557f0-126">-ResourceId</span></span>
<span data-ttu-id="557f0-127">整合帳戶元件資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="557f0-127">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="557f0-128">-確認</span><span class="sxs-lookup"><span data-stu-id="557f0-128">-Confirm</span></span>
<span data-ttu-id="557f0-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="557f0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="557f0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="557f0-130">-WhatIf</span></span>
<span data-ttu-id="557f0-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="557f0-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="557f0-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="557f0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="557f0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="557f0-133">CommonParameters</span></span>
<span data-ttu-id="557f0-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="557f0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="557f0-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="557f0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="557f0-136">輸入</span><span class="sxs-lookup"><span data-stu-id="557f0-136">INPUTS</span></span>

### <span data-ttu-id="557f0-137">Microsoft.Azure.Commands.LogicApp.models.PSAsseAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="557f0-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="557f0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="557f0-138">System.String</span></span>

## <span data-ttu-id="557f0-139">輸出</span><span class="sxs-lookup"><span data-stu-id="557f0-139">OUTPUTS</span></span>

### <span data-ttu-id="557f0-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="557f0-140">System.Boolean</span></span>

## <span data-ttu-id="557f0-141">筆記</span><span class="sxs-lookup"><span data-stu-id="557f0-141">NOTES</span></span>

## <span data-ttu-id="557f0-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="557f0-142">RELATED LINKS</span></span>
