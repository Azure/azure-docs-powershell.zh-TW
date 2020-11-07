---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1C18EE5D-A916-4776-ABAE-A7B24FA74108
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf97dd5958eb2e1fdd9790355ac0236974c0db7f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967104"
---
# <span data-ttu-id="07d37-101">Get-AzureAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="07d37-101">Get-AzureAutomationJobOutput</span></span>

## <span data-ttu-id="07d37-102">摘要</span><span class="sxs-lookup"><span data-stu-id="07d37-102">SYNOPSIS</span></span>

<span data-ttu-id="07d37-103">取得 Azure 自動化作業的輸出。</span><span class="sxs-lookup"><span data-stu-id="07d37-103">Gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="07d37-104">句法</span><span class="sxs-lookup"><span data-stu-id="07d37-104">SYNTAX</span></span>

```
Get-AzureAutomationJobOutput -Id <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="07d37-105">說明</span><span class="sxs-lookup"><span data-stu-id="07d37-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="07d37-106">**AzureAutomationJobOutput** Cmdlet 會取得 Microsoft Azure 自動化作業的輸出。</span><span class="sxs-lookup"><span data-stu-id="07d37-106">The **Get-AzureAutomationJobOutput** cmdlet gets the output of a Microsoft Azure Automation job.</span></span>

## <span data-ttu-id="07d37-107">示例</span><span class="sxs-lookup"><span data-stu-id="07d37-107">EXAMPLES</span></span>

### <span data-ttu-id="07d37-108">範例1：取得 Azure 自動化作業的輸出</span><span class="sxs-lookup"><span data-stu-id="07d37-108">Example 1: Get the output of an Azure Automation job</span></span>
```
PS C:\> Get-AzureAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -Stream "Any"
```

<span data-ttu-id="07d37-109">這個命令會取得具有指定識別碼之作業的所有輸出。</span><span class="sxs-lookup"><span data-stu-id="07d37-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="07d37-110">參數</span><span class="sxs-lookup"><span data-stu-id="07d37-110">PARAMETERS</span></span>

### <span data-ttu-id="07d37-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="07d37-111">-AutomationAccountName</span></span>
<span data-ttu-id="07d37-112">指定 Azure 自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="07d37-112">Specifies the name of an Azure Automation account.</span></span>

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

### <span data-ttu-id="07d37-113">-識別碼</span><span class="sxs-lookup"><span data-stu-id="07d37-113">-Id</span></span>
<span data-ttu-id="07d37-114">指定作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="07d37-114">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07d37-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="07d37-115">-Profile</span></span>
<span data-ttu-id="07d37-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="07d37-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="07d37-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="07d37-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="07d37-118">-StartTime</span><span class="sxs-lookup"><span data-stu-id="07d37-118">-StartTime</span></span>
<span data-ttu-id="07d37-119">指定開始時間。</span><span class="sxs-lookup"><span data-stu-id="07d37-119">Specifies a start time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07d37-120">資料流程</span><span class="sxs-lookup"><span data-stu-id="07d37-120">-Stream</span></span>
<span data-ttu-id="07d37-121">指定輸出的類型。</span><span class="sxs-lookup"><span data-stu-id="07d37-121">Specifies the type of output.</span></span>
<span data-ttu-id="07d37-122">有效值為：</span><span class="sxs-lookup"><span data-stu-id="07d37-122">Valid values are:</span></span> 

- <span data-ttu-id="07d37-123">每</span><span class="sxs-lookup"><span data-stu-id="07d37-123">Any</span></span>
- <span data-ttu-id="07d37-124">Debug</span><span class="sxs-lookup"><span data-stu-id="07d37-124">Debug</span></span>
- <span data-ttu-id="07d37-125">出錯</span><span class="sxs-lookup"><span data-stu-id="07d37-125">Error</span></span>
- <span data-ttu-id="07d37-126">收</span><span class="sxs-lookup"><span data-stu-id="07d37-126">Output</span></span>
- <span data-ttu-id="07d37-127">處理</span><span class="sxs-lookup"><span data-stu-id="07d37-127">Progress</span></span>
- <span data-ttu-id="07d37-128">冗長</span><span class="sxs-lookup"><span data-stu-id="07d37-128">Verbose</span></span>
- <span data-ttu-id="07d37-129">警告</span><span class="sxs-lookup"><span data-stu-id="07d37-129">Warning</span></span>

```yaml
Type: StreamType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07d37-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d37-130">CommonParameters</span></span>
<span data-ttu-id="07d37-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="07d37-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d37-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="07d37-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d37-133">輸入</span><span class="sxs-lookup"><span data-stu-id="07d37-133">INPUTS</span></span>

## <span data-ttu-id="07d37-134">輸出</span><span class="sxs-lookup"><span data-stu-id="07d37-134">OUTPUTS</span></span>

## <span data-ttu-id="07d37-135">筆記</span><span class="sxs-lookup"><span data-stu-id="07d37-135">NOTES</span></span>

## <span data-ttu-id="07d37-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="07d37-136">RELATED LINKS</span></span>

[<span data-ttu-id="07d37-137">AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="07d37-137">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="07d37-138">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="07d37-138">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="07d37-139">停止 AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="07d37-139">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="07d37-140">暫停-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="07d37-140">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


