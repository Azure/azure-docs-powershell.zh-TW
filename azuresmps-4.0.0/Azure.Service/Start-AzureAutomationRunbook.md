---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B0AE1969-71FD-4B6E-B0C0-1B744814BD5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93dc73193c300f0f10fd9dccaff1c1f3954b8306
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967478"
---
# <span data-ttu-id="65c89-101">Start-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="65c89-101">Start-AzureAutomationRunbook</span></span>

## <span data-ttu-id="65c89-102">摘要</span><span class="sxs-lookup"><span data-stu-id="65c89-102">SYNOPSIS</span></span>

<span data-ttu-id="65c89-103">啟動 runbook 作業。</span><span class="sxs-lookup"><span data-stu-id="65c89-103">Starts a runbook job.</span></span>

## <span data-ttu-id="65c89-104">句法</span><span class="sxs-lookup"><span data-stu-id="65c89-104">SYNTAX</span></span>

```
Start-AzureAutomationRunbook -Name <String> [-Parameters <IDictionary>] [-RunOn <String>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="65c89-105">說明</span><span class="sxs-lookup"><span data-stu-id="65c89-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="65c89-106">**AzureAutomationRunbook** Cmdlet 會啟動 Microsoft Azure 自動化 runbook 作業。</span><span class="sxs-lookup"><span data-stu-id="65c89-106">The **Start-AzureAutomationRunbook** cmdlet starts a Microsoft Azure Automation runbook job.</span></span>
<span data-ttu-id="65c89-107">指定 runbook 的識別碼或名稱。</span><span class="sxs-lookup"><span data-stu-id="65c89-107">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="65c89-108">示例</span><span class="sxs-lookup"><span data-stu-id="65c89-108">EXAMPLES</span></span>

### <span data-ttu-id="65c89-109">範例1：啟動 runbook 作業</span><span class="sxs-lookup"><span data-stu-id="65c89-109">Example 1: Start a runbook job</span></span>
```
PS C:\> Start-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01"
```

<span data-ttu-id="65c89-110">這個命令會在名為 [Contoso17] 的自動化帳戶中，為名為「Runbk01」的 runbook 啟動 runbook 作業。</span><span class="sxs-lookup"><span data-stu-id="65c89-110">This command starts a runbook job for the runbook named Runbk01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="65c89-111">參數</span><span class="sxs-lookup"><span data-stu-id="65c89-111">PARAMETERS</span></span>

### <span data-ttu-id="65c89-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="65c89-112">-AutomationAccountName</span></span>
<span data-ttu-id="65c89-113">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="65c89-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="65c89-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="65c89-114">-Name</span></span>
<span data-ttu-id="65c89-115">指定 runbook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="65c89-115">Specifies the name of a runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c89-116">-參數</span><span class="sxs-lookup"><span data-stu-id="65c89-116">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c89-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="65c89-117">-Profile</span></span>
<span data-ttu-id="65c89-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="65c89-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="65c89-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="65c89-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="65c89-120">-RunOn</span><span class="sxs-lookup"><span data-stu-id="65c89-120">-RunOn</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c89-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65c89-121">CommonParameters</span></span>
<span data-ttu-id="65c89-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="65c89-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65c89-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="65c89-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65c89-124">輸入</span><span class="sxs-lookup"><span data-stu-id="65c89-124">INPUTS</span></span>

## <span data-ttu-id="65c89-125">輸出</span><span class="sxs-lookup"><span data-stu-id="65c89-125">OUTPUTS</span></span>

### <span data-ttu-id="65c89-126">[作為] 的 [自動化] 工作</span><span class="sxs-lookup"><span data-stu-id="65c89-126">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

## <span data-ttu-id="65c89-127">筆記</span><span class="sxs-lookup"><span data-stu-id="65c89-127">NOTES</span></span>

## <span data-ttu-id="65c89-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="65c89-128">RELATED LINKS</span></span>

[<span data-ttu-id="65c89-129">AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="65c89-129">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="65c89-130">新-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="65c89-130">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="65c89-131">發佈-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="65c89-131">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="65c89-132">移除-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="65c89-132">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="65c89-133">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="65c89-133">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)


