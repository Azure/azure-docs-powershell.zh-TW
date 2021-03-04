---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/powershell/module/az.automation/start-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 7dfd7e0cfab041e43deae8321732b935adc5366a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915614"
---
# <span data-ttu-id="de3a1-101">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="de3a1-101">Start-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="de3a1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="de3a1-102">SYNOPSIS</span></span>
<span data-ttu-id="de3a1-103">在自動化中編譯 DSC 組配置。</span><span class="sxs-lookup"><span data-stu-id="de3a1-103">Compiles a DSC configuration in Automation.</span></span>

## <span data-ttu-id="de3a1-104">語法</span><span class="sxs-lookup"><span data-stu-id="de3a1-104">SYNTAX</span></span>

```
Start-AzAutomationDscCompilationJob [-ConfigurationName] <String> [-Parameters <IDictionary>]
 [-ConfigurationData <IDictionary>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de3a1-105">描述</span><span class="sxs-lookup"><span data-stu-id="de3a1-105">DESCRIPTION</span></span>
<span data-ttu-id="de3a1-106">**Start-AzAutomationDscCompilationJob** Cmdlet 會編譯 Azure Automation 中的 APS (DSC) 狀態組態。</span><span class="sxs-lookup"><span data-stu-id="de3a1-106">The **Start-AzAutomationDscCompilationJob** cmdlet compiles an APS Desired State Configuration (DSC) configuration in Azure Automation.</span></span>

## <span data-ttu-id="de3a1-107">例子</span><span class="sxs-lookup"><span data-stu-id="de3a1-107">EXAMPLES</span></span>

### <span data-ttu-id="de3a1-108">範例 1：在自動化中編譯 Azure DSC 組</span><span class="sxs-lookup"><span data-stu-id="de3a1-108">Example 1: Compile an Azure DSC configuration in Automation</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="de3a1-109">第一個命令會建立參數字典，並儲存在$Params變數中。</span><span class="sxs-lookup"><span data-stu-id="de3a1-109">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="de3a1-110">第二個命令會編譯名為 Config01 的 DSC 組配置。</span><span class="sxs-lookup"><span data-stu-id="de3a1-110">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="de3a1-111">該命令包含 DSC 設定參數$Params值。</span><span class="sxs-lookup"><span data-stu-id="de3a1-111">The command includes the values in $Params for DSC configuration parameters.</span></span>

### <span data-ttu-id="de3a1-112">範例 2：在自動化中以新的節點組配置版本編譯 Azure DSC 組配置。</span><span class="sxs-lookup"><span data-stu-id="de3a1-112">Example 2: Compile an Azure DSC configuration in Automation with a new Node Configuration build version.</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="de3a1-113">類似第一個範例，第一個命令會建立參數字典，並儲存在$Params變數中。</span><span class="sxs-lookup"><span data-stu-id="de3a1-113">Similar to the first example, the first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="de3a1-114">第二個命令會編譯名為 Config01 的 DSC 組配置。</span><span class="sxs-lookup"><span data-stu-id="de3a1-114">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="de3a1-115">該命令包含 DSC 設定參數$Params值。</span><span class="sxs-lookup"><span data-stu-id="de3a1-115">The command includes the values in $Params for DSC configuration parameters.</span></span>
<span data-ttu-id="de3a1-116">它不會使用名稱為 Config01[<2 或 2 的節點組 <NodeName>>]。</span><span class="sxs-lookup"><span data-stu-id="de3a1-116">It does not override the earlier existing Node Configuration by creating a new Node Configuration with the name Config01[<2>].<NodeName>.</span></span> <span data-ttu-id="de3a1-117">版本號碼會依據現有的版本號碼遞增。</span><span class="sxs-lookup"><span data-stu-id="de3a1-117">The version number is incremented based on the existing version number already present.</span></span>

## <span data-ttu-id="de3a1-118">參數</span><span class="sxs-lookup"><span data-stu-id="de3a1-118">PARAMETERS</span></span>

### <span data-ttu-id="de3a1-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="de3a1-119">-AutomationAccountName</span></span>
<span data-ttu-id="de3a1-120">指定包含此 Cmdlet 編譯之 DSC 配置的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="de3a1-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="de3a1-121">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="de3a1-121">-ConfigurationData</span></span>
<span data-ttu-id="de3a1-122">指定 DSC 組配置的群組原則資料字典。</span><span class="sxs-lookup"><span data-stu-id="de3a1-122">Specifies a dictionary of configuration data for DSC configuration.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3a1-123">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="de3a1-123">-ConfigurationName</span></span>
<span data-ttu-id="de3a1-124">指定此 Cmdlet 編譯的 DSC 組配置名稱。</span><span class="sxs-lookup"><span data-stu-id="de3a1-124">Specifies the name of the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de3a1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de3a1-125">-DefaultProfile</span></span>
<span data-ttu-id="de3a1-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="de3a1-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de3a1-127">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="de3a1-127">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="de3a1-128">建立新節點組組建版本。</span><span class="sxs-lookup"><span data-stu-id="de3a1-128">Creates a new Node Configuration build version.</span></span>

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

### <span data-ttu-id="de3a1-129">-參數</span><span class="sxs-lookup"><span data-stu-id="de3a1-129">-Parameters</span></span>
<span data-ttu-id="de3a1-130">指定此 Cmdlet 用來編譯 DSC 設定的參數字典。</span><span class="sxs-lookup"><span data-stu-id="de3a1-130">Specifies a dictionary of parameters that this cmdlet uses to compile the DSC configuration.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de3a1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de3a1-131">-ResourceGroupName</span></span>
<span data-ttu-id="de3a1-132">指定此 Cmdlet 編譯群組原則的資源組名。</span><span class="sxs-lookup"><span data-stu-id="de3a1-132">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="de3a1-133">-確認</span><span class="sxs-lookup"><span data-stu-id="de3a1-133">-Confirm</span></span>
<span data-ttu-id="de3a1-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="de3a1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de3a1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de3a1-135">-WhatIf</span></span>
<span data-ttu-id="de3a1-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="de3a1-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de3a1-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="de3a1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de3a1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de3a1-138">CommonParameters</span></span>
<span data-ttu-id="de3a1-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="de3a1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de3a1-140">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="de3a1-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de3a1-141">輸入</span><span class="sxs-lookup"><span data-stu-id="de3a1-141">INPUTS</span></span>

### <span data-ttu-id="de3a1-142">System.String</span><span class="sxs-lookup"><span data-stu-id="de3a1-142">System.String</span></span>

## <span data-ttu-id="de3a1-143">輸出</span><span class="sxs-lookup"><span data-stu-id="de3a1-143">OUTPUTS</span></span>

### <span data-ttu-id="de3a1-144">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="de3a1-144">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="de3a1-145">筆記</span><span class="sxs-lookup"><span data-stu-id="de3a1-145">NOTES</span></span>

## <span data-ttu-id="de3a1-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="de3a1-146">RELATED LINKS</span></span>

[<span data-ttu-id="de3a1-147">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="de3a1-147">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="de3a1-148">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="de3a1-148">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)


