---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: a3b0b53146703a13f0ae8ea1627d2d9722c85eeb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613801"
---
# <span data-ttu-id="13f4b-101">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="13f4b-101">Get-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="13f4b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13f4b-102">SYNOPSIS</span></span>
<span data-ttu-id="13f4b-103">取得自動化中的 DSC 節點配置中繼資料。</span><span class="sxs-lookup"><span data-stu-id="13f4b-103">Gets metadata for DSC node configurations in Automation.</span></span>

## <span data-ttu-id="13f4b-104">句法</span><span class="sxs-lookup"><span data-stu-id="13f4b-104">SYNTAX</span></span>

### <span data-ttu-id="13f4b-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="13f4b-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13f4b-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="13f4b-106">ByNodeConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="13f4b-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="13f4b-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13f4b-108">說明</span><span class="sxs-lookup"><span data-stu-id="13f4b-108">DESCRIPTION</span></span>
<span data-ttu-id="13f4b-109">**AzAutomationDscNodeConfiguration** Cmdlet 會取得 Azure 自動化中 (DSC) 節點設定的 Ap 所需狀態設定的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="13f4b-109">The **Get-AzAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="13f4b-110">自動化會將 DSC 節點設定儲存為受管理的物件格式， (MOF) 設定檔。</span><span class="sxs-lookup"><span data-stu-id="13f4b-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="13f4b-111">示例</span><span class="sxs-lookup"><span data-stu-id="13f4b-111">EXAMPLES</span></span>

### <span data-ttu-id="13f4b-112">範例1：取得所有的 DSC 節點設定</span><span class="sxs-lookup"><span data-stu-id="13f4b-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="13f4b-113">這個命令會針對自動化帳戶（名為 Contoso17）中的所有 DSC 節點配置取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="13f4b-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="13f4b-114">範例2：取得 DSC 設定的所有 DSC 節點設定</span><span class="sxs-lookup"><span data-stu-id="13f4b-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="13f4b-115">這個命令會在名為 Contoso17 的自動化帳戶中，取得名為 ContosoConfiguration 產生的 DSC 設定的所有 DSC 節點配置的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="13f4b-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="13f4b-116">範例3：依名稱取得 DSC 節點設定</span><span class="sxs-lookup"><span data-stu-id="13f4b-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="13f4b-117">這個命令會以名為 Contoso17 的自動化帳戶中的名稱 ContosoConfiguration 來取得 DSC 節點配置的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="13f4b-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="13f4b-118">參數</span><span class="sxs-lookup"><span data-stu-id="13f4b-118">PARAMETERS</span></span>

### <span data-ttu-id="13f4b-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="13f4b-119">-AutomationAccountName</span></span>
<span data-ttu-id="13f4b-120">指定包含此 Cmdlet 取得中繼資料之 DSC 節點配置之自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="13f4b-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="13f4b-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="13f4b-121">-ConfigurationName</span></span>
<span data-ttu-id="13f4b-122">指定此 Cmdlet 取得節點配置中繼資料之 DSC 配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="13f4b-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

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

### <span data-ttu-id="13f4b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13f4b-123">-DefaultProfile</span></span>
<span data-ttu-id="13f4b-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="13f4b-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13f4b-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="13f4b-125">-Name</span></span>
<span data-ttu-id="13f4b-126">指定此 Cmdlet 取得中繼資料的 DSC 節點配置名稱。</span><span class="sxs-lookup"><span data-stu-id="13f4b-126">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="13f4b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13f4b-127">-ResourceGroupName</span></span>
<span data-ttu-id="13f4b-128">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="13f4b-128">Specifies the name of a resource group.</span></span>
<span data-ttu-id="13f4b-129">這個 Cmdlet 會取得此參數指定之資源群組中的 DSC 節點配置中繼資料。</span><span class="sxs-lookup"><span data-stu-id="13f4b-129">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="13f4b-130">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="13f4b-130">-RollupStatus</span></span>
<span data-ttu-id="13f4b-131">指定此 Cmdlet 取得的 DSC 節點配置的匯總狀態。</span><span class="sxs-lookup"><span data-stu-id="13f4b-131">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="13f4b-132">有效值為：</span><span class="sxs-lookup"><span data-stu-id="13f4b-132">Valid values are:</span></span> 
- <span data-ttu-id="13f4b-133">壞事</span><span class="sxs-lookup"><span data-stu-id="13f4b-133">Bad</span></span> 
- <span data-ttu-id="13f4b-134">良好</span><span class="sxs-lookup"><span data-stu-id="13f4b-134">Good</span></span>

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

### <span data-ttu-id="13f4b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13f4b-135">CommonParameters</span></span>
<span data-ttu-id="13f4b-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13f4b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13f4b-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="13f4b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13f4b-138">輸入</span><span class="sxs-lookup"><span data-stu-id="13f4b-138">INPUTS</span></span>

### <span data-ttu-id="13f4b-139">System.object</span><span class="sxs-lookup"><span data-stu-id="13f4b-139">System.String</span></span>

## <span data-ttu-id="13f4b-140">輸出</span><span class="sxs-lookup"><span data-stu-id="13f4b-140">OUTPUTS</span></span>

### <span data-ttu-id="13f4b-141">CompilationJob 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="13f4b-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="13f4b-142">筆記</span><span class="sxs-lookup"><span data-stu-id="13f4b-142">NOTES</span></span>

## <span data-ttu-id="13f4b-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="13f4b-143">RELATED LINKS</span></span>

[<span data-ttu-id="13f4b-144">匯入-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="13f4b-144">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)


