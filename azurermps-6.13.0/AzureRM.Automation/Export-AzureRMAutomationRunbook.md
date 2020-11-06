---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 0FF88136-4FC9-41F2-A3E6-BFADBAFF4E44
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/export-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRMAutomationRunbook.md
ms.openlocfilehash: f982c68c49d6a8a92bb06bf150e352626730f67d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448488"
---
# <span data-ttu-id="13094-101">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="13094-101">Export-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="13094-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13094-102">SYNOPSIS</span></span>
<span data-ttu-id="13094-103">匯出自動化 runbook。</span><span class="sxs-lookup"><span data-stu-id="13094-103">Exports an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13094-104">句法</span><span class="sxs-lookup"><span data-stu-id="13094-104">SYNTAX</span></span>

```
Export-AzureRmAutomationRunbook [-Name] <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13094-105">說明</span><span class="sxs-lookup"><span data-stu-id="13094-105">DESCRIPTION</span></span>
<span data-ttu-id="13094-106">**Export-AzureRmAutomationRunbook** Cmdlet 會將 Azure 自動化 runbook 匯出至 wps_2 腳本 ( ps1 ) 檔案、wps_2 或 Wps_2 的工作流程 runbook，或針對圖形 runbook ( graphrunbook) 檔案。</span><span class="sxs-lookup"><span data-stu-id="13094-106">The **Export-AzureRmAutomationRunbook** cmdlet exports an Azure Automation runbook to a wps_2 script (.ps1 ) file, for wps_2 or wps_2 Workflow runbooks, or to a graphical runbook (.graphrunbook) file, for graphical runbooks.</span></span>
<span data-ttu-id="13094-107">[Runbook] 的名稱會變成匯出檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="13094-107">The name of the runbook becomes the name of the exported file.</span></span>

## <span data-ttu-id="13094-108">示例</span><span class="sxs-lookup"><span data-stu-id="13094-108">EXAMPLES</span></span>

### <span data-ttu-id="13094-109">範例1：匯出 runbook</span><span class="sxs-lookup"><span data-stu-id="13094-109">Example 1: Export a runbook</span></span>
```
PS C:\>Export-AzureRmAutomationRunbook -ResourceGroupName "ResourceGroup01" -AutomationAccountName "ContosoAutomationAccount" -Name "Runbook03" -Slot "Published" -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="13094-110">這個命令會將 [自動化] runbook 的已發佈版本匯出到使用者桌面。</span><span class="sxs-lookup"><span data-stu-id="13094-110">This command exports the published version of an Automation runbook to a user desktop.</span></span>

## <span data-ttu-id="13094-111">參數</span><span class="sxs-lookup"><span data-stu-id="13094-111">PARAMETERS</span></span>

### <span data-ttu-id="13094-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="13094-112">-AutomationAccountName</span></span>
<span data-ttu-id="13094-113">指定此 Cmdlet 匯出 runbook 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="13094-113">Specifies the name of the Automation account in which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="13094-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13094-114">-DefaultProfile</span></span>
<span data-ttu-id="13094-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="13094-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13094-116">-Force</span><span class="sxs-lookup"><span data-stu-id="13094-116">-Force</span></span>
<span data-ttu-id="13094-117">ps_force</span><span class="sxs-lookup"><span data-stu-id="13094-117">ps_force</span></span>

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

### <span data-ttu-id="13094-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="13094-118">-Name</span></span>
<span data-ttu-id="13094-119">指定此 Cmdlet 匯出的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="13094-119">Specifies the name of the runbook that this cmdlet exports.</span></span>
<span data-ttu-id="13094-120">[Runbook] 的名稱會變成匯出檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="13094-120">The name of the runbook becomes the name of the export file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13094-121">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="13094-121">-OutputFolder</span></span>
<span data-ttu-id="13094-122">指定此 Cmdlet 在其中建立匯出檔案的資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="13094-122">Specifies the path of a folder in which this cmdlet creates the export file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="13094-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13094-123">-ResourceGroupName</span></span>
<span data-ttu-id="13094-124">指定此 Cmdlet 匯出 runbook 的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="13094-124">Specifies the name of the resource group for which this cmdlet exports a runbook.</span></span>

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

### <span data-ttu-id="13094-125">-槽</span><span class="sxs-lookup"><span data-stu-id="13094-125">-Slot</span></span>
<span data-ttu-id="13094-126">指定此 Cmdlet 是否匯出 runbook 的草稿或已發佈內容。</span><span class="sxs-lookup"><span data-stu-id="13094-126">Specifies whether this cmdlet exports the draft or published content of the runbook.</span></span>
<span data-ttu-id="13094-127">有效值為：</span><span class="sxs-lookup"><span data-stu-id="13094-127">Valid values are:</span></span> 
- <span data-ttu-id="13094-128">時間</span><span class="sxs-lookup"><span data-stu-id="13094-128">Published</span></span> 
- <span data-ttu-id="13094-129">草案</span><span class="sxs-lookup"><span data-stu-id="13094-129">Draft</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13094-130">-確認</span><span class="sxs-lookup"><span data-stu-id="13094-130">-Confirm</span></span>
<span data-ttu-id="13094-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="13094-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13094-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13094-132">-WhatIf</span></span>
<span data-ttu-id="13094-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="13094-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13094-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13094-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13094-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13094-135">CommonParameters</span></span>
<span data-ttu-id="13094-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13094-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13094-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="13094-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13094-138">輸入</span><span class="sxs-lookup"><span data-stu-id="13094-138">INPUTS</span></span>

### <span data-ttu-id="13094-139">System.object</span><span class="sxs-lookup"><span data-stu-id="13094-139">System.String</span></span>

## <span data-ttu-id="13094-140">輸出</span><span class="sxs-lookup"><span data-stu-id="13094-140">OUTPUTS</span></span>

### <span data-ttu-id="13094-141">DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="13094-141">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="13094-142">筆記</span><span class="sxs-lookup"><span data-stu-id="13094-142">NOTES</span></span>

## <span data-ttu-id="13094-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="13094-143">RELATED LINKS</span></span>

[<span data-ttu-id="13094-144">AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="13094-144">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="13094-145">匯入-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="13094-145">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="13094-146">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="13094-146">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="13094-147">新-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="13094-147">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="13094-148">發佈-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="13094-148">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="13094-149">移除-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="13094-149">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="13094-150">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="13094-150">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="13094-151">開始-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="13094-151">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


