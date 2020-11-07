---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 436A6D6E-2280-475C-A1F5-6A6D72DAD9E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4895c9aa12ad56b8e3ddffb88a19439777d5b54a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967101"
---
# <span data-ttu-id="b7e2b-101">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="b7e2b-101">Get-AzureAutomationSchedule</span></span>

## <span data-ttu-id="b7e2b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b7e2b-102">SYNOPSIS</span></span>

<span data-ttu-id="b7e2b-103">取得 Azure 自動化排程。</span><span class="sxs-lookup"><span data-stu-id="b7e2b-103">Gets an Azure Automation schedule.</span></span>

## <span data-ttu-id="b7e2b-104">句法</span><span class="sxs-lookup"><span data-stu-id="b7e2b-104">SYNTAX</span></span>

### <span data-ttu-id="b7e2b-105">ByAll (預設) </span><span class="sxs-lookup"><span data-stu-id="b7e2b-105">ByAll (Default)</span></span>
```
Get-AzureAutomationSchedule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b7e2b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b7e2b-106">ByName</span></span>
```
Get-AzureAutomationSchedule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7e2b-107">說明</span><span class="sxs-lookup"><span data-stu-id="b7e2b-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="b7e2b-108">**AzureAutomationSchedule** Cmdlet 會取得 Microsoft Azure 自動化排程。</span><span class="sxs-lookup"><span data-stu-id="b7e2b-108">The **Get-AzureAutomationSchedule** cmdlet gets a Microsoft Azure Automation schedule.</span></span>

## <span data-ttu-id="b7e2b-109">示例</span><span class="sxs-lookup"><span data-stu-id="b7e2b-109">EXAMPLES</span></span>

### <span data-ttu-id="b7e2b-110">範例1：取得排程</span><span class="sxs-lookup"><span data-stu-id="b7e2b-110">Example 1: Get a schedule</span></span>
```
PS C:\> Get-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "DailySchedule08"
```

<span data-ttu-id="b7e2b-111">這個命令會取得名為 DailySchedule08 的排程。</span><span class="sxs-lookup"><span data-stu-id="b7e2b-111">This command gets the schedule named DailySchedule08.</span></span>

## <span data-ttu-id="b7e2b-112">參數</span><span class="sxs-lookup"><span data-stu-id="b7e2b-112">PARAMETERS</span></span>

### <span data-ttu-id="b7e2b-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b7e2b-113">-AutomationAccountName</span></span>
<span data-ttu-id="b7e2b-114">指定 Azure 自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7e2b-114">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="b7e2b-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="b7e2b-115">-Name</span></span>
<span data-ttu-id="b7e2b-116">指定排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7e2b-116">Specifies the name of a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ScheduleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7e2b-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b7e2b-117">-Profile</span></span>
<span data-ttu-id="b7e2b-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b7e2b-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b7e2b-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b7e2b-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b7e2b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7e2b-120">CommonParameters</span></span>
<span data-ttu-id="b7e2b-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b7e2b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7e2b-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b7e2b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7e2b-123">輸入</span><span class="sxs-lookup"><span data-stu-id="b7e2b-123">INPUTS</span></span>

## <span data-ttu-id="b7e2b-124">輸出</span><span class="sxs-lookup"><span data-stu-id="b7e2b-124">OUTPUTS</span></span>

### <span data-ttu-id="b7e2b-125">[-Azure. 命令. 自動化. 模型]。排程</span><span class="sxs-lookup"><span data-stu-id="b7e2b-125">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="b7e2b-126">筆記</span><span class="sxs-lookup"><span data-stu-id="b7e2b-126">NOTES</span></span>

## <span data-ttu-id="b7e2b-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7e2b-127">RELATED LINKS</span></span>

[<span data-ttu-id="b7e2b-128">新-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="b7e2b-128">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="b7e2b-129">移除-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="b7e2b-129">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)

[<span data-ttu-id="b7e2b-130">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="b7e2b-130">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


