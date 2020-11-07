---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: E1141271-BA00-455C-AE80-DF5CD00348E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: c0dff4cb86ca46826a1fc7355a9f2c241d8de405
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967517"
---
# <span data-ttu-id="31907-101">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="31907-101">Set-AzureAutomationSchedule</span></span>

## <span data-ttu-id="31907-102">摘要</span><span class="sxs-lookup"><span data-stu-id="31907-102">SYNOPSIS</span></span>

<span data-ttu-id="31907-103">修改自動化排程。</span><span class="sxs-lookup"><span data-stu-id="31907-103">Modifies an Automation schedule.</span></span>

## <span data-ttu-id="31907-104">句法</span><span class="sxs-lookup"><span data-stu-id="31907-104">SYNTAX</span></span>

```
Set-AzureAutomationSchedule -Name <String> [-IsEnabled <Boolean>] [-Description <String>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="31907-105">說明</span><span class="sxs-lookup"><span data-stu-id="31907-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="31907-106">**AzureAutomationSchedule** Cmdlet 會在 Microsoft Azure 自動化中修改排程。</span><span class="sxs-lookup"><span data-stu-id="31907-106">The **Set-AzureAutomationSchedule** cmdlet modifies a schedule in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="31907-107">示例</span><span class="sxs-lookup"><span data-stu-id="31907-107">EXAMPLES</span></span>

### <span data-ttu-id="31907-108">範例1：修改排程</span><span class="sxs-lookup"><span data-stu-id="31907-108">Example 1: Modify a schedule</span></span>
```
PS C:\> Set-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -Description "Automation Schedule"
```

<span data-ttu-id="31907-109">這個命令會修改名為 Schedule01 的排程的描述。</span><span class="sxs-lookup"><span data-stu-id="31907-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="31907-110">參數</span><span class="sxs-lookup"><span data-stu-id="31907-110">PARAMETERS</span></span>

### <span data-ttu-id="31907-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="31907-111">-AutomationAccountName</span></span>
<span data-ttu-id="31907-112">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="31907-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="31907-113">-描述</span><span class="sxs-lookup"><span data-stu-id="31907-113">-Description</span></span>
<span data-ttu-id="31907-114">指定排程的描述。</span><span class="sxs-lookup"><span data-stu-id="31907-114">Specifies a description for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31907-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="31907-115">-IsEnabled</span></span>
<span data-ttu-id="31907-116">指出排程是否已啟用。</span><span class="sxs-lookup"><span data-stu-id="31907-116">Indicates whether the schedule is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31907-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="31907-117">-Name</span></span>
<span data-ttu-id="31907-118">指定排程的名稱。</span><span class="sxs-lookup"><span data-stu-id="31907-118">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="31907-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="31907-119">-Profile</span></span>
<span data-ttu-id="31907-120">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="31907-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="31907-121">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="31907-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="31907-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31907-122">CommonParameters</span></span>
<span data-ttu-id="31907-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="31907-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31907-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="31907-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31907-125">輸入</span><span class="sxs-lookup"><span data-stu-id="31907-125">INPUTS</span></span>

## <span data-ttu-id="31907-126">輸出</span><span class="sxs-lookup"><span data-stu-id="31907-126">OUTPUTS</span></span>

### <span data-ttu-id="31907-127">[-Azure. 命令. 自動化. 模型]。排程</span><span class="sxs-lookup"><span data-stu-id="31907-127">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="31907-128">筆記</span><span class="sxs-lookup"><span data-stu-id="31907-128">NOTES</span></span>

## <span data-ttu-id="31907-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="31907-129">RELATED LINKS</span></span>

[<span data-ttu-id="31907-130">AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="31907-130">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="31907-131">新-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="31907-131">New-AzureAutomationSchedule</span></span>](./New-AzureAutomationSchedule.md)

[<span data-ttu-id="31907-132">移除-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="31907-132">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)


