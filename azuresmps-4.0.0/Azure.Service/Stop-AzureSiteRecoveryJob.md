---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8FF1362B-C7AB-4769-A88B-D1B6E214A006
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8275b8dfec4263c5ab7a8022dcb65edccb1171
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967853"
---
# <span data-ttu-id="298d4-101">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="298d4-101">Stop-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="298d4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="298d4-102">SYNOPSIS</span></span>
<span data-ttu-id="298d4-103">停止網站恢復作業。</span><span class="sxs-lookup"><span data-stu-id="298d4-103">Stops a Site Recovery job.</span></span>

## <span data-ttu-id="298d4-104">句法</span><span class="sxs-lookup"><span data-stu-id="298d4-104">SYNTAX</span></span>

### <span data-ttu-id="298d4-105">ByObject (預設) </span><span class="sxs-lookup"><span data-stu-id="298d4-105">ByObject (Default)</span></span>
```
Stop-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="298d4-106">ById</span><span class="sxs-lookup"><span data-stu-id="298d4-106">ById</span></span>
```
Stop-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="298d4-107">說明</span><span class="sxs-lookup"><span data-stu-id="298d4-107">DESCRIPTION</span></span>
<span data-ttu-id="298d4-108">**AzureSiteRecoveryJob** Cmdlet 會停止 Azure Site Recovery 作業。</span><span class="sxs-lookup"><span data-stu-id="298d4-108">The **Stop-AzureSiteRecoveryJob** cmdlet stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="298d4-109">示例</span><span class="sxs-lookup"><span data-stu-id="298d4-109">EXAMPLES</span></span>

### <span data-ttu-id="298d4-110">範例1：停止所有作業</span><span class="sxs-lookup"><span data-stu-id="298d4-110">Example 1: Stop all jobs</span></span>
```
PS C:\>$Jobs = Get-AzureSiteRecoveryJob 
PS C:\> Stop-AzureSiteRecoveryJob -Job $Jobs
```

<span data-ttu-id="298d4-111">第一個命令會使用 **AzureSiteRecoveryJob** Cmdlet 來取得目前 Azure site recovery 保存庫的 Azure 網站恢復作業，然後將結果儲存在 $Jobs 變數中。</span><span class="sxs-lookup"><span data-stu-id="298d4-111">The first command gets the Azure Site Recovery jobs for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryJob** cmdlet, and then stores the results in the $Jobs variable.</span></span>

<span data-ttu-id="298d4-112">第二個命令會停止 $Jobs 指定的工作。</span><span class="sxs-lookup"><span data-stu-id="298d4-112">The second command stops the jobs specified by $Jobs.</span></span>

## <span data-ttu-id="298d4-113">參數</span><span class="sxs-lookup"><span data-stu-id="298d4-113">PARAMETERS</span></span>

### <span data-ttu-id="298d4-114">-識別碼</span><span class="sxs-lookup"><span data-stu-id="298d4-114">-Id</span></span>
<span data-ttu-id="298d4-115">指定要停止的工作 ID。</span><span class="sxs-lookup"><span data-stu-id="298d4-115">Specifies the ID of the job to stop.</span></span>

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

### <span data-ttu-id="298d4-116">-工作</span><span class="sxs-lookup"><span data-stu-id="298d4-116">-Job</span></span>
<span data-ttu-id="298d4-117">指定要停止的工作。</span><span class="sxs-lookup"><span data-stu-id="298d4-117">Specifies the job to stop.</span></span>

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

### <span data-ttu-id="298d4-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="298d4-118">-Profile</span></span>
<span data-ttu-id="298d4-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="298d4-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="298d4-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="298d4-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="298d4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="298d4-121">CommonParameters</span></span>
<span data-ttu-id="298d4-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="298d4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="298d4-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="298d4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="298d4-124">輸入</span><span class="sxs-lookup"><span data-stu-id="298d4-124">INPUTS</span></span>

## <span data-ttu-id="298d4-125">輸出</span><span class="sxs-lookup"><span data-stu-id="298d4-125">OUTPUTS</span></span>

## <span data-ttu-id="298d4-126">筆記</span><span class="sxs-lookup"><span data-stu-id="298d4-126">NOTES</span></span>

## <span data-ttu-id="298d4-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="298d4-127">RELATED LINKS</span></span>

[<span data-ttu-id="298d4-128">AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="298d4-128">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="298d4-129">重新開機-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="298d4-129">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="298d4-130">Resume-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="298d4-130">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)


