---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/update-azurermautomationsourcecontrol
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Update-AzureRmAutomationSourceControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Update-AzureRmAutomationSourceControl.md
ms.openlocfilehash: 78308306e7bc46d4a9b3fadf4b00050cf9898f26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625362"
---
# <span data-ttu-id="a9413-101">Update-AzureRmAutomationSourceControl</span><span class="sxs-lookup"><span data-stu-id="a9413-101">Update-AzureRmAutomationSourceControl</span></span>

## <span data-ttu-id="a9413-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9413-102">SYNOPSIS</span></span>
<span data-ttu-id="a9413-103">更新 Azure 自動化來源控制。</span><span class="sxs-lookup"><span data-stu-id="a9413-103">Updates an Azure Automation source control.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9413-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9413-104">SYNTAX</span></span>

```
Update-AzureRmAutomationSourceControl -Name <String> [-AccessToken <SecureString>] [-FolderPath <String>]
 [-Branch <String>] [-Description <String>] [-AutoSync <Boolean>] [-PublishRunbook <Boolean>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9413-105">說明</span><span class="sxs-lookup"><span data-stu-id="a9413-105">DESCRIPTION</span></span>
<span data-ttu-id="a9413-106">Update-AzureRmAutomationSourceControl Cmdlet 會修改 Azure 自動化中來源控制項中欄位的值。</span><span class="sxs-lookup"><span data-stu-id="a9413-106">The Update-AzureRmAutomationSourceControl cmdlet modifies the value of a field in a source control in Azure Automation.</span></span>

## <span data-ttu-id="a9413-107">示例</span><span class="sxs-lookup"><span data-stu-id="a9413-107">EXAMPLES</span></span>

### <span data-ttu-id="a9413-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a9413-108">Example 1</span></span>
<span data-ttu-id="a9413-109">這個命令會將在名為 devAccount 的帳戶中名為 VSTSNative 的 Azure 自動化來源控制項的 PublishRunbook 欄位設為 false。</span><span class="sxs-lookup"><span data-stu-id="a9413-109">This commands sets the PublishRunbook field to false for the Azure Automation source control named VSTSNative in the account named devAccount.</span></span>


```powershell
Update-AzureRmAutomationSourceControl -ResourceGroupName "rg1" `
                                      -AutomationAccountName "devAccount" `
                                      -Name "VSTSNative" `
                                      -PublishRunbook $false 

Name            SourceType Branch FolderPath  AutoSync PublishRunbook RepoUrl
----            ---------- ------ ----------  -------- -------------- -------
VSTSNative      VsoTfvc           /MyRunbooks False    False          https://contoso.visualstudio.com/_git/Fin...
```

## <span data-ttu-id="a9413-110">參數</span><span class="sxs-lookup"><span data-stu-id="a9413-110">PARAMETERS</span></span>

### <span data-ttu-id="a9413-111">-AccessToken</span><span class="sxs-lookup"><span data-stu-id="a9413-111">-AccessToken</span></span>
<span data-ttu-id="a9413-112">來源控制項存取權杖。</span><span class="sxs-lookup"><span data-stu-id="a9413-112">The source control access token.</span></span>

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

### <span data-ttu-id="a9413-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a9413-113">-AutomationAccountName</span></span>
<span data-ttu-id="a9413-114">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a9413-114">The automation account name.</span></span>

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

### <span data-ttu-id="a9413-115">-AutoSync</span><span class="sxs-lookup"><span data-stu-id="a9413-115">-AutoSync</span></span>
<span data-ttu-id="a9413-116">來源控制項的 autoSync 屬性。</span><span class="sxs-lookup"><span data-stu-id="a9413-116">The autoSync property for the source control.</span></span>

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

### <span data-ttu-id="a9413-117">-分支</span><span class="sxs-lookup"><span data-stu-id="a9413-117">-Branch</span></span>
<span data-ttu-id="a9413-118">來源控制項分支。</span><span class="sxs-lookup"><span data-stu-id="a9413-118">The source control branch.</span></span>

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

### <span data-ttu-id="a9413-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9413-119">-DefaultProfile</span></span>
<span data-ttu-id="a9413-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9413-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9413-121">-描述</span><span class="sxs-lookup"><span data-stu-id="a9413-121">-Description</span></span>
<span data-ttu-id="a9413-122">來源控制項描述。</span><span class="sxs-lookup"><span data-stu-id="a9413-122">The source control description.</span></span>

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

### <span data-ttu-id="a9413-123">-FolderPath</span><span class="sxs-lookup"><span data-stu-id="a9413-123">-FolderPath</span></span>
<span data-ttu-id="a9413-124">[來源] 控制資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="a9413-124">The source control folder path.</span></span>

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

### <span data-ttu-id="a9413-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="a9413-125">-Name</span></span>
<span data-ttu-id="a9413-126">來源控制項名稱。</span><span class="sxs-lookup"><span data-stu-id="a9413-126">The source control name.</span></span>

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

### <span data-ttu-id="a9413-127">-PublishRunbook</span><span class="sxs-lookup"><span data-stu-id="a9413-127">-PublishRunbook</span></span>
<span data-ttu-id="a9413-128">來源控制項的 publishRunbook 屬性。</span><span class="sxs-lookup"><span data-stu-id="a9413-128">The publishRunbook property of the source control.</span></span>

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

### <span data-ttu-id="a9413-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9413-129">-ResourceGroupName</span></span>
<span data-ttu-id="a9413-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9413-130">The resource group name.</span></span>

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

### <span data-ttu-id="a9413-131">-確認</span><span class="sxs-lookup"><span data-stu-id="a9413-131">-Confirm</span></span>
<span data-ttu-id="a9413-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a9413-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9413-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9413-133">-WhatIf</span></span>
<span data-ttu-id="a9413-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a9413-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a9413-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9413-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9413-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9413-136">CommonParameters</span></span>
<span data-ttu-id="a9413-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9413-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9413-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a9413-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9413-139">輸入</span><span class="sxs-lookup"><span data-stu-id="a9413-139">INPUTS</span></span>

### <span data-ttu-id="a9413-140">System.object</span><span class="sxs-lookup"><span data-stu-id="a9413-140">System.String</span></span>

## <span data-ttu-id="a9413-141">輸出</span><span class="sxs-lookup"><span data-stu-id="a9413-141">OUTPUTS</span></span>

### <span data-ttu-id="a9413-142">SourceControl 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a9413-142">Microsoft.Azure.Commands.Automation.Model.SourceControl</span></span>

## <span data-ttu-id="a9413-143">筆記</span><span class="sxs-lookup"><span data-stu-id="a9413-143">NOTES</span></span>

## <span data-ttu-id="a9413-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9413-144">RELATED LINKS</span></span>
