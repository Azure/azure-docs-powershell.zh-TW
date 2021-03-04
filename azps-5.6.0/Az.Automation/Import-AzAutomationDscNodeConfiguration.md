---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/powershell/module/az.automation/import-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 3680d277addba29444f3f2955d7cca28505435a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917433"
---
# <span data-ttu-id="d4fb6-101">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4fb6-101">Import-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="d4fb6-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d4fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="d4fb6-103">在自動化中將 MOF 檔案做為 DSC 節點組組。</span><span class="sxs-lookup"><span data-stu-id="d4fb6-103">Imports a MOF document as a DSC node configuration in Automation.</span></span>

## <span data-ttu-id="d4fb6-104">語法</span><span class="sxs-lookup"><span data-stu-id="d4fb6-104">SYNTAX</span></span>

```
Import-AzAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4fb6-105">描述</span><span class="sxs-lookup"><span data-stu-id="d4fb6-105">DESCRIPTION</span></span>
<span data-ttu-id="d4fb6-106">**Import-AzAutomationDscConfiguration Cmdlet** 將 Managed 物件格式 (MOF) 組態檔，以做為所需的狀態組態 (DSC) 節點組態。</span><span class="sxs-lookup"><span data-stu-id="d4fb6-106">The **Import-AzAutomationDscConfiguration** cmdlet imports a Managed Object Format (MOF) configuration document into Azure Automation as a Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="d4fb6-107">指定 .mof 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="d4fb6-107">Specify the path of a .mof file.</span></span>

## <span data-ttu-id="d4fb6-108">例子</span><span class="sxs-lookup"><span data-stu-id="d4fb6-108">EXAMPLES</span></span>

### <span data-ttu-id="d4fb6-109">範例 1：將 DSC 節點組配置導入自動化</span><span class="sxs-lookup"><span data-stu-id="d4fb6-109">Example 1: Import a DSC node configuration into Automation</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

<span data-ttu-id="d4fb6-110">此命令會從名為 webserver.mof 的檔案中，將 DSC 節點組式組入名為 Contoso17 的自動化帳戶，在 DSC 組式 ContosoConfiguration 下。</span><span class="sxs-lookup"><span data-stu-id="d4fb6-110">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="d4fb6-111">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="d4fb6-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="d4fb6-112">如果有名為 ContosoConfiguration.webserver 的現有 DSC 節點組式，此命令會取代它。</span><span class="sxs-lookup"><span data-stu-id="d4fb6-112">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command replaces it.</span></span>

### <span data-ttu-id="d4fb6-113">範例 2：將 DSC 節點組式組入自動化，並建立新版，而不會覆寫現有的 NodeConfiguration。</span><span class="sxs-lookup"><span data-stu-id="d4fb6-113">Example 2: Import a DSC node configuration into Automation and create a new build version and not overwrite existing NodeConfiguration.</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="d4fb6-114">此命令會從名為 webserver.mof 的檔案中，將 DSC 節點組式組入名為 Contoso17 的自動化帳戶，在 DSC 組式 ContosoConfiguration 下。</span><span class="sxs-lookup"><span data-stu-id="d4fb6-114">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="d4fb6-115">命令會指定 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="d4fb6-115">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="d4fb6-116">如果有名為 ContosoConfiguration.webserver 的現有 DSC 節點組配置，此命令會新增名稱為 ContosoConfiguration[2].webserver 的新建立版本。</span><span class="sxs-lookup"><span data-stu-id="d4fb6-116">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command adds a new build version with the name ContosoConfiguration[2].webserver.</span></span>

## <span data-ttu-id="d4fb6-117">參數</span><span class="sxs-lookup"><span data-stu-id="d4fb6-117">PARAMETERS</span></span>

### <span data-ttu-id="d4fb6-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d4fb6-118">-AutomationAccountName</span></span>
<span data-ttu-id="d4fb6-119">指定此 Cmdlet 將 DSC 節點群組原則導入的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d4fb6-119">Specifies the name of the Automation account into which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="d4fb6-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d4fb6-120">-ConfigurationName</span></span>
<span data-ttu-id="d4fb6-121">指定自動化中的 DSC 組式組名，以做為節點組式要輸入的命名空間和容器。</span><span class="sxs-lookup"><span data-stu-id="d4fb6-121">Specifies the name of a DSC configuration in Automation to use as the namespace and container for the node configuration to import.</span></span>

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

### <span data-ttu-id="d4fb6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4fb6-122">-DefaultProfile</span></span>
<span data-ttu-id="d4fb6-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="d4fb6-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4fb6-124">-強制</span><span class="sxs-lookup"><span data-stu-id="d4fb6-124">-Force</span></span>
<span data-ttu-id="d4fb6-125">表示此 Cmdlet 取代 Automation 中現有的 DSC 節點組。</span><span class="sxs-lookup"><span data-stu-id="d4fb6-125">Indicates that this cmdlet replaces an existing DSC node configuration in Automation.</span></span>

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

### <span data-ttu-id="d4fb6-126">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="d4fb6-126">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="d4fb6-127">建立新節點組組建版本。</span><span class="sxs-lookup"><span data-stu-id="d4fb6-127">Creates a new Node Configuration build version.</span></span>

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

### <span data-ttu-id="d4fb6-128">-路徑</span><span class="sxs-lookup"><span data-stu-id="d4fb6-128">-Path</span></span>
<span data-ttu-id="d4fb6-129">指定此 Cmdlet 所導入的 MOF 群組原則檔路徑。</span><span class="sxs-lookup"><span data-stu-id="d4fb6-129">Specifies the path of the MOF configuration document that this cmdlet imports.</span></span>

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

### <span data-ttu-id="d4fb6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4fb6-130">-ResourceGroupName</span></span>
<span data-ttu-id="d4fb6-131">指定此 Cmdlet 所輸入 DSC 節點群組原則的資源組名。</span><span class="sxs-lookup"><span data-stu-id="d4fb6-131">Specifies the name of a resource group for which this cmdlet imports a DSC node configuration.</span></span>

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

### <span data-ttu-id="d4fb6-132">-確認</span><span class="sxs-lookup"><span data-stu-id="d4fb6-132">-Confirm</span></span>
<span data-ttu-id="d4fb6-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d4fb6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4fb6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4fb6-134">-WhatIf</span></span>
<span data-ttu-id="d4fb6-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d4fb6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4fb6-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d4fb6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4fb6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4fb6-137">CommonParameters</span></span>
<span data-ttu-id="d4fb6-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d4fb6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4fb6-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d4fb6-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4fb6-140">輸入</span><span class="sxs-lookup"><span data-stu-id="d4fb6-140">INPUTS</span></span>

### <span data-ttu-id="d4fb6-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d4fb6-141">System.String</span></span>

## <span data-ttu-id="d4fb6-142">輸出</span><span class="sxs-lookup"><span data-stu-id="d4fb6-142">OUTPUTS</span></span>

### <span data-ttu-id="d4fb6-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4fb6-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span></span>

## <span data-ttu-id="d4fb6-144">筆記</span><span class="sxs-lookup"><span data-stu-id="d4fb6-144">NOTES</span></span>

## <span data-ttu-id="d4fb6-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4fb6-145">RELATED LINKS</span></span>

[<span data-ttu-id="d4fb6-146">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4fb6-146">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="d4fb6-147">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4fb6-147">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)


