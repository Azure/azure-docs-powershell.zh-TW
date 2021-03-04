---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: 8ddc84e3fac5df9253ffdacb61d4f4c7a5568c6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903362"
---
# <span data-ttu-id="92691-101">Remove-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="92691-101">Remove-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="92691-102">簡介</span><span class="sxs-lookup"><span data-stu-id="92691-102">SYNOPSIS</span></span>
<span data-ttu-id="92691-103">移除 Azure 自動化軟體更新組配置。</span><span class="sxs-lookup"><span data-stu-id="92691-103">Removes an azure automation software update configuration.</span></span>

## <span data-ttu-id="92691-104">語法</span><span class="sxs-lookup"><span data-stu-id="92691-104">SYNTAX</span></span>

### <span data-ttu-id="92691-105">BySucName (預設) </span><span class="sxs-lookup"><span data-stu-id="92691-105">BySucName (Default)</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="92691-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="92691-106">BySuc</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92691-107">描述</span><span class="sxs-lookup"><span data-stu-id="92691-107">DESCRIPTION</span></span>
<span data-ttu-id="92691-108">此 Cmdlet 已移除 Azure 自動化軟體更新組配置。</span><span class="sxs-lookup"><span data-stu-id="92691-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="92691-109">例子</span><span class="sxs-lookup"><span data-stu-id="92691-109">EXAMPLES</span></span>

### <span data-ttu-id="92691-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="92691-110">Example 1</span></span>
<span data-ttu-id="92691-111">此範例顯示如何從自動化帳戶移除 "MyUpdateConfiguration"</span><span class="sxs-lookup"><span data-stu-id="92691-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="92691-112">參數</span><span class="sxs-lookup"><span data-stu-id="92691-112">PARAMETERS</span></span>

### <span data-ttu-id="92691-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="92691-113">-AutomationAccountName</span></span>
<span data-ttu-id="92691-114">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="92691-114">The automation account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92691-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92691-115">-DefaultProfile</span></span>
<span data-ttu-id="92691-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="92691-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92691-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="92691-117">-Name</span></span>
<span data-ttu-id="92691-118">要移除的軟體更新組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="92691-118">Name of the software update configuration to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92691-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92691-119">-PassThru</span></span>
<span data-ttu-id="92691-120">PassThru 會傳回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="92691-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="92691-121">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="92691-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="92691-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92691-122">-ResourceGroupName</span></span>
<span data-ttu-id="92691-123">資源組名。</span><span class="sxs-lookup"><span data-stu-id="92691-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92691-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="92691-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="92691-125">要移除的軟體更新組配置。</span><span class="sxs-lookup"><span data-stu-id="92691-125">The software update configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92691-126">-確認</span><span class="sxs-lookup"><span data-stu-id="92691-126">-Confirm</span></span>
<span data-ttu-id="92691-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="92691-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92691-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92691-128">-WhatIf</span></span>
<span data-ttu-id="92691-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="92691-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92691-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="92691-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92691-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92691-131">CommonParameters</span></span>
<span data-ttu-id="92691-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="92691-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92691-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="92691-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92691-134">輸入</span><span class="sxs-lookup"><span data-stu-id="92691-134">INPUTS</span></span>

### <span data-ttu-id="92691-135">System.String</span><span class="sxs-lookup"><span data-stu-id="92691-135">System.String</span></span>

### <span data-ttu-id="92691-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="92691-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="92691-137">輸出</span><span class="sxs-lookup"><span data-stu-id="92691-137">OUTPUTS</span></span>

### <span data-ttu-id="92691-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="92691-138">System.Void</span></span>

### <span data-ttu-id="92691-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="92691-139">System.Boolean</span></span>

## <span data-ttu-id="92691-140">筆記</span><span class="sxs-lookup"><span data-stu-id="92691-140">NOTES</span></span>

## <span data-ttu-id="92691-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="92691-141">RELATED LINKS</span></span>
