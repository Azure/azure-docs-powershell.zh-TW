---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 0B496085-670D-45F7-B989-D4541A3811FF
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37d95c570cc1c12bc40704ec2a2d89fcbec7cf48
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967380"
---
# <span data-ttu-id="9adfe-101">New-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9adfe-101">New-AzureAutomationRunbook</span></span>

## <span data-ttu-id="9adfe-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9adfe-102">SYNOPSIS</span></span>

<span data-ttu-id="9adfe-103">建立 runbook。</span><span class="sxs-lookup"><span data-stu-id="9adfe-103">Creates a runbook.</span></span>

## <span data-ttu-id="9adfe-104">句法</span><span class="sxs-lookup"><span data-stu-id="9adfe-104">SYNTAX</span></span>

### <span data-ttu-id="9adfe-105">ByRunbookName (預設) </span><span class="sxs-lookup"><span data-stu-id="9adfe-105">ByRunbookName (Default)</span></span>
```
New-AzureAutomationRunbook -Name <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9adfe-106">ByPath</span><span class="sxs-lookup"><span data-stu-id="9adfe-106">ByPath</span></span>
```
New-AzureAutomationRunbook -Path <String> [-Description <String>] [-Tags <String[]>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9adfe-107">說明</span><span class="sxs-lookup"><span data-stu-id="9adfe-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="9adfe-108">**新的-AzureAutomationRunbook** Cmdlet 會建立新的空白 Microsoft Azure 自動化 runbook。</span><span class="sxs-lookup"><span data-stu-id="9adfe-108">The **New-AzureAutomationRunbook** cmdlet creates a new, empty Microsoft Azure Automation runbook.</span></span>
<span data-ttu-id="9adfe-109">指定名稱以建立新的 runbook。</span><span class="sxs-lookup"><span data-stu-id="9adfe-109">Specify a name to create a new runbook.</span></span>

<span data-ttu-id="9adfe-110">您也可以指定 Windows PowerShell 腳本的路徑 (. ps1 ) 檔案匯入 runbook。</span><span class="sxs-lookup"><span data-stu-id="9adfe-110">You can also specify the path to a Windows PowerShell script (.ps1 ) file to import a runbook.</span></span>
<span data-ttu-id="9adfe-111">要匯入的腳本必須包含單一的 Windows PowerShell 工作流程定義。</span><span class="sxs-lookup"><span data-stu-id="9adfe-111">The script to import must contain a single Windows PowerShell Workflow definition.</span></span>
<span data-ttu-id="9adfe-112">這個 Windows PowerShell 工作流程的名稱會變成 runbook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="9adfe-112">The name of this Windows PowerShell Workflow becomes the name of the runbook.</span></span>

## <span data-ttu-id="9adfe-113">示例</span><span class="sxs-lookup"><span data-stu-id="9adfe-113">EXAMPLES</span></span>

### <span data-ttu-id="9adfe-114">範例1：建立 runbook</span><span class="sxs-lookup"><span data-stu-id="9adfe-114">Example 1: Create a runbook</span></span>
```
PS C:\> New-AzureAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02"
```

<span data-ttu-id="9adfe-115">這個命令會在名為 [Contoso17] 的自動化帳戶中，建立名為 Runbook02 的新 runbook。</span><span class="sxs-lookup"><span data-stu-id="9adfe-115">This command creates a new runbook named Runbook02 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="9adfe-116">參數</span><span class="sxs-lookup"><span data-stu-id="9adfe-116">PARAMETERS</span></span>

### <span data-ttu-id="9adfe-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9adfe-117">-AutomationAccountName</span></span>
<span data-ttu-id="9adfe-118">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="9adfe-118">Specifies the name of the Automation account.</span></span>

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

### <span data-ttu-id="9adfe-119">-描述</span><span class="sxs-lookup"><span data-stu-id="9adfe-119">-Description</span></span>
<span data-ttu-id="9adfe-120">指定 runbook 的描述。</span><span class="sxs-lookup"><span data-stu-id="9adfe-120">Specifies a description for the runbook.</span></span>

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

### <span data-ttu-id="9adfe-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="9adfe-121">-Name</span></span>
<span data-ttu-id="9adfe-122">指定 runbook 的名稱。</span><span class="sxs-lookup"><span data-stu-id="9adfe-122">Specifies the name for the runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9adfe-123">-Path</span><span class="sxs-lookup"><span data-stu-id="9adfe-123">-Path</span></span>
<span data-ttu-id="9adfe-124">指定路徑。</span><span class="sxs-lookup"><span data-stu-id="9adfe-124">Specifies the path.</span></span>

```yaml
Type: String
Parameter Sets: ByPath
Aliases: RunbookPath

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9adfe-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="9adfe-125">-Profile</span></span>
<span data-ttu-id="9adfe-126">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="9adfe-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9adfe-127">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="9adfe-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9adfe-128">-標記</span><span class="sxs-lookup"><span data-stu-id="9adfe-128">-Tags</span></span>
<span data-ttu-id="9adfe-129">指定 runbook 的標記。</span><span class="sxs-lookup"><span data-stu-id="9adfe-129">Specifies tags for the runbook.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9adfe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9adfe-130">CommonParameters</span></span>
<span data-ttu-id="9adfe-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9adfe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9adfe-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9adfe-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9adfe-133">輸入</span><span class="sxs-lookup"><span data-stu-id="9adfe-133">INPUTS</span></span>

## <span data-ttu-id="9adfe-134">輸出</span><span class="sxs-lookup"><span data-stu-id="9adfe-134">OUTPUTS</span></span>

### <span data-ttu-id="9adfe-135">[-Azure. 命令介面]。</span><span class="sxs-lookup"><span data-stu-id="9adfe-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="9adfe-136">筆記</span><span class="sxs-lookup"><span data-stu-id="9adfe-136">NOTES</span></span>

## <span data-ttu-id="9adfe-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="9adfe-137">RELATED LINKS</span></span>

[<span data-ttu-id="9adfe-138">AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9adfe-138">Get-AzureAutomationRunbook</span></span>](./Get-AzureAutomationRunbook.md)

[<span data-ttu-id="9adfe-139">發佈-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9adfe-139">Publish-AzureAutomationRunbook</span></span>](./Publish-AzureAutomationRunbook.md)

[<span data-ttu-id="9adfe-140">移除-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9adfe-140">Remove-AzureAutomationRunbook</span></span>](./Remove-AzureAutomationRunbook.md)

[<span data-ttu-id="9adfe-141">Set-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9adfe-141">Set-AzureAutomationRunbook</span></span>](./Set-AzureAutomationRunbook.md)

[<span data-ttu-id="9adfe-142">開始-AzureAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="9adfe-142">Start-AzureAutomationRunbook</span></span>](./Start-AzureAutomationRunbook.md)


