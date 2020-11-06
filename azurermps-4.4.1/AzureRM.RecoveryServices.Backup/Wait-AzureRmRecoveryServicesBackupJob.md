---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: c4678cfb29d366c5ad855ea86313ea36be35e10b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449551"
---
# <span data-ttu-id="f73d1-101">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f73d1-101">Wait-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="f73d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f73d1-102">SYNOPSIS</span></span>
<span data-ttu-id="f73d1-103">等待備份作業完成。</span><span class="sxs-lookup"><span data-stu-id="f73d1-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f73d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="f73d1-104">SYNTAX</span></span>

```
Wait-AzureRmRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f73d1-105">說明</span><span class="sxs-lookup"><span data-stu-id="f73d1-105">DESCRIPTION</span></span>
<span data-ttu-id="f73d1-106">**AzureRmRecoveryServicesBackupJob** Cmdlet 會等待 Azure 備份作業完成。</span><span class="sxs-lookup"><span data-stu-id="f73d1-106">The **Wait-AzureRmRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="f73d1-107">備份作業可能需要花很長的時間。</span><span class="sxs-lookup"><span data-stu-id="f73d1-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="f73d1-108">如果您執行的是腳本的一部份備份作業，您可能會想要強制腳本在作業完成後再繼續其他工作。</span><span class="sxs-lookup"><span data-stu-id="f73d1-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>

<span data-ttu-id="f73d1-109">包含此 Cmdlet 的腳本可能比輪詢備份服務的作業狀態更簡單。</span><span class="sxs-lookup"><span data-stu-id="f73d1-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

<span data-ttu-id="f73d1-110">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f73d1-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="f73d1-111">示例</span><span class="sxs-lookup"><span data-stu-id="f73d1-111">EXAMPLES</span></span>

### <span data-ttu-id="f73d1-112">範例1：等候作業完成</span><span class="sxs-lookup"><span data-stu-id="f73d1-112">Example 1: Wait for a job to finish</span></span>
```
PS C:\>
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
    $Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $Job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob -Job $Job
    }
   Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="f73d1-113">此腳本會輪詢目前正在進行中的第一個作業，直到該作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="f73d1-113">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="f73d1-114">參數</span><span class="sxs-lookup"><span data-stu-id="f73d1-114">PARAMETERS</span></span>

### <span data-ttu-id="f73d1-115">-工作</span><span class="sxs-lookup"><span data-stu-id="f73d1-115">-Job</span></span>
<span data-ttu-id="f73d1-116">指定要等候的工作。</span><span class="sxs-lookup"><span data-stu-id="f73d1-116">Specifies the job to wait for.</span></span>
<span data-ttu-id="f73d1-117">若要取得 **BackupJob** 物件，請使用 Get-AzureRmRecoveryServicesBackupJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f73d1-117">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f73d1-118">-超時</span><span class="sxs-lookup"><span data-stu-id="f73d1-118">-Timeout</span></span>
<span data-ttu-id="f73d1-119">指定此 Cmdlet 等候作業完成所需的最長時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="f73d1-119">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="f73d1-120">建議您指定一個超時值。</span><span class="sxs-lookup"><span data-stu-id="f73d1-120">It is recommended to specify a time-out value.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f73d1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f73d1-121">-DefaultProfile</span></span>
<span data-ttu-id="f73d1-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f73d1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f73d1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f73d1-123">CommonParameters</span></span>
<span data-ttu-id="f73d1-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f73d1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f73d1-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f73d1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f73d1-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f73d1-126">INPUTS</span></span>

### <span data-ttu-id="f73d1-127">面向</span><span class="sxs-lookup"><span data-stu-id="f73d1-127">Object</span></span>
<span data-ttu-id="f73d1-128">參數「作業」接受來自管線的 "Object" 類型的值</span><span class="sxs-lookup"><span data-stu-id="f73d1-128">Parameter 'Job' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="f73d1-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f73d1-129">OUTPUTS</span></span>

### <span data-ttu-id="f73d1-130">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="f73d1-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

### <span data-ttu-id="f73d1-131">[System.object]. RecoveryServices [JobBase] 的 [] （.]）</span><span class="sxs-lookup"><span data-stu-id="f73d1-131">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="f73d1-132">筆記</span><span class="sxs-lookup"><span data-stu-id="f73d1-132">NOTES</span></span>

## <span data-ttu-id="f73d1-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="f73d1-133">RELATED LINKS</span></span>

[<span data-ttu-id="f73d1-134">AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f73d1-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


