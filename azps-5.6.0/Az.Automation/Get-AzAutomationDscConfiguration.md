---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
ms.openlocfilehash: 82c853f6f18f12c1e7005a859a5df924d3555b79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912481"
---
# <span data-ttu-id="8cce8-101">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cce8-101">Get-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="8cce8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8cce8-102">SYNOPSIS</span></span>
<span data-ttu-id="8cce8-103">從自動化獲得 DSC 組配置。</span><span class="sxs-lookup"><span data-stu-id="8cce8-103">Gets DSC configurations from Automation.</span></span>

## <span data-ttu-id="8cce8-104">語法</span><span class="sxs-lookup"><span data-stu-id="8cce8-104">SYNTAX</span></span>

### <span data-ttu-id="8cce8-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="8cce8-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cce8-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8cce8-106">ByConfigurationName</span></span>
```
Get-AzAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cce8-107">描述</span><span class="sxs-lookup"><span data-stu-id="8cce8-107">DESCRIPTION</span></span>
<span data-ttu-id="8cce8-108">**Get-AzAutomationDscConfiguration Cmdlet** 會從 Azure Automation 取得 APS (DSC) 狀態組態。</span><span class="sxs-lookup"><span data-stu-id="8cce8-108">The **Get-AzAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="8cce8-109">例子</span><span class="sxs-lookup"><span data-stu-id="8cce8-109">EXAMPLES</span></span>

### <span data-ttu-id="8cce8-110">範例 1：取得所有 DSC 組配置</span><span class="sxs-lookup"><span data-stu-id="8cce8-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="8cce8-111">此命令會獲得自動化帳戶 Contoso17 中所有 DSC 配置的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="8cce8-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="8cce8-112">範例 2：根據名稱取得 DSC 組配置</span><span class="sxs-lookup"><span data-stu-id="8cce8-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="8cce8-113">此命令會針對名為 Contoso17 的自動化帳戶中名為 MyConfiguration 的 DSC 組式，獲得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="8cce8-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="8cce8-114">參數</span><span class="sxs-lookup"><span data-stu-id="8cce8-114">PARAMETERS</span></span>

### <span data-ttu-id="8cce8-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8cce8-115">-AutomationAccountName</span></span>
<span data-ttu-id="8cce8-116">指定包含此 Cmdlet 所獲得 DSC 配置的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8cce8-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8cce8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cce8-117">-DefaultProfile</span></span>
<span data-ttu-id="8cce8-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8cce8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cce8-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="8cce8-119">-Name</span></span>
<span data-ttu-id="8cce8-120">指定此 Cmdlet 所獲得 DSC 組組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8cce8-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cce8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cce8-121">-ResourceGroupName</span></span>
<span data-ttu-id="8cce8-122">指定此 Cmdlet 會獲得 DSC 群組原則的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8cce8-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="8cce8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cce8-123">CommonParameters</span></span>
<span data-ttu-id="8cce8-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8cce8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cce8-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="8cce8-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cce8-126">輸入</span><span class="sxs-lookup"><span data-stu-id="8cce8-126">INPUTS</span></span>

### <span data-ttu-id="8cce8-127">System.String</span><span class="sxs-lookup"><span data-stu-id="8cce8-127">System.String</span></span>

## <span data-ttu-id="8cce8-128">輸出</span><span class="sxs-lookup"><span data-stu-id="8cce8-128">OUTPUTS</span></span>

### <span data-ttu-id="8cce8-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cce8-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="8cce8-130">筆記</span><span class="sxs-lookup"><span data-stu-id="8cce8-130">NOTES</span></span>

## <span data-ttu-id="8cce8-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="8cce8-131">RELATED LINKS</span></span>

[<span data-ttu-id="8cce8-132">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cce8-132">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="8cce8-133">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cce8-133">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


