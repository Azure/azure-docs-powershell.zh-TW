---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: bd5e51b8951d2b246036b45ddddf3d1bbe4b8e4e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969361"
---
# <span data-ttu-id="2c165-101">Remove-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c165-101">Remove-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="2c165-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2c165-102">SYNOPSIS</span></span>
<span data-ttu-id="2c165-103">移除 azure 自動化軟體更新設定。</span><span class="sxs-lookup"><span data-stu-id="2c165-103">Removes an azure automation software update configuration.</span></span>

## <span data-ttu-id="2c165-104">句法</span><span class="sxs-lookup"><span data-stu-id="2c165-104">SYNTAX</span></span>

### <span data-ttu-id="2c165-105">BySucName (預設) </span><span class="sxs-lookup"><span data-stu-id="2c165-105">BySucName (Default)</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -Name <String> [-PassThru] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c165-106">BySuc</span><span class="sxs-lookup"><span data-stu-id="2c165-106">BySuc</span></span>
```
Remove-AzAutomationSoftwareUpdateConfiguration -SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>
 [-PassThru] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c165-107">說明</span><span class="sxs-lookup"><span data-stu-id="2c165-107">DESCRIPTION</span></span>
<span data-ttu-id="2c165-108">這個 Cmdlet 移除了 azure 自動化軟體更新設定。</span><span class="sxs-lookup"><span data-stu-id="2c165-108">This cmdlet removed an azure automation software update configuration.</span></span>

## <span data-ttu-id="2c165-109">示例</span><span class="sxs-lookup"><span data-stu-id="2c165-109">EXAMPLES</span></span>

### <span data-ttu-id="2c165-110">範例1</span><span class="sxs-lookup"><span data-stu-id="2c165-110">Example 1</span></span>
<span data-ttu-id="2c165-111">這個範例示範如何從自動化帳戶中移除「MyUpdateConfiguration」</span><span class="sxs-lookup"><span data-stu-id="2c165-111">This example shows how to remove 'MyUpdateConfiguration' from automation account</span></span>

```powershell
PS C:\> Remove-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyUpdateConfiguration"
```

## <span data-ttu-id="2c165-112">參數</span><span class="sxs-lookup"><span data-stu-id="2c165-112">PARAMETERS</span></span>

### <span data-ttu-id="2c165-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2c165-113">-AutomationAccountName</span></span>
<span data-ttu-id="2c165-114">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2c165-114">The automation account name.</span></span>

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

### <span data-ttu-id="2c165-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c165-115">-DefaultProfile</span></span>
<span data-ttu-id="2c165-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c165-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c165-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="2c165-117">-Name</span></span>
<span data-ttu-id="2c165-118">要移除的軟體更新配置名稱。</span><span class="sxs-lookup"><span data-stu-id="2c165-118">Name of the software update configuration to remove.</span></span>

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

### <span data-ttu-id="2c165-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c165-119">-PassThru</span></span>
<span data-ttu-id="2c165-120">PassThru 會傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="2c165-120">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="2c165-121">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="2c165-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2c165-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c165-122">-ResourceGroupName</span></span>
<span data-ttu-id="2c165-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c165-123">The resource group name.</span></span>

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

### <span data-ttu-id="2c165-124">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c165-124">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="2c165-125">要移除的軟體更新設定。</span><span class="sxs-lookup"><span data-stu-id="2c165-125">The software update configuration to remove.</span></span>

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

### <span data-ttu-id="2c165-126">-確認</span><span class="sxs-lookup"><span data-stu-id="2c165-126">-Confirm</span></span>
<span data-ttu-id="2c165-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2c165-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c165-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c165-128">-WhatIf</span></span>
<span data-ttu-id="2c165-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2c165-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c165-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2c165-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c165-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c165-131">CommonParameters</span></span>
<span data-ttu-id="2c165-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2c165-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c165-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2c165-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c165-134">輸入</span><span class="sxs-lookup"><span data-stu-id="2c165-134">INPUTS</span></span>

### <span data-ttu-id="2c165-135">System.object</span><span class="sxs-lookup"><span data-stu-id="2c165-135">System.String</span></span>

### <span data-ttu-id="2c165-136">UpdateManagement SoftwareUpdateConfiguration 中的 []</span><span class="sxs-lookup"><span data-stu-id="2c165-136">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="2c165-137">輸出</span><span class="sxs-lookup"><span data-stu-id="2c165-137">OUTPUTS</span></span>

### <span data-ttu-id="2c165-138">System.void</span><span class="sxs-lookup"><span data-stu-id="2c165-138">System.Void</span></span>

### <span data-ttu-id="2c165-139">System.object</span><span class="sxs-lookup"><span data-stu-id="2c165-139">System.Boolean</span></span>

## <span data-ttu-id="2c165-140">筆記</span><span class="sxs-lookup"><span data-stu-id="2c165-140">NOTES</span></span>

## <span data-ttu-id="2c165-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c165-141">RELATED LINKS</span></span>
