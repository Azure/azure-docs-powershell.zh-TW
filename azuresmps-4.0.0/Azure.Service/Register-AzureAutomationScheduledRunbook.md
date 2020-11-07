---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 6D15837A-22A9-4C5A-8064-C3605088EA71
online version: ''
schema: 2.0.0
ms.openlocfilehash: d31a2ef49674054ca6bb257df67d3439f5abe074
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967319"
---
# <span data-ttu-id="3de79-101">Register-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="3de79-101">Register-AzureAutomationScheduledRunbook</span></span>

## <span data-ttu-id="3de79-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3de79-102">SYNOPSIS</span></span>

<span data-ttu-id="3de79-103">將 runbook 與排程建立關聯。</span><span class="sxs-lookup"><span data-stu-id="3de79-103">Associates a runbook with a schedule.</span></span>

## <span data-ttu-id="3de79-104">句法</span><span class="sxs-lookup"><span data-stu-id="3de79-104">SYNTAX</span></span>

### <span data-ttu-id="3de79-105">ByRunbookName (預設) </span><span class="sxs-lookup"><span data-stu-id="3de79-105">ByRunbookName (Default)</span></span>
```
Register-AzureAutomationScheduledRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="3de79-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="3de79-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzureAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3de79-107">說明</span><span class="sxs-lookup"><span data-stu-id="3de79-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="3de79-108">**Register AzureAutomationScheduledRunbook** Cmdlet 會將 runbook 與排程建立關聯。</span><span class="sxs-lookup"><span data-stu-id="3de79-108">The **Register-AzureAutomationScheduledRunbook** cmdlet associates a runbook with a schedule.</span></span>
<span data-ttu-id="3de79-109">Runbook 會根據您使用 *ScheduleName* 參數指定的排程開始。</span><span class="sxs-lookup"><span data-stu-id="3de79-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="3de79-110">示例</span><span class="sxs-lookup"><span data-stu-id="3de79-110">EXAMPLES</span></span>

### <span data-ttu-id="3de79-111">範例1：將 runbook 與排程建立關聯</span><span class="sxs-lookup"><span data-stu-id="3de79-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\> Register-AzureAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01"
```

<span data-ttu-id="3de79-112">這個命令會將名為 Runbk01 的 runbook 與 Azure 自動化帳戶（名為 Contoso17）中名為 Sched01 的排程相關聯。</span><span class="sxs-lookup"><span data-stu-id="3de79-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="3de79-113">參數</span><span class="sxs-lookup"><span data-stu-id="3de79-113">PARAMETERS</span></span>

### <span data-ttu-id="3de79-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3de79-114">-AutomationAccountName</span></span>
<span data-ttu-id="3de79-115">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="3de79-115">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="3de79-116">-參數</span><span class="sxs-lookup"><span data-stu-id="3de79-116">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3de79-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3de79-117">-Profile</span></span>
<span data-ttu-id="3de79-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3de79-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3de79-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="3de79-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3de79-120">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="3de79-120">-RunbookName</span></span>
<span data-ttu-id="3de79-121">指定 runbook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="3de79-121">Specifies the name of the runbook.</span></span>

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

### <span data-ttu-id="3de79-122">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="3de79-122">-ScheduleName</span></span>
<span data-ttu-id="3de79-123">指定排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="3de79-123">Specifies the name of the schedule.</span></span>

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

### <span data-ttu-id="3de79-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3de79-124">CommonParameters</span></span>
<span data-ttu-id="3de79-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3de79-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3de79-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3de79-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3de79-127">輸入</span><span class="sxs-lookup"><span data-stu-id="3de79-127">INPUTS</span></span>

## <span data-ttu-id="3de79-128">輸出</span><span class="sxs-lookup"><span data-stu-id="3de79-128">OUTPUTS</span></span>

### <span data-ttu-id="3de79-129">JobSchedule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="3de79-129">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="3de79-130">筆記</span><span class="sxs-lookup"><span data-stu-id="3de79-130">NOTES</span></span>

## <span data-ttu-id="3de79-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="3de79-131">RELATED LINKS</span></span>

[<span data-ttu-id="3de79-132">新-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="3de79-132">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="3de79-133">取消註冊-AzureAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="3de79-133">Unregister-AzureAutomationScheduledRunbook</span></span>](./Unregister-AzureAutomationScheduledRunbook.md)


