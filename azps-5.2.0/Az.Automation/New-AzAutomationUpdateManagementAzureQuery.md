---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationupdatemanagementazurequery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
ms.openlocfilehash: 68139ff184df62583b3077a38fbc2e26fd5eae09
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98285283"
---
# <span data-ttu-id="db990-101">New-AzAutomationUpdateManagementAzureQuery</span><span class="sxs-lookup"><span data-stu-id="db990-101">New-AzAutomationUpdateManagementAzureQuery</span></span>

## <span data-ttu-id="db990-102">摘要</span><span class="sxs-lookup"><span data-stu-id="db990-102">SYNOPSIS</span></span>
<span data-ttu-id="db990-103">建立 azure 自動化軟體更新 configuration azure 查詢物件。</span><span class="sxs-lookup"><span data-stu-id="db990-103">Creates azure automation software update configuration azure query object.</span></span>

## <span data-ttu-id="db990-104">句法</span><span class="sxs-lookup"><span data-stu-id="db990-104">SYNTAX</span></span>

```
New-AzAutomationUpdateManagementAzureQuery -Scope <String[]> [-Location <String[]>] [-Tag <Hashtable>]
 [-FilterOperator <TagOperators>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db990-105">說明</span><span class="sxs-lookup"><span data-stu-id="db990-105">DESCRIPTION</span></span>
<span data-ttu-id="db990-106">建立將用來建立軟體更新設定的軟體更新 configuration azure 查詢物件，該設定將會在排程上執行，以更新 azure 虛擬機器清單的動態解析清單。</span><span class="sxs-lookup"><span data-stu-id="db990-106">Creates a software update configuration azure queries object that will be used to create a software update configuration which will runs on a schedule to update a list of dynamically resolved list of azure virtual machines.</span></span>

## <span data-ttu-id="db990-107">示例</span><span class="sxs-lookup"><span data-stu-id="db990-107">EXAMPLES</span></span>

### <span data-ttu-id="db990-108">範例1</span><span class="sxs-lookup"><span data-stu-id="db990-108">Example 1</span></span>
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

## <span data-ttu-id="db990-109">參數</span><span class="sxs-lookup"><span data-stu-id="db990-109">PARAMETERS</span></span>

### <span data-ttu-id="db990-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="db990-110">-AutomationAccountName</span></span>
<span data-ttu-id="db990-111">自動化帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="db990-111">The automation account name.</span></span>

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

### <span data-ttu-id="db990-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db990-112">-DefaultProfile</span></span>
<span data-ttu-id="db990-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="db990-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db990-114">-FilterOperator</span><span class="sxs-lookup"><span data-stu-id="db990-114">-FilterOperator</span></span>
<span data-ttu-id="db990-115">標記篩選運算子。</span><span class="sxs-lookup"><span data-stu-id="db990-115">Tag filter operator.</span></span>

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

### <span data-ttu-id="db990-116">-位置</span><span class="sxs-lookup"><span data-stu-id="db990-116">-Location</span></span>
<span data-ttu-id="db990-117">Azure 虛擬機器的位置清單。</span><span class="sxs-lookup"><span data-stu-id="db990-117">List of locations for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="db990-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db990-118">-ResourceGroupName</span></span>
<span data-ttu-id="db990-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="db990-119">The resource group name.</span></span>

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

### <span data-ttu-id="db990-120">-範圍</span><span class="sxs-lookup"><span data-stu-id="db990-120">-Scope</span></span>
<span data-ttu-id="db990-121">Azure 虛擬機器的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="db990-121">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="db990-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="db990-122">-Tag</span></span>
<span data-ttu-id="db990-123">Azure 虛擬機器的標記。</span><span class="sxs-lookup"><span data-stu-id="db990-123">Tag for azure virtual machines.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="db990-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db990-124">CommonParameters</span></span>
<span data-ttu-id="db990-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="db990-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="db990-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="db990-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db990-127">輸入</span><span class="sxs-lookup"><span data-stu-id="db990-127">INPUTS</span></span>

### <span data-ttu-id="db990-128">System.object []</span><span class="sxs-lookup"><span data-stu-id="db990-128">System.String[]</span></span>

### <span data-ttu-id="db990-129">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="db990-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="db990-130">UpdateManagement TagOperators 中的 []</span><span class="sxs-lookup"><span data-stu-id="db990-130">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.TagOperators</span></span>

### <span data-ttu-id="db990-131">System.object</span><span class="sxs-lookup"><span data-stu-id="db990-131">System.String</span></span>

## <span data-ttu-id="db990-132">輸出</span><span class="sxs-lookup"><span data-stu-id="db990-132">OUTPUTS</span></span>

### <span data-ttu-id="db990-133">UpdateManagement AzureQueryProperties 中的 []</span><span class="sxs-lookup"><span data-stu-id="db990-133">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties</span></span>

## <span data-ttu-id="db990-134">筆記</span><span class="sxs-lookup"><span data-stu-id="db990-134">NOTES</span></span>

## <span data-ttu-id="db990-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="db990-135">RELATED LINKS</span></span>
