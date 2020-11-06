---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/update-azautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Update-AzAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Update-AzAutomationSourceControl.md
ms.openlocfilehash: 7786431232f9570557593d2fbdde65a21e34f9bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613651"
---
# <span data-ttu-id="e8ff8-101">Update-AzAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="e8ff8-101">Update-AzAutomationSourceControl</span></span>

## <span data-ttu-id="e8ff8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e8ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="e8ff8-103">更新 Azure 自動化來源控制。</span><span class="sxs-lookup"><span data-stu-id="e8ff8-103">Updates an Azure Automation source control.</span></span>

## <span data-ttu-id="e8ff8-104">句法</span><span class="sxs-lookup"><span data-stu-id="e8ff8-104">SYNTAX</span></span>

```
Update-AzAutomationSourceControl -Name <String> [-AccessToken <SecureString>] [-FolderPath <String>]
 [-Branch <String>] [-Description <String>] [-AutoSync <Boolean>] [-PublishRunbook <Boolean>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8ff8-105">說明</span><span class="sxs-lookup"><span data-stu-id="e8ff8-105">DESCRIPTION</span></span>
<span data-ttu-id="e8ff8-106">Update-AzAutomationSourceControl Cmdlet 會修改 Azure 自動化中來源控制項中欄位的值。</span><span class="sxs-lookup"><span data-stu-id="e8ff8-106">The Update-AzAutomationSourceControl cmdlet modifies the value of a field in a source control in Azure Automation.</span></span>

## <span data-ttu-id="e8ff8-107">示例</span><span class="sxs-lookup"><span data-stu-id="e8ff8-107">EXAMPLES</span></span>

### <span data-ttu-id="e8ff8-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e8ff8-108">Example 1</span></span>
<span data-ttu-id="e8ff8-109">這個命令會將在名為 devAccount 的帳戶中名為 VSTSNative 的 Azure 自動化來源控制項的 PublishRunbook 欄位設為 false。</span><span class="sxs-lookup"><span data-stu-id="e8ff8-109">This commands sets the PublishRunbook field to false for the Azure Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
Update-AzAutomationSourceControl -ResourceGroupName "rg1" `
                                      -AutomationAccountName "devAccount" `
                                      -Name "VSTSNative" `
                                      -PublishRunbook $false 

Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    False          https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="e8ff8-110">參數</span><span class="sxs-lookup"><span data-stu-id="e8ff8-110">PARAMETERS</span></span>

### <span data-ttu-id="e8ff8-111">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="e8ff8-111">-AccessToken</span></span>
<span data-ttu-id="e8ff8-112">來源控制項存取權杖。</span><span class="sxs-lookup"><span data-stu-id="e8ff8-112">The source control access token.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ff8-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e8ff8-113">-AutomationAccountName</span></span>
<span data-ttu-id="e8ff8-114">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e8ff8-114">The automation account name.</span></span>

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

### <span data-ttu-id="e8ff8-115">-AutoSync</span><span class="sxs-lookup"><span data-stu-id="e8ff8-115">-AutoSync</span></span>
<span data-ttu-id="e8ff8-116">來源控制項的 autoSync 屬性。</span><span class="sxs-lookup"><span data-stu-id="e8ff8-116">The autoSync property for the source control.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ff8-117">-分支</span><span class="sxs-lookup"><span data-stu-id="e8ff8-117">-Branch</span></span>
<span data-ttu-id="e8ff8-118">來源控制項分支。</span><span class="sxs-lookup"><span data-stu-id="e8ff8-118">The source control branch.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ff8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8ff8-119">-DefaultProfile</span></span>
<span data-ttu-id="e8ff8-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8ff8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8ff8-121">-描述</span><span class="sxs-lookup"><span data-stu-id="e8ff8-121">-Description</span></span>
<span data-ttu-id="e8ff8-122">來源控制項描述。</span><span class="sxs-lookup"><span data-stu-id="e8ff8-122">The source control description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ff8-123">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="e8ff8-123">-FolderPath</span></span>
<span data-ttu-id="e8ff8-124">[來源] 控制資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="e8ff8-124">The source control folder path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ff8-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8ff8-125">-Name</span></span>
<span data-ttu-id="e8ff8-126">來源控制項名稱。</span><span class="sxs-lookup"><span data-stu-id="e8ff8-126">The source control name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8ff8-127">-PublishRunbook</span><span class="sxs-lookup"><span data-stu-id="e8ff8-127">-PublishRunbook</span></span>
<span data-ttu-id="e8ff8-128">來源控制項的 publishRunbook 屬性。</span><span class="sxs-lookup"><span data-stu-id="e8ff8-128">The publishRunbook property of the source control.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8ff8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8ff8-129">-ResourceGroupName</span></span>
<span data-ttu-id="e8ff8-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e8ff8-130">The resource group name.</span></span>

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

### <span data-ttu-id="e8ff8-131">-確認</span><span class="sxs-lookup"><span data-stu-id="e8ff8-131">-Confirm</span></span>
<span data-ttu-id="e8ff8-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e8ff8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8ff8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8ff8-133">-WhatIf</span></span>
<span data-ttu-id="e8ff8-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e8ff8-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8ff8-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e8ff8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8ff8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8ff8-136">CommonParameters</span></span>
<span data-ttu-id="e8ff8-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e8ff8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8ff8-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e8ff8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8ff8-139">輸入</span><span class="sxs-lookup"><span data-stu-id="e8ff8-139">INPUTS</span></span>

### <span data-ttu-id="e8ff8-140">System.object</span><span class="sxs-lookup"><span data-stu-id="e8ff8-140">System.String</span></span>

## <span data-ttu-id="e8ff8-141">輸出</span><span class="sxs-lookup"><span data-stu-id="e8ff8-141">OUTPUTS</span></span>

### <span data-ttu-id="e8ff8-142">SourceControl 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e8ff8-142">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="e8ff8-143">筆記</span><span class="sxs-lookup"><span data-stu-id="e8ff8-143">NOTES</span></span>

## <span data-ttu-id="e8ff8-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8ff8-144">RELATED LINKS</span></span>
