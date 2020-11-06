---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Export-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: ed35cf910dd0bf51803b6a38edc90a93f5411520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445140"
---
# <span data-ttu-id="6734b-101">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6734b-101">Export-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="6734b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6734b-102">SYNOPSIS</span></span>
<span data-ttu-id="6734b-103">將 DSC 設定從自動化匯出到本機檔案。</span><span class="sxs-lookup"><span data-stu-id="6734b-103">Exports a DSC configuration from Automation to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6734b-104">句法</span><span class="sxs-lookup"><span data-stu-id="6734b-104">SYNTAX</span></span>

```
Export-AzureRmAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6734b-105">說明</span><span class="sxs-lookup"><span data-stu-id="6734b-105">DESCRIPTION</span></span>
<span data-ttu-id="6734b-106">**Export AzureRmAutomationDscConfiguration** Cmdlet 會將 (DSC) 設定中的接入件人所需的狀態設定匯出到本機檔案。</span><span class="sxs-lookup"><span data-stu-id="6734b-106">The **Export-AzureRmAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="6734b-107">匯出的檔案具有. ps1 副檔名。</span><span class="sxs-lookup"><span data-stu-id="6734b-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="6734b-108">示例</span><span class="sxs-lookup"><span data-stu-id="6734b-108">EXAMPLES</span></span>

### <span data-ttu-id="6734b-109">範例1：匯出已發佈的 DSC 配置版本</span><span class="sxs-lookup"><span data-stu-id="6734b-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="6734b-110">這個命令會將 [自動化] 中的 [DSC 設定] 發行版本本匯出至指定的資料夾，即桌面。</span><span class="sxs-lookup"><span data-stu-id="6734b-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="6734b-111">參數</span><span class="sxs-lookup"><span data-stu-id="6734b-111">PARAMETERS</span></span>

### <span data-ttu-id="6734b-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6734b-112">-AutomationAccountName</span></span>
<span data-ttu-id="6734b-113">指定包含此 Cmdlet 匯出之 DSC 之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="6734b-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="6734b-114">-Force</span><span class="sxs-lookup"><span data-stu-id="6734b-114">-Force</span></span>
<span data-ttu-id="6734b-115">表示此 Cmdlet 會將現有的本機檔案替換成具有相同名稱的新檔案。</span><span class="sxs-lookup"><span data-stu-id="6734b-115">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="6734b-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="6734b-116">-Name</span></span>
<span data-ttu-id="6734b-117">指定此 Cmdlet 匯出的 DSC 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="6734b-117">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

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

### <span data-ttu-id="6734b-118">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="6734b-118">-OutputFolder</span></span>
<span data-ttu-id="6734b-119">指定此 Cmdlet 匯出 DSC 設定的輸出檔案夾。</span><span class="sxs-lookup"><span data-stu-id="6734b-119">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="6734b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6734b-120">-ResourceGroupName</span></span>
<span data-ttu-id="6734b-121">指定此 Cmdlet 匯出 DSC 設定之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6734b-121">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="6734b-122">-槽</span><span class="sxs-lookup"><span data-stu-id="6734b-122">-Slot</span></span>
<span data-ttu-id="6734b-123">指定此 Cmdlet 匯出的 DSC 配置版本。</span><span class="sxs-lookup"><span data-stu-id="6734b-123">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="6734b-124">有效值為：</span><span class="sxs-lookup"><span data-stu-id="6734b-124">Valid values are:</span></span> 

- <span data-ttu-id="6734b-125">草案</span><span class="sxs-lookup"><span data-stu-id="6734b-125">Draft</span></span>
- <span data-ttu-id="6734b-126">時間</span><span class="sxs-lookup"><span data-stu-id="6734b-126">Published</span></span> 

<span data-ttu-id="6734b-127">預設值是 [發佈]。</span><span class="sxs-lookup"><span data-stu-id="6734b-127">The default value is Published.</span></span>

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

### <span data-ttu-id="6734b-128">-確認</span><span class="sxs-lookup"><span data-stu-id="6734b-128">-Confirm</span></span>
<span data-ttu-id="6734b-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6734b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6734b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6734b-130">-WhatIf</span></span>
<span data-ttu-id="6734b-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6734b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6734b-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6734b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6734b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6734b-133">-DefaultProfile</span></span>
<span data-ttu-id="6734b-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6734b-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6734b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6734b-135">CommonParameters</span></span>
<span data-ttu-id="6734b-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6734b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6734b-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6734b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6734b-138">輸入</span><span class="sxs-lookup"><span data-stu-id="6734b-138">INPUTS</span></span>

## <span data-ttu-id="6734b-139">輸出</span><span class="sxs-lookup"><span data-stu-id="6734b-139">OUTPUTS</span></span>

### <span data-ttu-id="6734b-140">DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="6734b-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="6734b-141">筆記</span><span class="sxs-lookup"><span data-stu-id="6734b-141">NOTES</span></span>

## <span data-ttu-id="6734b-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="6734b-142">RELATED LINKS</span></span>

[<span data-ttu-id="6734b-143">AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6734b-143">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="6734b-144">匯入-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="6734b-144">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


