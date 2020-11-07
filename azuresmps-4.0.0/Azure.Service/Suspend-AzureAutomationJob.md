---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: CE04DEE6-28AE-43A3-A8DE-98AC0A57E575
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1c2d9a3aa53cb8efd2924f24aa80db2c7fd07fea
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967205"
---
# <span data-ttu-id="08214-101">Suspend-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="08214-101">Suspend-AzureAutomationJob</span></span>

## <span data-ttu-id="08214-102">摘要</span><span class="sxs-lookup"><span data-stu-id="08214-102">SYNOPSIS</span></span>

<span data-ttu-id="08214-103">暫停自動化作業。</span><span class="sxs-lookup"><span data-stu-id="08214-103">Suspends an Automation job.</span></span>

## <span data-ttu-id="08214-104">句法</span><span class="sxs-lookup"><span data-stu-id="08214-104">SYNTAX</span></span>

```
Suspend-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="08214-105">說明</span><span class="sxs-lookup"><span data-stu-id="08214-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="08214-106">**AzureAutomationJob** Cmdlet 會暫停 Microsoft Azure 自動化作業。</span><span class="sxs-lookup"><span data-stu-id="08214-106">The **Suspend-AzureAutomationJob** cmdlet suspends a Microsoft Azure Automation job.</span></span>
<span data-ttu-id="08214-107">指定執行自動化作業。</span><span class="sxs-lookup"><span data-stu-id="08214-107">Specify a running Automation job.</span></span>

<span data-ttu-id="08214-108">若要繼續暫停的作業，請使用 **Resume AzureAutomationJob** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="08214-108">To resume a suspended job, use the **Resume-AzureAutomationJob** cmdlet.</span></span>

## <span data-ttu-id="08214-109">示例</span><span class="sxs-lookup"><span data-stu-id="08214-109">EXAMPLES</span></span>

### <span data-ttu-id="08214-110">範例1：暫停作業</span><span class="sxs-lookup"><span data-stu-id="08214-110">Example 1: Suspend a job</span></span>
```
PS C:\> Suspend-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="08214-111">這個命令會暫停具有指定識別碼的作業。</span><span class="sxs-lookup"><span data-stu-id="08214-111">This command suspends the job that has the specified ID.</span></span>

## <span data-ttu-id="08214-112">參數</span><span class="sxs-lookup"><span data-stu-id="08214-112">PARAMETERS</span></span>

### <span data-ttu-id="08214-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="08214-113">-AutomationAccountName</span></span>
<span data-ttu-id="08214-114">指定自動化帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="08214-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="08214-115">-識別碼</span><span class="sxs-lookup"><span data-stu-id="08214-115">-Id</span></span>
<span data-ttu-id="08214-116">指定作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="08214-116">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="08214-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="08214-117">-Profile</span></span>
<span data-ttu-id="08214-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="08214-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="08214-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="08214-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="08214-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08214-120">CommonParameters</span></span>
<span data-ttu-id="08214-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="08214-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08214-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="08214-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08214-123">輸入</span><span class="sxs-lookup"><span data-stu-id="08214-123">INPUTS</span></span>

## <span data-ttu-id="08214-124">輸出</span><span class="sxs-lookup"><span data-stu-id="08214-124">OUTPUTS</span></span>

## <span data-ttu-id="08214-125">筆記</span><span class="sxs-lookup"><span data-stu-id="08214-125">NOTES</span></span>

## <span data-ttu-id="08214-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="08214-126">RELATED LINKS</span></span>

[<span data-ttu-id="08214-127">AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="08214-127">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="08214-128">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="08214-128">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="08214-129">停止 AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="08214-129">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)


