---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: b139ed5b67bbc36bad45ab2528ed74299d40c1b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906350"
---
# <span data-ttu-id="3ceab-101">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ceab-101">Get-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="3ceab-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3ceab-102">SYNOPSIS</span></span>
<span data-ttu-id="3ceab-103">在自動化中獲得 DSC 節點配置的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3ceab-103">Gets metadata for DSC node configurations in Automation.</span></span>

## <span data-ttu-id="3ceab-104">語法</span><span class="sxs-lookup"><span data-stu-id="3ceab-104">SYNTAX</span></span>

### <span data-ttu-id="3ceab-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="3ceab-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ceab-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3ceab-106">ByNodeConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ceab-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3ceab-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ceab-108">描述</span><span class="sxs-lookup"><span data-stu-id="3ceab-108">DESCRIPTION</span></span>
<span data-ttu-id="3ceab-109">**Get-AzAutomationDscNodeConfiguration Cmdlet** 會取得 Azure Automation 中 APS 所需狀態組態 (DSC) 節點配置的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3ceab-109">The **Get-AzAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="3ceab-110">自動化會以受管理的物件格式將 DSC 節點組 (MOF) 群組原則檔。</span><span class="sxs-lookup"><span data-stu-id="3ceab-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="3ceab-111">例子</span><span class="sxs-lookup"><span data-stu-id="3ceab-111">EXAMPLES</span></span>

### <span data-ttu-id="3ceab-112">範例 1：取得所有 DSC 節點組配置</span><span class="sxs-lookup"><span data-stu-id="3ceab-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="3ceab-113">此命令會獲得自動化帳戶中所有 DSC 節點配置的中繼資料，名稱為 Contoso17。</span><span class="sxs-lookup"><span data-stu-id="3ceab-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="3ceab-114">範例 2：取得 DSC 組配置的所有 DSC 節點組</span><span class="sxs-lookup"><span data-stu-id="3ceab-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="3ceab-115">此命令會針對名為 Contoso17 的自動化帳戶內所有 DSC 節點組配置的中繼資料，而由名稱為 ContosoConfiguration 的 DSC 組式產生。</span><span class="sxs-lookup"><span data-stu-id="3ceab-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="3ceab-116">範例 3：根據名稱取得 DSC 節點組</span><span class="sxs-lookup"><span data-stu-id="3ceab-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="3ceab-117">此命令會針對名為 Contoso17 的自動化帳戶中名稱為 ContosoConfiguration.webserver 的 DSC 節點組式，獲得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3ceab-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3ceab-118">參數</span><span class="sxs-lookup"><span data-stu-id="3ceab-118">PARAMETERS</span></span>

### <span data-ttu-id="3ceab-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3ceab-119">-AutomationAccountName</span></span>
<span data-ttu-id="3ceab-120">指定包含此 Cmdlet 可收到中繼資料之 DSC 節點配置的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3ceab-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="3ceab-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3ceab-121">-ConfigurationName</span></span>
<span data-ttu-id="3ceab-122">指定此 Cmdlet 會獲得節點組配置中繼資料的 DSC 群組原則名稱。</span><span class="sxs-lookup"><span data-stu-id="3ceab-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ceab-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ceab-123">-DefaultProfile</span></span>
<span data-ttu-id="3ceab-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="3ceab-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ceab-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="3ceab-125">-Name</span></span>
<span data-ttu-id="3ceab-126">指定此 Cmdlet 會獲得中繼資料的 DSC 節點組名。</span><span class="sxs-lookup"><span data-stu-id="3ceab-126">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeConfigurationName
Aliases: NodeConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ceab-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ceab-127">-ResourceGroupName</span></span>
<span data-ttu-id="3ceab-128">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ceab-128">Specifies the name of a resource group.</span></span>
<span data-ttu-id="3ceab-129">此 Cmdlet 會在此參數指定的資源群組中，獲得 DSC 節點配置的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3ceab-129">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3ceab-130">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="3ceab-130">-RollupStatus</span></span>
<span data-ttu-id="3ceab-131">指定此 Cmdlet 所獲得 DSC 節點配置的匯總狀態。</span><span class="sxs-lookup"><span data-stu-id="3ceab-131">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="3ceab-132">有效的值為：</span><span class="sxs-lookup"><span data-stu-id="3ceab-132">Valid values are:</span></span> 
- <span data-ttu-id="3ceab-133">壞</span><span class="sxs-lookup"><span data-stu-id="3ceab-133">Bad</span></span> 
- <span data-ttu-id="3ceab-134">好</span><span class="sxs-lookup"><span data-stu-id="3ceab-134">Good</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Good, Bad

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ceab-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ceab-135">CommonParameters</span></span>
<span data-ttu-id="3ceab-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3ceab-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ceab-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="3ceab-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ceab-138">輸入</span><span class="sxs-lookup"><span data-stu-id="3ceab-138">INPUTS</span></span>

### <span data-ttu-id="3ceab-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3ceab-139">System.String</span></span>

## <span data-ttu-id="3ceab-140">輸出</span><span class="sxs-lookup"><span data-stu-id="3ceab-140">OUTPUTS</span></span>

### <span data-ttu-id="3ceab-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="3ceab-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="3ceab-142">筆記</span><span class="sxs-lookup"><span data-stu-id="3ceab-142">NOTES</span></span>

## <span data-ttu-id="3ceab-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ceab-143">RELATED LINKS</span></span>

[<span data-ttu-id="3ceab-144">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="3ceab-144">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)


