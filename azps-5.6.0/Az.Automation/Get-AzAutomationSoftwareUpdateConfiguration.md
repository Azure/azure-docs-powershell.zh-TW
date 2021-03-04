---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: 99f2c14cbc3c3f652df062bb3bf806e89ca05f06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917470"
---
# <span data-ttu-id="e8050-101">Get-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8050-101">Get-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="e8050-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e8050-102">SYNOPSIS</span></span>
<span data-ttu-id="e8050-103">獲得 Azure 自動化軟體更新組配置的清單。</span><span class="sxs-lookup"><span data-stu-id="e8050-103">Gets a list of azure automation software update configurations.</span></span>

## <span data-ttu-id="e8050-104">語法</span><span class="sxs-lookup"><span data-stu-id="e8050-104">SYNTAX</span></span>

### <span data-ttu-id="e8050-105">根據預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="e8050-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8050-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e8050-106">ByName</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8050-107">ByMSID</span><span class="sxs-lookup"><span data-stu-id="e8050-107">ByVMId</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8050-108">描述</span><span class="sxs-lookup"><span data-stu-id="e8050-108">DESCRIPTION</span></span>
<span data-ttu-id="e8050-109">此Get-AzAutomationSoftwareUpdateConfiguration會返回軟體更新組配置清單。</span><span class="sxs-lookup"><span data-stu-id="e8050-109">The Get-AzAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="e8050-110">若要取得特定的軟體更新設定，請指定名稱參數。</span><span class="sxs-lookup"><span data-stu-id="e8050-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="e8050-111">您也可以指定此虛擬機器的 Azure 資源識別碼，以列出特定 Azure 虛擬機器的軟體更新群組原則。</span><span class="sxs-lookup"><span data-stu-id="e8050-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="e8050-112">例子</span><span class="sxs-lookup"><span data-stu-id="e8050-112">EXAMPLES</span></span>

### <span data-ttu-id="e8050-113">範例 1</span><span class="sxs-lookup"><span data-stu-id="e8050-113">Example 1</span></span>
<span data-ttu-id="e8050-114">取得 Azure 自動化軟體更新的組名。</span><span class="sxs-lookup"><span data-stu-id="e8050-114">Get an azure automation software update configuration by name.</span></span>

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

## <span data-ttu-id="e8050-115">參數</span><span class="sxs-lookup"><span data-stu-id="e8050-115">PARAMETERS</span></span>

### <span data-ttu-id="e8050-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e8050-116">-AutomationAccountName</span></span>
<span data-ttu-id="e8050-117">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="e8050-117">The automation account name.</span></span>

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

### <span data-ttu-id="e8050-118">-AzureEVResourceId</span><span class="sxs-lookup"><span data-stu-id="e8050-118">-AzureVMResourceId</span></span>
<span data-ttu-id="e8050-119">虛擬機器的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e8050-119">Azure resource Id of the virtual machine.</span></span>

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

### <span data-ttu-id="e8050-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8050-120">-DefaultProfile</span></span>
<span data-ttu-id="e8050-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e8050-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8050-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="e8050-122">-Name</span></span>
<span data-ttu-id="e8050-123">軟體更新組名。</span><span class="sxs-lookup"><span data-stu-id="e8050-123">Name of the software update configuration.</span></span>

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

### <span data-ttu-id="e8050-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8050-124">-ResourceGroupName</span></span>
<span data-ttu-id="e8050-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="e8050-125">The resource group name.</span></span>

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

### <span data-ttu-id="e8050-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8050-126">CommonParameters</span></span>
<span data-ttu-id="e8050-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e8050-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8050-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="e8050-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8050-129">輸入</span><span class="sxs-lookup"><span data-stu-id="e8050-129">INPUTS</span></span>

### <span data-ttu-id="e8050-130">System.String</span><span class="sxs-lookup"><span data-stu-id="e8050-130">System.String</span></span>

## <span data-ttu-id="e8050-131">輸出</span><span class="sxs-lookup"><span data-stu-id="e8050-131">OUTPUTS</span></span>

### <span data-ttu-id="e8050-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="e8050-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="e8050-133">筆記</span><span class="sxs-lookup"><span data-stu-id="e8050-133">NOTES</span></span>

## <span data-ttu-id="e8050-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="e8050-134">RELATED LINKS</span></span>
