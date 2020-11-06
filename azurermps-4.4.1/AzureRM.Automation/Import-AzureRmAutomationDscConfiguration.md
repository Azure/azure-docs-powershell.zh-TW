---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 12cc605a95cb44b933c748156054135cb8395d61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450065"
---
# <span data-ttu-id="0d686-101">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d686-101">Import-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="0d686-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d686-102">SYNOPSIS</span></span>
<span data-ttu-id="0d686-103">將 DSC 設定匯入自動化。</span><span class="sxs-lookup"><span data-stu-id="0d686-103">Imports a DSC configuration into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d686-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d686-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d686-105">說明</span><span class="sxs-lookup"><span data-stu-id="0d686-105">DESCRIPTION</span></span>
<span data-ttu-id="0d686-106">匯 **入-AzureRmAutomationDscConfiguration** Cmdlet 會將 (DSC) 設定的 [所需的接入介面] 狀態設定匯入至 Azure 自動化。</span><span class="sxs-lookup"><span data-stu-id="0d686-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="0d686-107">指定包含單一 DSC 配置的存取點腳本路徑。</span><span class="sxs-lookup"><span data-stu-id="0d686-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="0d686-108">示例</span><span class="sxs-lookup"><span data-stu-id="0d686-108">EXAMPLES</span></span>

### <span data-ttu-id="0d686-109">範例1：將 DSC 設定匯入自動化</span><span class="sxs-lookup"><span data-stu-id="0d686-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="0d686-110">這個命令會將名為 client.ps1 的檔案中的 DSC 設定匯入到名為 Contoso17 的自動化帳戶中。</span><span class="sxs-lookup"><span data-stu-id="0d686-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="0d686-111">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="0d686-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="0d686-112">如果有現有的 DSC 設定，此命令會將它取代。</span><span class="sxs-lookup"><span data-stu-id="0d686-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="0d686-113">參數</span><span class="sxs-lookup"><span data-stu-id="0d686-113">PARAMETERS</span></span>

### <span data-ttu-id="0d686-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0d686-114">-AutomationAccountName</span></span>
<span data-ttu-id="0d686-115">指定此 Cmdlet 要匯入 DSC 設定的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0d686-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="0d686-116">-描述</span><span class="sxs-lookup"><span data-stu-id="0d686-116">-Description</span></span>
<span data-ttu-id="0d686-117">指定此 Cmdlet 所匯入之設定的描述。</span><span class="sxs-lookup"><span data-stu-id="0d686-117">Specifies a description of the configuration that this cmdlet imports.</span></span>

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

### <span data-ttu-id="0d686-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0d686-118">-Force</span></span>
<span data-ttu-id="0d686-119">表示此 Cmdlet 會取代自動化中的現有 DSC 設定。</span><span class="sxs-lookup"><span data-stu-id="0d686-119">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

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

### <span data-ttu-id="0d686-120">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="0d686-120">-LogVerbose</span></span>
<span data-ttu-id="0d686-121">指定此 Cmdlet 是否會針對此 DSC 設定開啟或關閉編譯作業的詳細記錄。</span><span class="sxs-lookup"><span data-stu-id="0d686-121">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="0d686-122">指定 $True 的值以開啟詳細記錄，或 $False 將其關閉。</span><span class="sxs-lookup"><span data-stu-id="0d686-122">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d686-123">-已發佈</span><span class="sxs-lookup"><span data-stu-id="0d686-123">-Published</span></span>
<span data-ttu-id="0d686-124">指示此 Cmdlet 會在已發佈狀態中匯入 DSC 設定。</span><span class="sxs-lookup"><span data-stu-id="0d686-124">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

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

### <span data-ttu-id="0d686-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d686-125">-ResourceGroupName</span></span>
<span data-ttu-id="0d686-126">指定此 Cmdlet 匯入 DSC 設定之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d686-126">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="0d686-127">-SourcePath</span><span class="sxs-lookup"><span data-stu-id="0d686-127">-SourcePath</span></span>
<span data-ttu-id="0d686-128">指定包含此 Cmdlet 所匯入之 DSC 設定之 wps_2 腳本的路徑。</span><span class="sxs-lookup"><span data-stu-id="0d686-128">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d686-129">-標記</span><span class="sxs-lookup"><span data-stu-id="0d686-129">-Tags</span></span>
<span data-ttu-id="0d686-130">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="0d686-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0d686-131">例如：</span><span class="sxs-lookup"><span data-stu-id="0d686-131">For example:</span></span>

<span data-ttu-id="0d686-132">@ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0d686-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d686-133">-確認</span><span class="sxs-lookup"><span data-stu-id="0d686-133">-Confirm</span></span>
<span data-ttu-id="0d686-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0d686-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d686-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d686-135">-WhatIf</span></span>
<span data-ttu-id="0d686-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0d686-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d686-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0d686-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d686-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d686-138">-DefaultProfile</span></span>
<span data-ttu-id="0d686-139">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d686-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d686-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d686-140">CommonParameters</span></span>
<span data-ttu-id="0d686-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d686-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d686-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0d686-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d686-143">輸入</span><span class="sxs-lookup"><span data-stu-id="0d686-143">INPUTS</span></span>

## <span data-ttu-id="0d686-144">輸出</span><span class="sxs-lookup"><span data-stu-id="0d686-144">OUTPUTS</span></span>

### <span data-ttu-id="0d686-145">DscConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="0d686-145">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="0d686-146">筆記</span><span class="sxs-lookup"><span data-stu-id="0d686-146">NOTES</span></span>

## <span data-ttu-id="0d686-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d686-147">RELATED LINKS</span></span>

[<span data-ttu-id="0d686-148">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d686-148">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="0d686-149">AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d686-149">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)
