---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: af11442edfc5acb2d7e9683bc71d7d2e2c87bd5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136647"
---
# <span data-ttu-id="d638d-101">Get-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="d638d-101">Get-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="d638d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d638d-102">SYNOPSIS</span></span>
<span data-ttu-id="d638d-103">取得 azure 自動化軟體更新設定的清單。</span><span class="sxs-lookup"><span data-stu-id="d638d-103">Gets a list of azure automation software update configurations.</span></span>

## <span data-ttu-id="d638d-104">句法</span><span class="sxs-lookup"><span data-stu-id="d638d-104">SYNTAX</span></span>

### <span data-ttu-id="d638d-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="d638d-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d638d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d638d-106">ByName</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d638d-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="d638d-107">ByVMId</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d638d-108">說明</span><span class="sxs-lookup"><span data-stu-id="d638d-108">DESCRIPTION</span></span>
<span data-ttu-id="d638d-109">Get-AzAutomationSoftwareUpdateConfiguration 會傳回軟體更新配置的清單。</span><span class="sxs-lookup"><span data-stu-id="d638d-109">The Get-AzAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="d638d-110">若要取得特定軟體更新設定，請指定 name 參數。</span><span class="sxs-lookup"><span data-stu-id="d638d-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="d638d-111">您也可以透過指定此虛擬機器的 azure 資源識別碼來列出針對特定 azure 虛擬機器的軟體更新設定。</span><span class="sxs-lookup"><span data-stu-id="d638d-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="d638d-112">示例</span><span class="sxs-lookup"><span data-stu-id="d638d-112">EXAMPLES</span></span>

### <span data-ttu-id="d638d-113">範例1</span><span class="sxs-lookup"><span data-stu-id="d638d-113">Example 1</span></span>
<span data-ttu-id="d638d-114">依名稱取得 azure 自動化軟體更新設定。</span><span class="sxs-lookup"><span data-stu-id="d638d-114">Get an azure automation software update configuration by name.</span></span>

```powershell
PS C:\> Get-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyWeeklySchedule"

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

## <span data-ttu-id="d638d-115">參數</span><span class="sxs-lookup"><span data-stu-id="d638d-115">PARAMETERS</span></span>

### <span data-ttu-id="d638d-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d638d-116">-AutomationAccountName</span></span>
<span data-ttu-id="d638d-117">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="d638d-117">The automation account name.</span></span>

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

### <span data-ttu-id="d638d-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="d638d-118">-AzureVMResourceId</span></span>
<span data-ttu-id="d638d-119">虛擬機器的 Azure 資源 Id。</span><span class="sxs-lookup"><span data-stu-id="d638d-119">Azure resource Id of the virtual machine.</span></span>

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

### <span data-ttu-id="d638d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d638d-120">-DefaultProfile</span></span>
<span data-ttu-id="d638d-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d638d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d638d-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="d638d-122">-Name</span></span>
<span data-ttu-id="d638d-123">軟體更新配置的名稱。</span><span class="sxs-lookup"><span data-stu-id="d638d-123">Name of the software update configuration.</span></span>

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

### <span data-ttu-id="d638d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d638d-124">-ResourceGroupName</span></span>
<span data-ttu-id="d638d-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d638d-125">The resource group name.</span></span>

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

### <span data-ttu-id="d638d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d638d-126">CommonParameters</span></span>
<span data-ttu-id="d638d-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d638d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d638d-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d638d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d638d-129">輸入</span><span class="sxs-lookup"><span data-stu-id="d638d-129">INPUTS</span></span>

### <span data-ttu-id="d638d-130">System.object</span><span class="sxs-lookup"><span data-stu-id="d638d-130">System.String</span></span>

## <span data-ttu-id="d638d-131">輸出</span><span class="sxs-lookup"><span data-stu-id="d638d-131">OUTPUTS</span></span>

### <span data-ttu-id="d638d-132">UpdateManagement SoftwareUpdateConfiguration 中的 []</span><span class="sxs-lookup"><span data-stu-id="d638d-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="d638d-133">筆記</span><span class="sxs-lookup"><span data-stu-id="d638d-133">NOTES</span></span>

## <span data-ttu-id="d638d-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="d638d-134">RELATED LINKS</span></span>
