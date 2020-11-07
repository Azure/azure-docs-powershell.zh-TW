---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: cef704c9ab09a17ffe91d3a1541e39df1e943964
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623488"
---
# <span data-ttu-id="e5bec-101">Import-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5bec-101">Import-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="e5bec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5bec-102">SYNOPSIS</span></span>
<span data-ttu-id="e5bec-103">在自動化中將 MOF 檔案匯入為 DSC 節點配置。</span><span class="sxs-lookup"><span data-stu-id="e5bec-103">Imports a MOF document as a DSC node configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5bec-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5bec-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5bec-105">說明</span><span class="sxs-lookup"><span data-stu-id="e5bec-105">DESCRIPTION</span></span>
<span data-ttu-id="e5bec-106">匯 **入-AzureRmAutomationDscConfiguration** Cmdlet 會將受管理的物件格式（ (MOF) 設定檔）匯入到 Azure 自動化中，做為所需的狀態設定 (DSC) 節點設定。</span><span class="sxs-lookup"><span data-stu-id="e5bec-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports a Managed Object Format (MOF) configuration document into Azure Automation as a Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="e5bec-107">指定 mof 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="e5bec-107">Specify the path of a .mof file.</span></span>

## <span data-ttu-id="e5bec-108">示例</span><span class="sxs-lookup"><span data-stu-id="e5bec-108">EXAMPLES</span></span>

### <span data-ttu-id="e5bec-109">範例1：將 DSC 節點設定匯入自動化</span><span class="sxs-lookup"><span data-stu-id="e5bec-109">Example 1: Import a DSC node configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

<span data-ttu-id="e5bec-110">這個命令會將名為 web 檔案的 DSC 節點設定從 [DSC 設定] ContosoConfiguration 匯入到名為 Contoso17 的自動化帳戶中。</span><span class="sxs-lookup"><span data-stu-id="e5bec-110">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="e5bec-111">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="e5bec-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e5bec-112">如果有名為 ContosoConfiguration 的現有 DSC 節點設定，此命令會將它取代。</span><span class="sxs-lookup"><span data-stu-id="e5bec-112">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command replaces it.</span></span>

### <span data-ttu-id="e5bec-113">範例2：將 DSC 節點設定匯入自動化，然後建立新的組建版本，而不會覆寫現有的 NodeConfiguration。</span><span class="sxs-lookup"><span data-stu-id="e5bec-113">Example 2: Import a DSC node configuration into Automation and create a new build version and not overwrite existing NodeConfiguration.</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="e5bec-114">這個命令會將名為 web 檔案的 DSC 節點設定從 [DSC 設定] ContosoConfiguration 匯入到名為 Contoso17 的自動化帳戶中。</span><span class="sxs-lookup"><span data-stu-id="e5bec-114">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="e5bec-115">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="e5bec-115">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e5bec-116">如果有名為 ContosoConfiguration 的現有 DSC 節點設定，此命令會新增名稱為 ContosoConfiguration [2] 的新組建版本。</span><span class="sxs-lookup"><span data-stu-id="e5bec-116">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command adds a new build version with the name ContosoConfiguration[2].webserver.</span></span>

## <span data-ttu-id="e5bec-117">參數</span><span class="sxs-lookup"><span data-stu-id="e5bec-117">PARAMETERS</span></span>

### <span data-ttu-id="e5bec-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e5bec-118">-AutomationAccountName</span></span>
<span data-ttu-id="e5bec-119">指定此 Cmdlet 匯入 DSC 節點配置的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e5bec-119">Specifies the name of the Automation account into which this cmdlet imports a DSC node configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5bec-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e5bec-120">-ConfigurationName</span></span>
<span data-ttu-id="e5bec-121">指定自動化中的 DSC 設定名稱，以做為要匯入之節點配置的命名空間和容器。</span><span class="sxs-lookup"><span data-stu-id="e5bec-121">Specifies the name of a DSC configuration in Automation to use as the namespace and container for the node configuration to import.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5bec-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5bec-122">-DefaultProfile</span></span>
<span data-ttu-id="e5bec-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e5bec-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5bec-124">-Force</span><span class="sxs-lookup"><span data-stu-id="e5bec-124">-Force</span></span>
<span data-ttu-id="e5bec-125">表示此 Cmdlet 會取代自動化中現有的 DSC 節點設定。</span><span class="sxs-lookup"><span data-stu-id="e5bec-125">Indicates that this cmdlet replaces an existing DSC node configuration in Automation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5bec-126">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="e5bec-126">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="e5bec-127">建立新的節點配置組建版本。</span><span class="sxs-lookup"><span data-stu-id="e5bec-127">Creates a new Node Configuration build version.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5bec-128">-Path</span><span class="sxs-lookup"><span data-stu-id="e5bec-128">-Path</span></span>
<span data-ttu-id="e5bec-129">指定此 Cmdlet 所匯入的 MOF 設定檔路徑。</span><span class="sxs-lookup"><span data-stu-id="e5bec-129">Specifies the path of the MOF configuration document that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5bec-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5bec-130">-ResourceGroupName</span></span>
<span data-ttu-id="e5bec-131">指定此 Cmdlet 匯入 DSC 節點設定的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5bec-131">Specifies the name of a resource group for which this cmdlet imports a DSC node configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5bec-132">-確認</span><span class="sxs-lookup"><span data-stu-id="e5bec-132">-Confirm</span></span>
<span data-ttu-id="e5bec-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5bec-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5bec-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5bec-134">-WhatIf</span></span>
<span data-ttu-id="e5bec-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5bec-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5bec-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5bec-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5bec-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5bec-137">CommonParameters</span></span>
<span data-ttu-id="e5bec-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5bec-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5bec-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5bec-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5bec-140">輸入</span><span class="sxs-lookup"><span data-stu-id="e5bec-140">INPUTS</span></span>

### <span data-ttu-id="e5bec-141">所有</span><span class="sxs-lookup"><span data-stu-id="e5bec-141">None</span></span>
<span data-ttu-id="e5bec-142">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e5bec-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e5bec-143">輸出</span><span class="sxs-lookup"><span data-stu-id="e5bec-143">OUTPUTS</span></span>

### <span data-ttu-id="e5bec-144">NodeConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e5bec-144">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span></span>

## <span data-ttu-id="e5bec-145">筆記</span><span class="sxs-lookup"><span data-stu-id="e5bec-145">NOTES</span></span>

## <span data-ttu-id="e5bec-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5bec-146">RELATED LINKS</span></span>

[<span data-ttu-id="e5bec-147">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5bec-147">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="e5bec-148">AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5bec-148">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)


