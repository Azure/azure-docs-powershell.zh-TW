---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/register-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: ec89359453af2dd997aed6359914ac499a6a3f7e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446555"
---
# <span data-ttu-id="068a0-101">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="068a0-101">Register-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="068a0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="068a0-102">SYNOPSIS</span></span>
<span data-ttu-id="068a0-103">將 runbook 與排程建立關聯。</span><span class="sxs-lookup"><span data-stu-id="068a0-103">Associates a runbook to a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="068a0-104">句法</span><span class="sxs-lookup"><span data-stu-id="068a0-104">SYNTAX</span></span>

### <span data-ttu-id="068a0-105">ByRunbookName (預設) </span><span class="sxs-lookup"><span data-stu-id="068a0-105">ByRunbookName (Default)</span></span>
```
Register-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="068a0-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="068a0-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="068a0-107">說明</span><span class="sxs-lookup"><span data-stu-id="068a0-107">DESCRIPTION</span></span>
<span data-ttu-id="068a0-108">**AzureRmAutomationScheduledRunbook** Cmdlet 會將 Azure 自動化 runbook 與排程相關聯。</span><span class="sxs-lookup"><span data-stu-id="068a0-108">The **Register-AzureRmAutomationScheduledRunbook** cmdlet associates an Azure Automation runbook to a schedule.</span></span>
<span data-ttu-id="068a0-109">Runbook 會根據您使用 *ScheduleName* 參數指定的排程開始。</span><span class="sxs-lookup"><span data-stu-id="068a0-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="068a0-110">示例</span><span class="sxs-lookup"><span data-stu-id="068a0-110">EXAMPLES</span></span>

### <span data-ttu-id="068a0-111">範例1：將 runbook 與排程建立關聯</span><span class="sxs-lookup"><span data-stu-id="068a0-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\>Register-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="068a0-112">這個命令會將名為 Runbk01 的 runbook 與 Azure 自動化帳戶（名為 Contoso17）中名為 Sched01 的排程相關聯。</span><span class="sxs-lookup"><span data-stu-id="068a0-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="068a0-113">參數</span><span class="sxs-lookup"><span data-stu-id="068a0-113">PARAMETERS</span></span>

### <span data-ttu-id="068a0-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="068a0-114">-AutomationAccountName</span></span>
<span data-ttu-id="068a0-115">指定此 Cmdlet 在其上執行的 runbook 自動化帳戶。</span><span class="sxs-lookup"><span data-stu-id="068a0-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="068a0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="068a0-116">-DefaultProfile</span></span>
<span data-ttu-id="068a0-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="068a0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068a0-118">-參數</span><span class="sxs-lookup"><span data-stu-id="068a0-118">-Parameters</span></span>
<span data-ttu-id="068a0-119">指定鍵/值對的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="068a0-119">Specifies a hash table of key/value pairs.</span></span>
<span data-ttu-id="068a0-120">金鑰是 runbook 參數名稱。</span><span class="sxs-lookup"><span data-stu-id="068a0-120">The keys are runbook parameter names.</span></span>
<span data-ttu-id="068a0-121">這些值是 runbook 參數值。</span><span class="sxs-lookup"><span data-stu-id="068a0-121">The values are runbook parameter values.</span></span>
<span data-ttu-id="068a0-122">當 runbook 啟動以回應相關聯的排程時，這些參數會傳遞至 runbook。</span><span class="sxs-lookup"><span data-stu-id="068a0-122">When the runbook starts in response to the associated schedule, these parameters are passed to the runbook.</span></span>

```yaml
Type: IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="068a0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="068a0-123">-ResourceGroupName</span></span>
<span data-ttu-id="068a0-124">指定排程的 runbook 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="068a0-124">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="068a0-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="068a0-125">-RunbookName</span></span>
<span data-ttu-id="068a0-126">指定此 Cmdlet 關聯至排程的 runbook 名稱。</span><span class="sxs-lookup"><span data-stu-id="068a0-126">Specifies the name of the runbook that this cmdlet associates to a schedule.</span></span>

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

### <span data-ttu-id="068a0-127">-RunOn</span><span class="sxs-lookup"><span data-stu-id="068a0-127">-RunOn</span></span>
<span data-ttu-id="068a0-128">混合式 runbook 輔助角色群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="068a0-128">The name of the hybrid runbook worker group.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="068a0-129">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="068a0-129">-ScheduleName</span></span>
<span data-ttu-id="068a0-130">指定此 Cmdlet 將 runbook 關聯到哪個排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="068a0-130">Specifies the name of the schedule to which this cmdlet associates a runbook.</span></span>

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

### <span data-ttu-id="068a0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="068a0-131">CommonParameters</span></span>
<span data-ttu-id="068a0-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="068a0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="068a0-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="068a0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="068a0-134">輸入</span><span class="sxs-lookup"><span data-stu-id="068a0-134">INPUTS</span></span>

### <span data-ttu-id="068a0-135">所有</span><span class="sxs-lookup"><span data-stu-id="068a0-135">None</span></span>
<span data-ttu-id="068a0-136">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="068a0-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="068a0-137">輸出</span><span class="sxs-lookup"><span data-stu-id="068a0-137">OUTPUTS</span></span>

### <span data-ttu-id="068a0-138">JobSchedule 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="068a0-138">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="068a0-139">筆記</span><span class="sxs-lookup"><span data-stu-id="068a0-139">NOTES</span></span>

## <span data-ttu-id="068a0-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="068a0-140">RELATED LINKS</span></span>

[<span data-ttu-id="068a0-141">AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="068a0-141">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="068a0-142">取消註冊-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="068a0-142">Unregister-AzureRmAutomationScheduledRunbook</span></span>](./Unregister-AzureRMAutomationScheduledRunbook.md)


