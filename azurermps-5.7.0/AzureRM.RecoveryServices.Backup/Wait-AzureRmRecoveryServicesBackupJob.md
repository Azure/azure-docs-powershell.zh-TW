---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/wait-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 651c1cd08f8a2c711a4a0cec16ddb965ccfa8211
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446091"
---
# <span data-ttu-id="6a709-101">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="6a709-101">Wait-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="6a709-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6a709-102">SYNOPSIS</span></span>
<span data-ttu-id="6a709-103">等待備份作業完成。</span><span class="sxs-lookup"><span data-stu-id="6a709-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a709-104">句法</span><span class="sxs-lookup"><span data-stu-id="6a709-104">SYNTAX</span></span>

```
Wait-AzureRmRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a709-105">說明</span><span class="sxs-lookup"><span data-stu-id="6a709-105">DESCRIPTION</span></span>
<span data-ttu-id="6a709-106">**AzureRmRecoveryServicesBackupJob** Cmdlet 會等待 Azure 備份作業完成。</span><span class="sxs-lookup"><span data-stu-id="6a709-106">The **Wait-AzureRmRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="6a709-107">備份作業可能需要花很長的時間。</span><span class="sxs-lookup"><span data-stu-id="6a709-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="6a709-108">如果您執行的是腳本的一部份備份作業，您可能會想要強制腳本在作業完成後再繼續其他工作。</span><span class="sxs-lookup"><span data-stu-id="6a709-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>

<span data-ttu-id="6a709-109">包含此 Cmdlet 的腳本可能比輪詢備份服務的作業狀態更簡單。</span><span class="sxs-lookup"><span data-stu-id="6a709-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

<span data-ttu-id="6a709-110">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6a709-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="6a709-111">示例</span><span class="sxs-lookup"><span data-stu-id="6a709-111">EXAMPLES</span></span>

### <span data-ttu-id="6a709-112">範例1：等候作業完成</span><span class="sxs-lookup"><span data-stu-id="6a709-112">Example 1: Wait for a job to finish</span></span>
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

<span data-ttu-id="6a709-113">此腳本會輪詢目前正在進行中的第一個作業，直到該作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="6a709-113">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="6a709-114">參數</span><span class="sxs-lookup"><span data-stu-id="6a709-114">PARAMETERS</span></span>

### <span data-ttu-id="6a709-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a709-115">-DefaultProfile</span></span>
<span data-ttu-id="6a709-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6a709-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a709-117">-工作</span><span class="sxs-lookup"><span data-stu-id="6a709-117">-Job</span></span>
<span data-ttu-id="6a709-118">指定要等候的工作。</span><span class="sxs-lookup"><span data-stu-id="6a709-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="6a709-119">若要取得 **BackupJob** 物件，請使用 Get-AzureRmRecoveryServicesBackupJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6a709-119">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a709-120">-超時</span><span class="sxs-lookup"><span data-stu-id="6a709-120">-Timeout</span></span>
<span data-ttu-id="6a709-121">指定此 Cmdlet 等候作業完成所需的最長時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6a709-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="6a709-122">建議您指定一個超時值。</span><span class="sxs-lookup"><span data-stu-id="6a709-122">It is recommended to specify a time-out value.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a709-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a709-123">CommonParameters</span></span>
<span data-ttu-id="6a709-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6a709-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a709-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6a709-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a709-126">輸入</span><span class="sxs-lookup"><span data-stu-id="6a709-126">INPUTS</span></span>

### <span data-ttu-id="6a709-127">面向</span><span class="sxs-lookup"><span data-stu-id="6a709-127">Object</span></span>
<span data-ttu-id="6a709-128">參數「作業」接受來自管線的 "Object" 類型的值</span><span class="sxs-lookup"><span data-stu-id="6a709-128">Parameter 'Job' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="6a709-129">輸出</span><span class="sxs-lookup"><span data-stu-id="6a709-129">OUTPUTS</span></span>

### <span data-ttu-id="6a709-130">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="6a709-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

### <span data-ttu-id="6a709-131">[System.object]. RecoveryServices [JobBase] 的 [] （.]）</span><span class="sxs-lookup"><span data-stu-id="6a709-131">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="6a709-132">筆記</span><span class="sxs-lookup"><span data-stu-id="6a709-132">NOTES</span></span>

## <span data-ttu-id="6a709-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a709-133">RELATED LINKS</span></span>

[<span data-ttu-id="6a709-134">AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="6a709-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


