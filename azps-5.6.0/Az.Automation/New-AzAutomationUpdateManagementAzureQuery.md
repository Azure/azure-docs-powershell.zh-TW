---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationupdatemanagementazurequery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
ms.openlocfilehash: 90534fa058da876a09456d421bfa59d9906d6055
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903045"
---
# <span data-ttu-id="0dbf0-101">New-AzAutomationUpdateManagementAzureQuery</span><span class="sxs-lookup"><span data-stu-id="0dbf0-101">New-AzAutomationUpdateManagementAzureQuery</span></span>

## <span data-ttu-id="0dbf0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0dbf0-102">SYNOPSIS</span></span>
<span data-ttu-id="0dbf0-103">建立 Azure 自動化軟體更新組組 Azure 查詢物件。</span><span class="sxs-lookup"><span data-stu-id="0dbf0-103">Creates azure automation software update configuration azure query object.</span></span>

## <span data-ttu-id="0dbf0-104">語法</span><span class="sxs-lookup"><span data-stu-id="0dbf0-104">SYNTAX</span></span>

```
New-AzAutomationUpdateManagementAzureQuery -Scope <String[]> [-Location <String[]>] [-Tag <Hashtable>]
 [-FilterOperator <TagOperators>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0dbf0-105">描述</span><span class="sxs-lookup"><span data-stu-id="0dbf0-105">DESCRIPTION</span></span>
<span data-ttu-id="0dbf0-106">建立軟體更新組式 azure 查詢物件，用來建立軟體更新組式，並排程執行以更新 Azure 虛擬機器動態解析清單清單。</span><span class="sxs-lookup"><span data-stu-id="0dbf0-106">Creates a software update configuration azure queries object that will be used to create a software update configuration which will runs on a schedule to update a list of dynamically resolved list of azure virtual machines.</span></span>

## <span data-ttu-id="0dbf0-107">例子</span><span class="sxs-lookup"><span data-stu-id="0dbf0-107">EXAMPLES</span></span>

### <span data-ttu-id="0dbf0-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="0dbf0-108">Example 1</span></span>
```powershell
PS C:\>$query1Scope = @(        
"/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/resourceGroupName",
"/subscriptions/32e2445a-0984-4fa5-86a4-0280d76c4b2d/"
    )
PS C:\>$query1Location =@("Japan East", "UK South")
PS C:\>$query1FilterOperator = "All"
PS C:\>$tag1 = @{"tag1"= @("tag1Value1", "tag1Value2")}
PS C:\>$tag1.add("tag2", "tag2Value")
PS C:\>$azq = New-AzAutomationUpdateManagementAzureQuery -ResourceGroupName "mygroup" `
                                       -AutomationAccountName "myaccount" `
                                       -Scope $query1Scope `
                                       -Location $query1Location `
                                       -Tag $tag1
PS C:\>$AzureQueries = @($azq)
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"

PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `                                                 
                                                 -AzureQuery $AzureQueries `
                                                 -IncludedUpdateClassification Critical `
                                                 -Duration $duration

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Provisioning
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:27 AM +00:00
Description           :

```

## <span data-ttu-id="0dbf0-109">參數</span><span class="sxs-lookup"><span data-stu-id="0dbf0-109">PARAMETERS</span></span>

### <span data-ttu-id="0dbf0-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0dbf0-110">-AutomationAccountName</span></span>
<span data-ttu-id="0dbf0-111">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="0dbf0-111">The automation account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dbf0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dbf0-112">-DefaultProfile</span></span>
<span data-ttu-id="0dbf0-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0dbf0-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dbf0-114">-FilterOperator</span><span class="sxs-lookup"><span data-stu-id="0dbf0-114">-FilterOperator</span></span>
<span data-ttu-id="0dbf0-115">標記篩選運算子。</span><span class="sxs-lookup"><span data-stu-id="0dbf0-115">Tag filter operator.</span></span>

```yaml
Type: TagOperators
Parameter Sets: (All)
Aliases:
Accepted values: All, Any

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="0dbf0-116">-位置</span><span class="sxs-lookup"><span data-stu-id="0dbf0-116">-Location</span></span>
<span data-ttu-id="0dbf0-117">Azure 虛擬機器的位置清單。</span><span class="sxs-lookup"><span data-stu-id="0dbf0-117">List of locations for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="0dbf0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dbf0-118">-ResourceGroupName</span></span>
<span data-ttu-id="0dbf0-119">資源組名。</span><span class="sxs-lookup"><span data-stu-id="0dbf0-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0dbf0-120">-範圍</span><span class="sxs-lookup"><span data-stu-id="0dbf0-120">-Scope</span></span>
<span data-ttu-id="0dbf0-121">Azure 虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0dbf0-121">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="0dbf0-122">-標記</span><span class="sxs-lookup"><span data-stu-id="0dbf0-122">-Tag</span></span>
<span data-ttu-id="0dbf0-123">Azure 虛擬機器的標記。</span><span class="sxs-lookup"><span data-stu-id="0dbf0-123">Tag for azure virtual machines.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="0dbf0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dbf0-124">CommonParameters</span></span>
<span data-ttu-id="0dbf0-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0dbf0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0dbf0-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0dbf0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dbf0-127">輸入</span><span class="sxs-lookup"><span data-stu-id="0dbf0-127">INPUTS</span></span>

### <span data-ttu-id="0dbf0-128">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0dbf0-128">System.String[]</span></span>

### <span data-ttu-id="0dbf0-129">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0dbf0-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0dbf0-130">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.TagOperators</span><span class="sxs-lookup"><span data-stu-id="0dbf0-130">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.TagOperators</span></span>

### <span data-ttu-id="0dbf0-131">System.String</span><span class="sxs-lookup"><span data-stu-id="0dbf0-131">System.String</span></span>

## <span data-ttu-id="0dbf0-132">輸出</span><span class="sxs-lookup"><span data-stu-id="0dbf0-132">OUTPUTS</span></span>

### <span data-ttu-id="0dbf0-133">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties</span><span class="sxs-lookup"><span data-stu-id="0dbf0-133">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties</span></span>

## <span data-ttu-id="0dbf0-134">筆記</span><span class="sxs-lookup"><span data-stu-id="0dbf0-134">NOTES</span></span>

## <span data-ttu-id="0dbf0-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="0dbf0-135">RELATED LINKS</span></span>
