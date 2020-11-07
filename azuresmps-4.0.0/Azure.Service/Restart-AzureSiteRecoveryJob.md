---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AE26EA0F-9D92-4FDF-92EF-CA33BF06C0DB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68a97359e5181bbc27183c0c1dbb6f526fa2e529
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967522"
---
# <span data-ttu-id="ae544-101">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ae544-101">Restart-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="ae544-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae544-102">SYNOPSIS</span></span>
<span data-ttu-id="ae544-103">重新開機網站恢復作業。</span><span class="sxs-lookup"><span data-stu-id="ae544-103">Restarts a Site Recovery job.</span></span>

## <span data-ttu-id="ae544-104">句法</span><span class="sxs-lookup"><span data-stu-id="ae544-104">SYNTAX</span></span>

### <span data-ttu-id="ae544-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="ae544-105">ByObject (Default)</span></span>
```
Restart-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ae544-106">ById</span><span class="sxs-lookup"><span data-stu-id="ae544-106">ById</span></span>
```
Restart-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ae544-107">說明</span><span class="sxs-lookup"><span data-stu-id="ae544-107">DESCRIPTION</span></span>
<span data-ttu-id="ae544-108">**Restart AzureSiteRecoveryJob** Cmdlet 會重新開機 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="ae544-108">The **Restart-AzureSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="ae544-109">示例</span><span class="sxs-lookup"><span data-stu-id="ae544-109">EXAMPLES</span></span>

### <span data-ttu-id="ae544-110">範例1：重新開機作業</span><span class="sxs-lookup"><span data-stu-id="ae544-110">Example 1: Restart a job</span></span>
```
PS C:\> Restart-AzureSiteRecoveryJob -Id "bbf0b839-9aaa-49e1-8354-601c9145966d"
ID               : bbf0b839-9aaa-49e1-8354-601c9145966d
ClientRequestId  : ef42c8b0-640c-4442-960b-349f83d161a5-2014-24-06 14:24:04Z-P
State            : Failed
StateDescription : Failed
StartTime        : 10/6/2014 9:41:08 AM
EndTime          : 10/6/2014 9:41:21 AM
AllowedActions   : {Cancel, Restart}
Name             : Enable protection
Tasks            : {Prerequisites check for enabling protection , Identifying replication target, Enable replication, 
                   Starting initial replication...} 
Errors           : {CreateProtectionTargetTask}
```

<span data-ttu-id="ae544-111">這個命令會重新開機具有指定識別碼的作業。</span><span class="sxs-lookup"><span data-stu-id="ae544-111">This command restarts the job that has the specified ID.</span></span>

## <span data-ttu-id="ae544-112">參數</span><span class="sxs-lookup"><span data-stu-id="ae544-112">PARAMETERS</span></span>

### <span data-ttu-id="ae544-113">-識別碼</span><span class="sxs-lookup"><span data-stu-id="ae544-113">-Id</span></span>
<span data-ttu-id="ae544-114">指定要重新開機作業的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ae544-114">Specifies the ID of the job to restart.</span></span>

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

### <span data-ttu-id="ae544-115">-工作</span><span class="sxs-lookup"><span data-stu-id="ae544-115">-Job</span></span>
<span data-ttu-id="ae544-116">指定要重新開機的工作。</span><span class="sxs-lookup"><span data-stu-id="ae544-116">Specifies the job to restart.</span></span>

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

### <span data-ttu-id="ae544-117">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ae544-117">-Profile</span></span>
<span data-ttu-id="ae544-118">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ae544-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ae544-119">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ae544-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ae544-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae544-120">CommonParameters</span></span>
<span data-ttu-id="ae544-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae544-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae544-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ae544-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae544-123">輸入</span><span class="sxs-lookup"><span data-stu-id="ae544-123">INPUTS</span></span>

## <span data-ttu-id="ae544-124">輸出</span><span class="sxs-lookup"><span data-stu-id="ae544-124">OUTPUTS</span></span>

## <span data-ttu-id="ae544-125">筆記</span><span class="sxs-lookup"><span data-stu-id="ae544-125">NOTES</span></span>

## <span data-ttu-id="ae544-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae544-126">RELATED LINKS</span></span>

[<span data-ttu-id="ae544-127">AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ae544-127">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="ae544-128">Resume-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ae544-128">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="ae544-129">停止 AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="ae544-129">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


