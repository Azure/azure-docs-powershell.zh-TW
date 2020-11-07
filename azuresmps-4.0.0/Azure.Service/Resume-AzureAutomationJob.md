---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 5E5B8102-9E7E-4128-8160-3AA3803B118F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ff0831e6458a9d587b508acfa2e09948d81d87e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966908"
---
# <span data-ttu-id="ec83f-101">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ec83f-101">Resume-AzureAutomationJob</span></span>

## <span data-ttu-id="ec83f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ec83f-102">SYNOPSIS</span></span>

<span data-ttu-id="ec83f-103">繼續已暫停的自動作業。</span><span class="sxs-lookup"><span data-stu-id="ec83f-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="ec83f-104">句法</span><span class="sxs-lookup"><span data-stu-id="ec83f-104">SYNTAX</span></span>

```
Resume-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ec83f-105">說明</span><span class="sxs-lookup"><span data-stu-id="ec83f-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="ec83f-106">**Resume AzureAutomationJob** Cmdlet 會繼續執行暫停的 Microsoft Azure 自動化作業。</span><span class="sxs-lookup"><span data-stu-id="ec83f-106">The **Resume-AzureAutomationJob** cmdlet resumes a suspended Microsoft Azure Automation job.</span></span>
<span data-ttu-id="ec83f-107">使用 *識別碼* 參數來指定暫停的作業。</span><span class="sxs-lookup"><span data-stu-id="ec83f-107">Use the *Id* parameter to specify the suspended job.</span></span>

<span data-ttu-id="ec83f-108">若要暫停作業，請使用 Suspend-AzureAutomationJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ec83f-108">To suspend a job, use the Suspend-AzureAutomationJob cmdlet.</span></span>

## <span data-ttu-id="ec83f-109">示例</span><span class="sxs-lookup"><span data-stu-id="ec83f-109">EXAMPLES</span></span>

### <span data-ttu-id="ec83f-110">範例1：繼續暫停的作業</span><span class="sxs-lookup"><span data-stu-id="ec83f-110">Example 1: Resume a suspended job</span></span>
```
PS C:\> Resume-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="ec83f-111">這個命令會繼續執行具有指定識別碼的作業。</span><span class="sxs-lookup"><span data-stu-id="ec83f-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="ec83f-112">參數</span><span class="sxs-lookup"><span data-stu-id="ec83f-112">PARAMETERS</span></span>

### <span data-ttu-id="ec83f-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ec83f-113">-AutomationAccountName</span></span>
<span data-ttu-id="ec83f-114">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec83f-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="ec83f-115">-識別碼</span><span class="sxs-lookup"><span data-stu-id="ec83f-115">-Id</span></span>
<span data-ttu-id="ec83f-116">指定作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ec83f-116">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="ec83f-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ec83f-117">-Profile</span></span>
<span data-ttu-id="ec83f-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ec83f-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ec83f-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ec83f-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ec83f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec83f-120">CommonParameters</span></span>
<span data-ttu-id="ec83f-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ec83f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec83f-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ec83f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec83f-123">輸入</span><span class="sxs-lookup"><span data-stu-id="ec83f-123">INPUTS</span></span>

## <span data-ttu-id="ec83f-124">輸出</span><span class="sxs-lookup"><span data-stu-id="ec83f-124">OUTPUTS</span></span>

## <span data-ttu-id="ec83f-125">筆記</span><span class="sxs-lookup"><span data-stu-id="ec83f-125">NOTES</span></span>

## <span data-ttu-id="ec83f-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="ec83f-126">RELATED LINKS</span></span>

[<span data-ttu-id="ec83f-127">AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ec83f-127">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="ec83f-128">停止 AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ec83f-128">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="ec83f-129">暫停-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="ec83f-129">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


