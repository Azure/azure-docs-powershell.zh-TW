---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 3036b02d280542ffa4c8eea85dafed2da8eb5e28
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966428"
---
# <span data-ttu-id="429b6-101">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="429b6-101">Import-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="429b6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="429b6-102">SYNOPSIS</span></span>
<span data-ttu-id="429b6-103">在自動化中將 MOF 檔案匯入為 DSC 節點配置。</span><span class="sxs-lookup"><span data-stu-id="429b6-103">Imports a MOF document as a DSC node configuration in Automation.</span></span>

## <span data-ttu-id="429b6-104">句法</span><span class="sxs-lookup"><span data-stu-id="429b6-104">SYNTAX</span></span>

```
Import-AzAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="429b6-105">說明</span><span class="sxs-lookup"><span data-stu-id="429b6-105">DESCRIPTION</span></span>
<span data-ttu-id="429b6-106">匯 **入-AzAutomationDscConfiguration** Cmdlet 會將受管理的物件格式（ (MOF) 設定檔）匯入到 Azure 自動化中，做為所需的狀態設定 (DSC) 節點設定。</span><span class="sxs-lookup"><span data-stu-id="429b6-106">The **Import-AzAutomationDscConfiguration** cmdlet imports a Managed Object Format (MOF) configuration document into Azure Automation as a Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="429b6-107">指定 mof 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="429b6-107">Specify the path of a .mof file.</span></span>

## <span data-ttu-id="429b6-108">示例</span><span class="sxs-lookup"><span data-stu-id="429b6-108">EXAMPLES</span></span>

### <span data-ttu-id="429b6-109">範例1：將 DSC 節點設定匯入自動化</span><span class="sxs-lookup"><span data-stu-id="429b6-109">Example 1: Import a DSC node configuration into Automation</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

<span data-ttu-id="429b6-110">這個命令會將名為 web 檔案的 DSC 節點設定從 [DSC 設定] ContosoConfiguration 匯入到名為 Contoso17 的自動化帳戶中。</span><span class="sxs-lookup"><span data-stu-id="429b6-110">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="429b6-111">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="429b6-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="429b6-112">如果有名為 ContosoConfiguration 的現有 DSC 節點設定，此命令會將它取代。</span><span class="sxs-lookup"><span data-stu-id="429b6-112">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command replaces it.</span></span>

### <span data-ttu-id="429b6-113">範例2：將 DSC 節點設定匯入自動化，然後建立新的組建版本，而不會覆寫現有的 NodeConfiguration。</span><span class="sxs-lookup"><span data-stu-id="429b6-113">Example 2: Import a DSC node configuration into Automation and create a new build version and not overwrite existing NodeConfiguration.</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="429b6-114">這個命令會將名為 web 檔案的 DSC 節點設定從 [DSC 設定] ContosoConfiguration 匯入到名為 Contoso17 的自動化帳戶中。</span><span class="sxs-lookup"><span data-stu-id="429b6-114">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="429b6-115">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="429b6-115">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="429b6-116">如果有名為 ContosoConfiguration 的現有 DSC 節點設定，此命令會新增名稱為 ContosoConfiguration [2] 的新組建版本。</span><span class="sxs-lookup"><span data-stu-id="429b6-116">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command adds a new build version with the name ContosoConfiguration[2].webserver.</span></span>

## <span data-ttu-id="429b6-117">參數</span><span class="sxs-lookup"><span data-stu-id="429b6-117">PARAMETERS</span></span>

### <span data-ttu-id="429b6-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="429b6-118">-AutomationAccountName</span></span>
<span data-ttu-id="429b6-119">指定此 Cmdlet 匯入 DSC 節點配置的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="429b6-119">Specifies the name of the Automation account into which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="429b6-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="429b6-120">-ConfigurationName</span></span>
<span data-ttu-id="429b6-121">指定自動化中的 DSC 設定名稱，以做為要匯入之節點配置的命名空間和容器。</span><span class="sxs-lookup"><span data-stu-id="429b6-121">Specifies the name of a DSC configuration in Automation to use as the namespace and container for the node configuration to import.</span></span>

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

### <span data-ttu-id="429b6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="429b6-122">-DefaultProfile</span></span>
<span data-ttu-id="429b6-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="429b6-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="429b6-124">-Force</span><span class="sxs-lookup"><span data-stu-id="429b6-124">-Force</span></span>
<span data-ttu-id="429b6-125">表示此 Cmdlet 會取代自動化中現有的 DSC 節點設定。</span><span class="sxs-lookup"><span data-stu-id="429b6-125">Indicates that this cmdlet replaces an existing DSC node configuration in Automation.</span></span>

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

### <span data-ttu-id="429b6-126">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="429b6-126">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="429b6-127">建立新的節點配置組建版本。</span><span class="sxs-lookup"><span data-stu-id="429b6-127">Creates a new Node Configuration build version.</span></span>

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

### <span data-ttu-id="429b6-128">-Path</span><span class="sxs-lookup"><span data-stu-id="429b6-128">-Path</span></span>
<span data-ttu-id="429b6-129">指定此 Cmdlet 所匯入的 MOF 設定檔路徑。</span><span class="sxs-lookup"><span data-stu-id="429b6-129">Specifies the path of the MOF configuration document that this cmdlet imports.</span></span>

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

### <span data-ttu-id="429b6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="429b6-130">-ResourceGroupName</span></span>
<span data-ttu-id="429b6-131">指定此 Cmdlet 匯入 DSC 節點設定的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="429b6-131">Specifies the name of a resource group for which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="429b6-132">-確認</span><span class="sxs-lookup"><span data-stu-id="429b6-132">-Confirm</span></span>
<span data-ttu-id="429b6-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="429b6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="429b6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="429b6-134">-WhatIf</span></span>
<span data-ttu-id="429b6-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="429b6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="429b6-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="429b6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="429b6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="429b6-137">CommonParameters</span></span>
<span data-ttu-id="429b6-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="429b6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="429b6-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="429b6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="429b6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="429b6-140">INPUTS</span></span>

### <span data-ttu-id="429b6-141">System.object</span><span class="sxs-lookup"><span data-stu-id="429b6-141">System.String</span></span>

## <span data-ttu-id="429b6-142">輸出</span><span class="sxs-lookup"><span data-stu-id="429b6-142">OUTPUTS</span></span>

### <span data-ttu-id="429b6-143">NodeConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="429b6-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span></span>

## <span data-ttu-id="429b6-144">筆記</span><span class="sxs-lookup"><span data-stu-id="429b6-144">NOTES</span></span>

## <span data-ttu-id="429b6-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="429b6-145">RELATED LINKS</span></span>

[<span data-ttu-id="429b6-146">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="429b6-146">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="429b6-147">AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="429b6-147">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

