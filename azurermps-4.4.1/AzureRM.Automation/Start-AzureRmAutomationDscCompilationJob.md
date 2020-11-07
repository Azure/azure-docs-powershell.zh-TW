---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: 6e4db8baaa4e86fe9557ce20f1fd486ce14bdd6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624222"
---
# <span data-ttu-id="97511-101">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="97511-101">Start-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="97511-102">摘要</span><span class="sxs-lookup"><span data-stu-id="97511-102">SYNOPSIS</span></span>
<span data-ttu-id="97511-103">在自動化中編譯 DSC 設定。</span><span class="sxs-lookup"><span data-stu-id="97511-103">Compiles a DSC configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97511-104">句法</span><span class="sxs-lookup"><span data-stu-id="97511-104">SYNTAX</span></span>

```
Start-AzureRmAutomationDscCompilationJob [-ConfigurationName] <String> [-Parameters <IDictionary>]
 [-ConfigurationData <IDictionary>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="97511-105">說明</span><span class="sxs-lookup"><span data-stu-id="97511-105">DESCRIPTION</span></span>
<span data-ttu-id="97511-106">**Start-AzureRmAutomationDscCompilationJob** Cmdlet 會在 Azure 自動化中編譯 (DSC) 設定的 Ap 所需狀態設定。</span><span class="sxs-lookup"><span data-stu-id="97511-106">The **Start-AzureRmAutomationDscCompilationJob** cmdlet compiles an APS Desired State Configuration (DSC) configuration in Azure Automation.</span></span>

## <span data-ttu-id="97511-107">示例</span><span class="sxs-lookup"><span data-stu-id="97511-107">EXAMPLES</span></span>

### <span data-ttu-id="97511-108">範例1：在自動化中編譯 Azure DSC 設定</span><span class="sxs-lookup"><span data-stu-id="97511-108">Example 1: Compile an Azure DSC configuration in Automation</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzureRmAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="97511-109">第一個命令會建立參數字典，並將它們儲存在 $Params 變數中。</span><span class="sxs-lookup"><span data-stu-id="97511-109">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="97511-110">第二個命令會編譯名為 Config01 的 DSC 配置。</span><span class="sxs-lookup"><span data-stu-id="97511-110">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="97511-111">此命令包括 DSC 設定參數 $Params 中的值。</span><span class="sxs-lookup"><span data-stu-id="97511-111">The command includes the values in $Params for DSC configuration parameters.</span></span>

### <span data-ttu-id="97511-112">範例2：使用新的節點配置組建版本，在自動化中編譯 Azure DSC 設定。</span><span class="sxs-lookup"><span data-stu-id="97511-112">Example 2: Compile an Azure DSC configuration in Automation with a new Node Configuration build version.</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzureRmAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="97511-113">與第一個範例類似，第一個命令會建立一個參數字典，並將它們儲存在 $Params 變數中。</span><span class="sxs-lookup"><span data-stu-id="97511-113">Similar to the first example, the first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="97511-114">第二個命令會編譯名為 Config01 的 DSC 配置。</span><span class="sxs-lookup"><span data-stu-id="97511-114">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="97511-115">此命令包括 DSC 設定參數 $Params 中的值。</span><span class="sxs-lookup"><span data-stu-id="97511-115">The command includes the values in $Params for DSC configuration parameters.</span></span>

<span data-ttu-id="97511-116">它不會以名稱 Config01 [<2>]」建立新的節點設定，來覆寫較舊的現有節點 <NodeName> 設定。</span><span class="sxs-lookup"><span data-stu-id="97511-116">It does not override the earlier existing Node Configuration by creating a new Node Configuration with the name Config01[<2>].<NodeName>.</span></span> <span data-ttu-id="97511-117">版本號碼會根據已存在的現有版本編號增加。</span><span class="sxs-lookup"><span data-stu-id="97511-117">The version number is incremented based on the existing version number already present.</span></span>

## <span data-ttu-id="97511-118">參數</span><span class="sxs-lookup"><span data-stu-id="97511-118">PARAMETERS</span></span>

### <span data-ttu-id="97511-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="97511-119">-AutomationAccountName</span></span>
<span data-ttu-id="97511-120">指定包含此 Cmdlet 所編譯之 DSC 設定的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="97511-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="97511-121">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="97511-121">-ConfigurationData</span></span>
<span data-ttu-id="97511-122">指定 DSC 設定的配置資料字典。</span><span class="sxs-lookup"><span data-stu-id="97511-122">Specifies a dictionary of configuration data for DSC configuration.</span></span>

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

### <span data-ttu-id="97511-123">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="97511-123">-ConfigurationName</span></span>
<span data-ttu-id="97511-124">指定此 Cmdlet 編譯的 DSC 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="97511-124">Specifies the name of the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="97511-125">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="97511-125">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="97511-126">建立新的節點配置組建版本。</span><span class="sxs-lookup"><span data-stu-id="97511-126">Creates a new Node Configuration build version.</span></span>

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

### <span data-ttu-id="97511-127">-參數</span><span class="sxs-lookup"><span data-stu-id="97511-127">-Parameters</span></span>
<span data-ttu-id="97511-128">指定此 Cmdlet 用來編譯 DSC 設定的參數字典。</span><span class="sxs-lookup"><span data-stu-id="97511-128">Specifies a dictionary of parameters that this cmdlet uses to compile the DSC configuration.</span></span>

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

### <span data-ttu-id="97511-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97511-129">-ResourceGroupName</span></span>
<span data-ttu-id="97511-130">指定此 Cmdlet 在其中編譯配置的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="97511-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="97511-131">-確認</span><span class="sxs-lookup"><span data-stu-id="97511-131">-Confirm</span></span>
<span data-ttu-id="97511-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="97511-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97511-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97511-133">-WhatIf</span></span>
<span data-ttu-id="97511-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="97511-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97511-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="97511-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97511-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97511-136">-DefaultProfile</span></span>
<span data-ttu-id="97511-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="97511-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97511-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97511-138">CommonParameters</span></span>
<span data-ttu-id="97511-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="97511-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97511-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="97511-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97511-141">輸入</span><span class="sxs-lookup"><span data-stu-id="97511-141">INPUTS</span></span>

## <span data-ttu-id="97511-142">輸出</span><span class="sxs-lookup"><span data-stu-id="97511-142">OUTPUTS</span></span>

### <span data-ttu-id="97511-143">CompilationJob 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="97511-143">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="97511-144">筆記</span><span class="sxs-lookup"><span data-stu-id="97511-144">NOTES</span></span>

## <span data-ttu-id="97511-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="97511-145">RELATED LINKS</span></span>

[<span data-ttu-id="97511-146">AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="97511-146">Get-AzureRmAutomationDscCompilationJob</span></span>](./Get-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="97511-147">AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="97511-147">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)


