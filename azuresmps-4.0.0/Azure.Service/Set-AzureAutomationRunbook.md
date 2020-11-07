---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C24CFC83-3151-452D-A7B9-E78466493474
online version: ''
schema: 2.0.0
ms.openlocfilehash: e193dba6f64553e5e52d7f900bdc5c54deac5112
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967518"
---
# <span data-ttu-id="4a88f-101">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a88f-101">Set-AzureAutomationRunbook</span></span>

## <span data-ttu-id="4a88f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4a88f-102">SYNOPSIS</span></span>

<span data-ttu-id="4a88f-103">修改 runbook 的設定。</span><span class="sxs-lookup"><span data-stu-id="4a88f-103">Modifies the configuration of a runbook.</span></span>

## <span data-ttu-id="4a88f-104">句法</span><span class="sxs-lookup"><span data-stu-id="4a88f-104">SYNTAX</span></span>

```
Set-AzureAutomationRunbook -Name <String> [-Description <String>] [-Tags <String[]>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4a88f-105">說明</span><span class="sxs-lookup"><span data-stu-id="4a88f-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="4a88f-106">AzureAutomationRunbook Cmdlet 會修改 Microsoft Azure 自動化 runbook 的 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="4a88f-106">The **Set-AzureAutomationRunbook** cmdlet modifies the configuration of a Microsoft Azure Automation runbook.</span></span>

## <span data-ttu-id="4a88f-107">示例</span><span class="sxs-lookup"><span data-stu-id="4a88f-107">EXAMPLES</span></span>

### <span data-ttu-id="4a88f-108">範例1：針對 runbook 啟用詳細記錄</span><span class="sxs-lookup"><span data-stu-id="4a88f-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\> Set-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "MyRunbook" -LogVerbose $True
```

<span data-ttu-id="4a88f-109">這個命令會針對在名為 Contoso17 的自動化帳戶中指定的 runbook 啟用詳細記錄。</span><span class="sxs-lookup"><span data-stu-id="4a88f-109">This command enables verbose logging for the jobs of the specified runbook in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="4a88f-110">參數</span><span class="sxs-lookup"><span data-stu-id="4a88f-110">PARAMETERS</span></span>

### <span data-ttu-id="4a88f-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4a88f-111">-AutomationAccountName</span></span>
<span data-ttu-id="4a88f-112">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="4a88f-112">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="4a88f-113">-描述</span><span class="sxs-lookup"><span data-stu-id="4a88f-113">-Description</span></span>
<span data-ttu-id="4a88f-114">指定 runbook 的描述。</span><span class="sxs-lookup"><span data-stu-id="4a88f-114">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="4a88f-115">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="4a88f-115">-LogProgress</span></span>
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

### <span data-ttu-id="4a88f-116">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="4a88f-116">-LogVerbose</span></span>
<span data-ttu-id="4a88f-117">指出是否要使用詳細記錄。</span><span class="sxs-lookup"><span data-stu-id="4a88f-117">Indicates whether to use verbose logging.</span></span>

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

### <span data-ttu-id="4a88f-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="4a88f-118">-Name</span></span>
<span data-ttu-id="4a88f-119">指定名稱。</span><span class="sxs-lookup"><span data-stu-id="4a88f-119">Specifies a name.</span></span>

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

### <span data-ttu-id="4a88f-120">-設定檔</span><span class="sxs-lookup"><span data-stu-id="4a88f-120">-Profile</span></span>
<span data-ttu-id="4a88f-121">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="4a88f-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4a88f-122">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="4a88f-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4a88f-123">-標記</span><span class="sxs-lookup"><span data-stu-id="4a88f-123">-Tags</span></span>
<span data-ttu-id="4a88f-124">指定標記的陣列。</span><span class="sxs-lookup"><span data-stu-id="4a88f-124">Specifies an array of tags.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a88f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a88f-125">CommonParameters</span></span>
<span data-ttu-id="4a88f-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4a88f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a88f-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4a88f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a88f-128">輸入</span><span class="sxs-lookup"><span data-stu-id="4a88f-128">INPUTS</span></span>

## <span data-ttu-id="4a88f-129">輸出</span><span class="sxs-lookup"><span data-stu-id="4a88f-129">OUTPUTS</span></span>

### <span data-ttu-id="4a88f-130">[-Azure. 命令介面]。</span><span class="sxs-lookup"><span data-stu-id="4a88f-130">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="4a88f-131">筆記</span><span class="sxs-lookup"><span data-stu-id="4a88f-131">NOTES</span></span>

## <span data-ttu-id="4a88f-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="4a88f-132">RELATED LINKS</span></span>

[<span data-ttu-id="4a88f-133">AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a88f-133">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="4a88f-134">新-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a88f-134">New-AzureAutomationRunbook</span></span>](./New-AzureAutomationRunbook.md)

[<span data-ttu-id="4a88f-135">發佈-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a88f-135">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="4a88f-136">移除-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a88f-136">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="4a88f-137">開始-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4a88f-137">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


