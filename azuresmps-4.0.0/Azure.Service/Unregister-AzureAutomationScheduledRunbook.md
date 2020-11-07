---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: EA7C1449-E11F-4AE8-A513-59BDCA38875D
online version: ''
schema: 2.0.0
ms.openlocfilehash: e432edd2469fa25519c12f0cd1f2dadb1d0dca2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93968033"
---
# <span data-ttu-id="5274a-101">Unregister-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="5274a-101">Unregister-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="5274a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5274a-102">SYNOPSIS</span></span>

<span data-ttu-id="5274a-103">移除 [runbook] 與 [排程] 之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="5274a-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="5274a-104">句法</span><span class="sxs-lookup"><span data-stu-id="5274a-104">SYNTAX</span></span>

### <span data-ttu-id="5274a-105">ByJobScheduleId (預設) </span><span class="sxs-lookup"><span data-stu-id="5274a-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5274a-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="5274a-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5274a-107">說明</span><span class="sxs-lookup"><span data-stu-id="5274a-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="5274a-108">**AzureAutomationScheduledRunbook** Cmdlet 會移除 Microsoft Azure 自動化 runbook 與排程之間的關聯，這會在排程觸發時停止 runbook 的啟動。</span><span class="sxs-lookup"><span data-stu-id="5274a-108">The **Unregister-AzureAutomationScheduledRunbook** cmdlet removes the association between a Microsoft Azure Automation runbook and a schedule, which stops the runbook from starting when the schedule fires.</span></span>

## <span data-ttu-id="5274a-109">示例</span><span class="sxs-lookup"><span data-stu-id="5274a-109">EXAMPLES</span></span>

### <span data-ttu-id="5274a-110">範例1：移除 [runbook] 與 [排程] 之間的關聯</span><span class="sxs-lookup"><span data-stu-id="5274a-110">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\> Unregister-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="5274a-111">這個命令會移除名為 Runbk01 的 runbook 與名為 Runbk01Sched 的排程之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="5274a-111">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="5274a-112">參數</span><span class="sxs-lookup"><span data-stu-id="5274a-112">PARAMETERS</span></span>

### <span data-ttu-id="5274a-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5274a-113">-AutomationAccountName</span></span>
<span data-ttu-id="5274a-114">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="5274a-114">Specifies the name of an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5274a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5274a-115">-Force</span></span>
<span data-ttu-id="5274a-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="5274a-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5274a-117">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="5274a-117">-JobScheduleId</span></span>
<span data-ttu-id="5274a-118">指定排程的 runbook ID。</span><span class="sxs-lookup"><span data-stu-id="5274a-118">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5274a-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="5274a-119">-Profile</span></span>
<span data-ttu-id="5274a-120">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5274a-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5274a-121">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="5274a-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5274a-122">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="5274a-122">-RunbookName</span></span>
<span data-ttu-id="5274a-123">指定 runbook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="5274a-123">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5274a-124">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="5274a-124">-ScheduleName</span></span>
<span data-ttu-id="5274a-125">指定排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="5274a-125">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5274a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5274a-126">CommonParameters</span></span>
<span data-ttu-id="5274a-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5274a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5274a-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5274a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5274a-129">輸入</span><span class="sxs-lookup"><span data-stu-id="5274a-129">INPUTS</span></span>

## <span data-ttu-id="5274a-130">輸出</span><span class="sxs-lookup"><span data-stu-id="5274a-130">OUTPUTS</span></span>

## <span data-ttu-id="5274a-131">筆記</span><span class="sxs-lookup"><span data-stu-id="5274a-131">NOTES</span></span>

## <span data-ttu-id="5274a-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="5274a-132">RELATED LINKS</span></span>

[<span data-ttu-id="5274a-133">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="5274a-133">Register-AzureAutomationScheduledRunbook</span></span>](./Register-AzureAutomationScheduledRunbook.md)


