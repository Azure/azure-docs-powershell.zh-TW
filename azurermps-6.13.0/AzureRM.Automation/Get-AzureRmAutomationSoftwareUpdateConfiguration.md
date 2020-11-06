---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: f4d17fa6cdcb64aab2ab373420891f686facfdf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453912"
---
# <span data-ttu-id="6f43e-101">Get-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="6f43e-101">Get-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="6f43e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f43e-102">SYNOPSIS</span></span>
<span data-ttu-id="6f43e-103">取得 azure 自動化軟體更新設定的清單。</span><span class="sxs-lookup"><span data-stu-id="6f43e-103">Gets a list of azure automation software update configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f43e-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f43e-104">SYNTAX</span></span>

### <span data-ttu-id="6f43e-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="6f43e-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f43e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6f43e-106">ByName</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f43e-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="6f43e-107">ByVMId</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f43e-108">說明</span><span class="sxs-lookup"><span data-stu-id="6f43e-108">DESCRIPTION</span></span>
<span data-ttu-id="6f43e-109">Get-AzureRmAutomationSoftwareUpdateConfiguration 會傳回軟體更新配置的清單。</span><span class="sxs-lookup"><span data-stu-id="6f43e-109">The Get-AzureRmAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="6f43e-110">若要取得特定軟體更新設定，請指定 name 參數。</span><span class="sxs-lookup"><span data-stu-id="6f43e-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="6f43e-111">您也可以透過指定此虛擬機器的 azure 資源識別碼來列出針對特定 azure 虛擬機器的軟體更新設定。</span><span class="sxs-lookup"><span data-stu-id="6f43e-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="6f43e-112">示例</span><span class="sxs-lookup"><span data-stu-id="6f43e-112">EXAMPLES</span></span>

### <span data-ttu-id="6f43e-113">範例1</span><span class="sxs-lookup"><span data-stu-id="6f43e-113">Example 1</span></span>
<span data-ttu-id="6f43e-114">依名稱取得 azure 自動化軟體更新設定。</span><span class="sxs-lookup"><span data-stu-id="6f43e-114">Get an azure automation software update configuration by name.</span></span>

```powershell
PS C:\> Get-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyWeeklySchedule"

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Succeeded
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:37 AM +00:00
Description           :
```

## <span data-ttu-id="6f43e-115">參數</span><span class="sxs-lookup"><span data-stu-id="6f43e-115">PARAMETERS</span></span>

### <span data-ttu-id="6f43e-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6f43e-116">-AutomationAccountName</span></span>
<span data-ttu-id="6f43e-117">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="6f43e-117">The automation account name.</span></span>

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

### <span data-ttu-id="6f43e-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="6f43e-118">-AzureVMResourceId</span></span>
<span data-ttu-id="6f43e-119">虛擬機器的 Azure 資源 Id。</span><span class="sxs-lookup"><span data-stu-id="6f43e-119">Azure resource Id of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVMId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f43e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f43e-120">-DefaultProfile</span></span>
<span data-ttu-id="6f43e-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f43e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f43e-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f43e-122">-Name</span></span>
<span data-ttu-id="6f43e-123">軟體更新配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f43e-123">Name of the software update configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f43e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f43e-124">-ResourceGroupName</span></span>
<span data-ttu-id="6f43e-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f43e-125">The resource group name.</span></span>

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

### <span data-ttu-id="6f43e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f43e-126">CommonParameters</span></span>
<span data-ttu-id="6f43e-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f43e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f43e-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6f43e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f43e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="6f43e-129">INPUTS</span></span>

### <span data-ttu-id="6f43e-130">System.object</span><span class="sxs-lookup"><span data-stu-id="6f43e-130">System.String</span></span>

## <span data-ttu-id="6f43e-131">輸出</span><span class="sxs-lookup"><span data-stu-id="6f43e-131">OUTPUTS</span></span>

### <span data-ttu-id="6f43e-132">UpdateManagement SoftwareUpdateConfiguration 中的 []</span><span class="sxs-lookup"><span data-stu-id="6f43e-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="6f43e-133">筆記</span><span class="sxs-lookup"><span data-stu-id="6f43e-133">NOTES</span></span>

## <span data-ttu-id="6f43e-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f43e-134">RELATED LINKS</span></span>
