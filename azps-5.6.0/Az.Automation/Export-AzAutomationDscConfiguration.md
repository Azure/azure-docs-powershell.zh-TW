---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/powershell/module/az.automation/export-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
ms.openlocfilehash: c27f878d2dbb0e52a16216a2158c737bc523c932
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903681"
---
# <span data-ttu-id="f36fe-101">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f36fe-101">Export-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="f36fe-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f36fe-102">SYNOPSIS</span></span>
<span data-ttu-id="f36fe-103">將 DSC 組案從自動化匯出至本地檔案。</span><span class="sxs-lookup"><span data-stu-id="f36fe-103">Exports a DSC configuration from Automation to a local file.</span></span>

## <span data-ttu-id="f36fe-104">語法</span><span class="sxs-lookup"><span data-stu-id="f36fe-104">SYNTAX</span></span>

```
Export-AzAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f36fe-105">描述</span><span class="sxs-lookup"><span data-stu-id="f36fe-105">DESCRIPTION</span></span>
<span data-ttu-id="f36fe-106">**Export-AzAutomationDscConfiguration Cmdlet** 會從 Azure Automation 將 APS 想要的狀態組態 (DSC) 組態匯出至本地檔案。</span><span class="sxs-lookup"><span data-stu-id="f36fe-106">The **Export-AzAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="f36fe-107">匯出的檔案副檔名為 .ps1。</span><span class="sxs-lookup"><span data-stu-id="f36fe-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="f36fe-108">例子</span><span class="sxs-lookup"><span data-stu-id="f36fe-108">EXAMPLES</span></span>

### <span data-ttu-id="f36fe-109">範例 1：匯出 DSC 組配置的已發佈版本</span><span class="sxs-lookup"><span data-stu-id="f36fe-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="f36fe-110">此命令會匯出自動化中已發佈的 DSC 組配置版本至指定的資料夾 ，即桌面。</span><span class="sxs-lookup"><span data-stu-id="f36fe-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="f36fe-111">參數</span><span class="sxs-lookup"><span data-stu-id="f36fe-111">PARAMETERS</span></span>

### <span data-ttu-id="f36fe-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f36fe-112">-AutomationAccountName</span></span>
<span data-ttu-id="f36fe-113">指定包含此 Cmdlet 匯出之 DSC 的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f36fe-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="f36fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f36fe-114">-DefaultProfile</span></span>
<span data-ttu-id="f36fe-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="f36fe-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f36fe-116">-強制</span><span class="sxs-lookup"><span data-stu-id="f36fe-116">-Force</span></span>
<span data-ttu-id="f36fe-117">表示此 Cmdlet 會以名稱相同的新檔案取代現有的本地檔案。</span><span class="sxs-lookup"><span data-stu-id="f36fe-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="f36fe-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="f36fe-118">-Name</span></span>
<span data-ttu-id="f36fe-119">指定此 Cmdlet 匯出的 DSC 群組原則名稱。</span><span class="sxs-lookup"><span data-stu-id="f36fe-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

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

### <span data-ttu-id="f36fe-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="f36fe-120">-OutputFolder</span></span>
<span data-ttu-id="f36fe-121">指定此 Cmdlet 匯出 DSC 組配置的輸出檔案夾。</span><span class="sxs-lookup"><span data-stu-id="f36fe-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="f36fe-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f36fe-122">-ResourceGroupName</span></span>
<span data-ttu-id="f36fe-123">指定此 Cmdlet 匯出 DSC 群組原則的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f36fe-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="f36fe-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="f36fe-124">-Slot</span></span>
<span data-ttu-id="f36fe-125">指定此 Cmdlet 匯出的 DSC 群組原則版本。</span><span class="sxs-lookup"><span data-stu-id="f36fe-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="f36fe-126">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="f36fe-126">Valid values are:</span></span> 
- <span data-ttu-id="f36fe-127">草案</span><span class="sxs-lookup"><span data-stu-id="f36fe-127">Draft</span></span>
- <span data-ttu-id="f36fe-128">已發佈預設值為已發佈。</span><span class="sxs-lookup"><span data-stu-id="f36fe-128">Published The default value is Published.</span></span>

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

### <span data-ttu-id="f36fe-129">-確認</span><span class="sxs-lookup"><span data-stu-id="f36fe-129">-Confirm</span></span>
<span data-ttu-id="f36fe-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f36fe-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f36fe-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f36fe-131">-WhatIf</span></span>
<span data-ttu-id="f36fe-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f36fe-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f36fe-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f36fe-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f36fe-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f36fe-134">CommonParameters</span></span>
<span data-ttu-id="f36fe-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f36fe-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f36fe-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f36fe-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f36fe-137">輸入</span><span class="sxs-lookup"><span data-stu-id="f36fe-137">INPUTS</span></span>

### <span data-ttu-id="f36fe-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f36fe-138">System.String</span></span>

## <span data-ttu-id="f36fe-139">輸出</span><span class="sxs-lookup"><span data-stu-id="f36fe-139">OUTPUTS</span></span>

### <span data-ttu-id="f36fe-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="f36fe-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="f36fe-141">筆記</span><span class="sxs-lookup"><span data-stu-id="f36fe-141">NOTES</span></span>

## <span data-ttu-id="f36fe-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="f36fe-142">RELATED LINKS</span></span>

[<span data-ttu-id="f36fe-143">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f36fe-143">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="f36fe-144">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f36fe-144">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


