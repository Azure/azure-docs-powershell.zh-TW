---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/export-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
ms.openlocfilehash: 27fbac9c368725a25845454adf044c2ff6704f3d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98274763"
---
# <span data-ttu-id="c7221-101">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7221-101">Export-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="c7221-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c7221-102">SYNOPSIS</span></span>
<span data-ttu-id="c7221-103">將 DSC 設定從自動化匯出到本機檔案。</span><span class="sxs-lookup"><span data-stu-id="c7221-103">Exports a DSC configuration from Automation to a local file.</span></span>

## <span data-ttu-id="c7221-104">句法</span><span class="sxs-lookup"><span data-stu-id="c7221-104">SYNTAX</span></span>

```
Export-AzAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7221-105">說明</span><span class="sxs-lookup"><span data-stu-id="c7221-105">DESCRIPTION</span></span>
<span data-ttu-id="c7221-106">**Export AzAutomationDscConfiguration** Cmdlet 會將 (DSC) 設定中的接入件人所需的狀態設定匯出到本機檔案。</span><span class="sxs-lookup"><span data-stu-id="c7221-106">The **Export-AzAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="c7221-107">匯出的檔案具有. ps1 副檔名。</span><span class="sxs-lookup"><span data-stu-id="c7221-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="c7221-108">示例</span><span class="sxs-lookup"><span data-stu-id="c7221-108">EXAMPLES</span></span>

### <span data-ttu-id="c7221-109">範例1：匯出已發佈的 DSC 配置版本</span><span class="sxs-lookup"><span data-stu-id="c7221-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="c7221-110">這個命令會將 [自動化] 中的 [DSC 設定] 發行版本本匯出至指定的資料夾，即桌面。</span><span class="sxs-lookup"><span data-stu-id="c7221-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="c7221-111">參數</span><span class="sxs-lookup"><span data-stu-id="c7221-111">PARAMETERS</span></span>

### <span data-ttu-id="c7221-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c7221-112">-AutomationAccountName</span></span>
<span data-ttu-id="c7221-113">指定包含此 Cmdlet 匯出之 DSC 之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7221-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="c7221-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7221-114">-DefaultProfile</span></span>
<span data-ttu-id="c7221-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c7221-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7221-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c7221-116">-Force</span></span>
<span data-ttu-id="c7221-117">表示此 Cmdlet 會將現有的本機檔案替換成具有相同名稱的新檔案。</span><span class="sxs-lookup"><span data-stu-id="c7221-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="c7221-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="c7221-118">-Name</span></span>
<span data-ttu-id="c7221-119">指定此 Cmdlet 匯出的 DSC 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="c7221-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7221-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="c7221-120">-OutputFolder</span></span>
<span data-ttu-id="c7221-121">指定此 Cmdlet 匯出 DSC 設定的輸出檔案夾。</span><span class="sxs-lookup"><span data-stu-id="c7221-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="c7221-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7221-122">-ResourceGroupName</span></span>
<span data-ttu-id="c7221-123">指定此 Cmdlet 匯出 DSC 設定之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c7221-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="c7221-124">-槽</span><span class="sxs-lookup"><span data-stu-id="c7221-124">-Slot</span></span>
<span data-ttu-id="c7221-125">指定此 Cmdlet 匯出的 DSC 配置版本。</span><span class="sxs-lookup"><span data-stu-id="c7221-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="c7221-126">有效值為：</span><span class="sxs-lookup"><span data-stu-id="c7221-126">Valid values are:</span></span> 
- <span data-ttu-id="c7221-127">草案</span><span class="sxs-lookup"><span data-stu-id="c7221-127">Draft</span></span>
- <span data-ttu-id="c7221-128">已發佈預設值已發佈。</span><span class="sxs-lookup"><span data-stu-id="c7221-128">Published The default value is Published.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7221-129">-確認</span><span class="sxs-lookup"><span data-stu-id="c7221-129">-Confirm</span></span>
<span data-ttu-id="c7221-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c7221-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7221-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7221-131">-WhatIf</span></span>
<span data-ttu-id="c7221-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c7221-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7221-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c7221-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7221-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7221-134">CommonParameters</span></span>
<span data-ttu-id="c7221-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c7221-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7221-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c7221-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7221-137">輸入</span><span class="sxs-lookup"><span data-stu-id="c7221-137">INPUTS</span></span>

### <span data-ttu-id="c7221-138">System.object</span><span class="sxs-lookup"><span data-stu-id="c7221-138">System.String</span></span>

## <span data-ttu-id="c7221-139">輸出</span><span class="sxs-lookup"><span data-stu-id="c7221-139">OUTPUTS</span></span>

### <span data-ttu-id="c7221-140">DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="c7221-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="c7221-141">筆記</span><span class="sxs-lookup"><span data-stu-id="c7221-141">NOTES</span></span>

## <span data-ttu-id="c7221-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c7221-142">RELATED LINKS</span></span>

[<span data-ttu-id="c7221-143">AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7221-143">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="c7221-144">匯入-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7221-144">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


