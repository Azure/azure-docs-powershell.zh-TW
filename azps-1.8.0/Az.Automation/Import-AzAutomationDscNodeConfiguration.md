---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 32eafa841acd6bbe11e88775b021e4566b629717
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93623028"
---
# <span data-ttu-id="c9a13-101">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9a13-101">Import-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="c9a13-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c9a13-102">SYNOPSIS</span></span>
<span data-ttu-id="c9a13-103">在自動化中將 MOF 檔案匯入為 DSC 節點配置。</span><span class="sxs-lookup"><span data-stu-id="c9a13-103">Imports a MOF document as a DSC node configuration in Automation.</span></span>

## <span data-ttu-id="c9a13-104">句法</span><span class="sxs-lookup"><span data-stu-id="c9a13-104">SYNTAX</span></span>

```
Import-AzAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9a13-105">說明</span><span class="sxs-lookup"><span data-stu-id="c9a13-105">DESCRIPTION</span></span>
<span data-ttu-id="c9a13-106">匯 **入-AzAutomationDscConfiguration** Cmdlet 會將受管理的物件格式（ (MOF) 設定檔）匯入到 Azure 自動化中，做為所需的狀態設定 (DSC) 節點設定。</span><span class="sxs-lookup"><span data-stu-id="c9a13-106">The **Import-AzAutomationDscConfiguration** cmdlet imports a Managed Object Format (MOF) configuration document into Azure Automation as a Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="c9a13-107">指定 mof 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="c9a13-107">Specify the path of a .mof file.</span></span>

## <span data-ttu-id="c9a13-108">示例</span><span class="sxs-lookup"><span data-stu-id="c9a13-108">EXAMPLES</span></span>

### <span data-ttu-id="c9a13-109">範例1：將 DSC 節點設定匯入自動化</span><span class="sxs-lookup"><span data-stu-id="c9a13-109">Example 1: Import a DSC node configuration into Automation</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

<span data-ttu-id="c9a13-110">這個命令會將名為 web 檔案的 DSC 節點設定從 [DSC 設定] ContosoConfiguration 匯入到名為 Contoso17 的自動化帳戶中。</span><span class="sxs-lookup"><span data-stu-id="c9a13-110">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="c9a13-111">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="c9a13-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c9a13-112">如果有名為 ContosoConfiguration 的現有 DSC 節點設定，此命令會將它取代。</span><span class="sxs-lookup"><span data-stu-id="c9a13-112">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command replaces it.</span></span>

### <span data-ttu-id="c9a13-113">範例2：將 DSC 節點設定匯入自動化，然後建立新的組建版本，而不會覆寫現有的 NodeConfiguration。</span><span class="sxs-lookup"><span data-stu-id="c9a13-113">Example 2: Import a DSC node configuration into Automation and create a new build version and not overwrite existing NodeConfiguration.</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="c9a13-114">這個命令會將名為 web 檔案的 DSC 節點設定從 [DSC 設定] ContosoConfiguration 匯入到名為 Contoso17 的自動化帳戶中。</span><span class="sxs-lookup"><span data-stu-id="c9a13-114">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="c9a13-115">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="c9a13-115">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c9a13-116">如果有名為 ContosoConfiguration 的現有 DSC 節點設定，此命令會新增名稱為 ContosoConfiguration [2] 的新組建版本。</span><span class="sxs-lookup"><span data-stu-id="c9a13-116">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command adds a new build version with the name ContosoConfiguration[2].webserver.</span></span>

## <span data-ttu-id="c9a13-117">參數</span><span class="sxs-lookup"><span data-stu-id="c9a13-117">PARAMETERS</span></span>

### <span data-ttu-id="c9a13-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c9a13-118">-AutomationAccountName</span></span>
<span data-ttu-id="c9a13-119">指定此 Cmdlet 匯入 DSC 節點配置的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="c9a13-119">Specifies the name of the Automation account into which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="c9a13-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c9a13-120">-ConfigurationName</span></span>
<span data-ttu-id="c9a13-121">指定自動化中的 DSC 設定名稱，以做為要匯入之節點配置的命名空間和容器。</span><span class="sxs-lookup"><span data-stu-id="c9a13-121">Specifies the name of a DSC configuration in Automation to use as the namespace and container for the node configuration to import.</span></span>

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

### <span data-ttu-id="c9a13-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9a13-122">-DefaultProfile</span></span>
<span data-ttu-id="c9a13-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="c9a13-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9a13-124">-Force</span><span class="sxs-lookup"><span data-stu-id="c9a13-124">-Force</span></span>
<span data-ttu-id="c9a13-125">表示此 Cmdlet 會取代自動化中現有的 DSC 節點設定。</span><span class="sxs-lookup"><span data-stu-id="c9a13-125">Indicates that this cmdlet replaces an existing DSC node configuration in Automation.</span></span>

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

### <span data-ttu-id="c9a13-126">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="c9a13-126">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="c9a13-127">建立新的節點配置組建版本。</span><span class="sxs-lookup"><span data-stu-id="c9a13-127">Creates a new Node Configuration build version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9a13-128">-Path</span><span class="sxs-lookup"><span data-stu-id="c9a13-128">-Path</span></span>
<span data-ttu-id="c9a13-129">指定此 Cmdlet 所匯入的 MOF 設定檔路徑。</span><span class="sxs-lookup"><span data-stu-id="c9a13-129">Specifies the path of the MOF configuration document that this cmdlet imports.</span></span>

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

### <span data-ttu-id="c9a13-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9a13-130">-ResourceGroupName</span></span>
<span data-ttu-id="c9a13-131">指定此 Cmdlet 匯入 DSC 節點設定的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9a13-131">Specifies the name of a resource group for which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="c9a13-132">-確認</span><span class="sxs-lookup"><span data-stu-id="c9a13-132">-Confirm</span></span>
<span data-ttu-id="c9a13-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c9a13-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9a13-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9a13-134">-WhatIf</span></span>
<span data-ttu-id="c9a13-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c9a13-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9a13-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c9a13-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9a13-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9a13-137">CommonParameters</span></span>
<span data-ttu-id="c9a13-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c9a13-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9a13-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c9a13-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9a13-140">輸入</span><span class="sxs-lookup"><span data-stu-id="c9a13-140">INPUTS</span></span>

### <span data-ttu-id="c9a13-141">System.object</span><span class="sxs-lookup"><span data-stu-id="c9a13-141">System.String</span></span>

## <span data-ttu-id="c9a13-142">輸出</span><span class="sxs-lookup"><span data-stu-id="c9a13-142">OUTPUTS</span></span>

### <span data-ttu-id="c9a13-143">NodeConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c9a13-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span></span>

## <span data-ttu-id="c9a13-144">筆記</span><span class="sxs-lookup"><span data-stu-id="c9a13-144">NOTES</span></span>

## <span data-ttu-id="c9a13-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9a13-145">RELATED LINKS</span></span>

[<span data-ttu-id="c9a13-146">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9a13-146">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="c9a13-147">AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="c9a13-147">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)


