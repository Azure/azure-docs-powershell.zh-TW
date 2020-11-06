---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 10e04dc24c34ba60186c8166e2626524fcc60a37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444071"
---
# <span data-ttu-id="3e2da-101">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e2da-101">Get-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="3e2da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3e2da-102">SYNOPSIS</span></span>
<span data-ttu-id="3e2da-103">從自動化取得 DSC 配置。</span><span class="sxs-lookup"><span data-stu-id="3e2da-103">Gets DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e2da-104">句法</span><span class="sxs-lookup"><span data-stu-id="3e2da-104">SYNTAX</span></span>

### <span data-ttu-id="3e2da-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="3e2da-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e2da-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3e2da-106">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e2da-107">說明</span><span class="sxs-lookup"><span data-stu-id="3e2da-107">DESCRIPTION</span></span>
<span data-ttu-id="3e2da-108">**AzureRmAutomationDscConfiguration** Cmdlet 會從 Azure 自動化 (DSC) 配置中取得受 Ap 所需的狀態設定。</span><span class="sxs-lookup"><span data-stu-id="3e2da-108">The **Get-AzureRmAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="3e2da-109">示例</span><span class="sxs-lookup"><span data-stu-id="3e2da-109">EXAMPLES</span></span>

### <span data-ttu-id="3e2da-110">範例1：取得所有的 DSC 設定</span><span class="sxs-lookup"><span data-stu-id="3e2da-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="3e2da-111">這個命令會針對自動化帳戶（名為 Contoso17）中的所有 DSC 設定，取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3e2da-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="3e2da-112">範例2：依名稱取得 DSC 設定</span><span class="sxs-lookup"><span data-stu-id="3e2da-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="3e2da-113">這個命令會針對自動化帳戶（名為 Contoso17）中名為 MyConfiguration 的 DSC 配置取得中繼資料。</span><span class="sxs-lookup"><span data-stu-id="3e2da-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="3e2da-114">參數</span><span class="sxs-lookup"><span data-stu-id="3e2da-114">PARAMETERS</span></span>

### <span data-ttu-id="3e2da-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3e2da-115">-AutomationAccountName</span></span>
<span data-ttu-id="3e2da-116">指定包含此 Cmdlet 所取得的 DSC 設定的自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="3e2da-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3e2da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e2da-117">-DefaultProfile</span></span>
<span data-ttu-id="3e2da-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3e2da-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e2da-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="3e2da-119">-Name</span></span>
<span data-ttu-id="3e2da-120">指定此 Cmdlet 取得的 DSC 配置名稱。</span><span class="sxs-lookup"><span data-stu-id="3e2da-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="3e2da-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e2da-121">-ResourceGroupName</span></span>
<span data-ttu-id="3e2da-122">指定此 Cmdlet 取得 DSC 設定之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e2da-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="3e2da-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e2da-123">CommonParameters</span></span>
<span data-ttu-id="3e2da-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3e2da-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e2da-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3e2da-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e2da-126">輸入</span><span class="sxs-lookup"><span data-stu-id="3e2da-126">INPUTS</span></span>

### <span data-ttu-id="3e2da-127">System.object</span><span class="sxs-lookup"><span data-stu-id="3e2da-127">System.String</span></span>

## <span data-ttu-id="3e2da-128">輸出</span><span class="sxs-lookup"><span data-stu-id="3e2da-128">OUTPUTS</span></span>

### <span data-ttu-id="3e2da-129">DscConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3e2da-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="3e2da-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3e2da-130">NOTES</span></span>

## <span data-ttu-id="3e2da-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e2da-131">RELATED LINKS</span></span>

[<span data-ttu-id="3e2da-132">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e2da-132">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="3e2da-133">匯入-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3e2da-133">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


