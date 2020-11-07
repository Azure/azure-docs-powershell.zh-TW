---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: E214AFEB-90A6-4553-94D4-FBEA6ADE572E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ee340c2302670628bb8a3893567d7f8a2da754f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967886"
---
# <span data-ttu-id="80ca1-101">Resume-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="80ca1-101">Resume-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="80ca1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80ca1-102">SYNOPSIS</span></span>
<span data-ttu-id="80ca1-103">繼續暫停的網站恢復作業。</span><span class="sxs-lookup"><span data-stu-id="80ca1-103">Resumes a suspended Site Recovery job.</span></span>

## <span data-ttu-id="80ca1-104">句法</span><span class="sxs-lookup"><span data-stu-id="80ca1-104">SYNTAX</span></span>

### <span data-ttu-id="80ca1-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="80ca1-105">ByObject (Default)</span></span>
```
Resume-AzureSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="80ca1-106">ById</span><span class="sxs-lookup"><span data-stu-id="80ca1-106">ById</span></span>
```
Resume-AzureSiteRecoveryJob -Id <String> [-Comments <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="80ca1-107">說明</span><span class="sxs-lookup"><span data-stu-id="80ca1-107">DESCRIPTION</span></span>
<span data-ttu-id="80ca1-108">**Resume AzureSiteRecoveryJob** Cmdlet 會繼續執行暫停的 Azure 網站還原作業。</span><span class="sxs-lookup"><span data-stu-id="80ca1-108">The **Resume-AzureSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="80ca1-109">示例</span><span class="sxs-lookup"><span data-stu-id="80ca1-109">EXAMPLES</span></span>

### <span data-ttu-id="80ca1-110">範例1：繼續所有作業</span><span class="sxs-lookup"><span data-stu-id="80ca1-110">Example 1: Resume all jobs</span></span>
```
PS C:\> $Jobs = Get-AzureSiteRecoveryJob  
PS C:\> Resume-AzureSiteRecoveryJob -Job $Jobs
ID               : d16397fb-cdf1-4972-b677-c333f3c557b4
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : Suspended
StateDescription : WaitingForManualAction
StartTime        : 10/6/2014 10:19:28 AM
EndTime          : 10/6/2014 10:19:31 AM
AllowedActions   : {Cancel, RestartTestFailoverCleanup}
Name             : Test failover
Tasks            : {Recovery plan preflight checks, Create test environment, All groups failover: Pre steps (1), 
                   Recovery plan failover...} 
Errors           : {}
```

<span data-ttu-id="80ca1-111">第一個命令會使用 **AzureSiteRecoveryJob** Cmdlet 來取得目前網站復原電子倉庫的所有 Azure Site recovery 作業，然後將結果儲存在 $Jobs 變數中。</span><span class="sxs-lookup"><span data-stu-id="80ca1-111">The first command gets all the Azure Site Recovery jobs for the current Site Recovery vault by using the **Get-AzureSiteRecoveryJob** cmdlet, and then stores the results in the $Jobs variable.</span></span>

<span data-ttu-id="80ca1-112">第二個命令會繼續 $Jobs 指定的工作。</span><span class="sxs-lookup"><span data-stu-id="80ca1-112">The second command resumes the job specified by $Jobs.</span></span>

## <span data-ttu-id="80ca1-113">參數</span><span class="sxs-lookup"><span data-stu-id="80ca1-113">PARAMETERS</span></span>

### <span data-ttu-id="80ca1-114">-批註</span><span class="sxs-lookup"><span data-stu-id="80ca1-114">-Comments</span></span>
<span data-ttu-id="80ca1-115">指定作業記錄的批註。</span><span class="sxs-lookup"><span data-stu-id="80ca1-115">Specifies the comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ca1-116">-識別碼</span><span class="sxs-lookup"><span data-stu-id="80ca1-116">-Id</span></span>
<span data-ttu-id="80ca1-117">指定要繼續作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="80ca1-117">Specifies the ID of a job to resume.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ca1-118">-工作</span><span class="sxs-lookup"><span data-stu-id="80ca1-118">-Job</span></span>
<span data-ttu-id="80ca1-119">指定要繼續執行的工作。</span><span class="sxs-lookup"><span data-stu-id="80ca1-119">Specifies the job to resume.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80ca1-120">-設定檔</span><span class="sxs-lookup"><span data-stu-id="80ca1-120">-Profile</span></span>
<span data-ttu-id="80ca1-121">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="80ca1-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="80ca1-122">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="80ca1-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="80ca1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80ca1-123">CommonParameters</span></span>
<span data-ttu-id="80ca1-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80ca1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80ca1-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="80ca1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80ca1-126">輸入</span><span class="sxs-lookup"><span data-stu-id="80ca1-126">INPUTS</span></span>

## <span data-ttu-id="80ca1-127">輸出</span><span class="sxs-lookup"><span data-stu-id="80ca1-127">OUTPUTS</span></span>

## <span data-ttu-id="80ca1-128">筆記</span><span class="sxs-lookup"><span data-stu-id="80ca1-128">NOTES</span></span>

## <span data-ttu-id="80ca1-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="80ca1-129">RELATED LINKS</span></span>

[<span data-ttu-id="80ca1-130">AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="80ca1-130">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="80ca1-131">重新開機-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="80ca1-131">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="80ca1-132">停止 AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="80ca1-132">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


