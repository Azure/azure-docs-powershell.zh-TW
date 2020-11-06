---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 10131025768b93fd1bbd692b07a22a03d8a88726
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621011"
---
# <span data-ttu-id="1ea86-101">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="1ea86-101">Wait-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="1ea86-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1ea86-102">SYNOPSIS</span></span>
<span data-ttu-id="1ea86-103">等待備份作業完成。</span><span class="sxs-lookup"><span data-stu-id="1ea86-103">Waits for a Backup job to finish.</span></span>

## <span data-ttu-id="1ea86-104">句法</span><span class="sxs-lookup"><span data-stu-id="1ea86-104">SYNTAX</span></span>

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ea86-105">說明</span><span class="sxs-lookup"><span data-stu-id="1ea86-105">DESCRIPTION</span></span>
<span data-ttu-id="1ea86-106">**AzRecoveryServicesBackupJob** Cmdlet 會等待 Azure 備份作業完成。</span><span class="sxs-lookup"><span data-stu-id="1ea86-106">The **Wait-AzRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="1ea86-107">備份作業可能需要花很長的時間。</span><span class="sxs-lookup"><span data-stu-id="1ea86-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="1ea86-108">如果您執行的是腳本的一部份備份作業，您可能會想要強制腳本在作業完成後再繼續其他工作。</span><span class="sxs-lookup"><span data-stu-id="1ea86-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="1ea86-109">包含此 Cmdlet 的腳本可能比輪詢備份服務的作業狀態更簡單。</span><span class="sxs-lookup"><span data-stu-id="1ea86-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="1ea86-110">使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ea86-110">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="1ea86-111">示例</span><span class="sxs-lookup"><span data-stu-id="1ea86-111">EXAMPLES</span></span>

### <span data-ttu-id="1ea86-112">範例1：等候作業完成</span><span class="sxs-lookup"><span data-stu-id="1ea86-112">Example 1: Wait for a job to finish</span></span>
```
PS C:\>
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress
    $Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $Job = Get-AzBackAzureRmRecoveryServicesBackupJob -Job $Job
    }
   Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="1ea86-113">此腳本會輪詢目前正在進行中的第一個作業，直到該作業完成為止。</span><span class="sxs-lookup"><span data-stu-id="1ea86-113">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="1ea86-114">參數</span><span class="sxs-lookup"><span data-stu-id="1ea86-114">PARAMETERS</span></span>

### <span data-ttu-id="1ea86-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ea86-115">-DefaultProfile</span></span>
<span data-ttu-id="1ea86-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1ea86-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ea86-117">-工作</span><span class="sxs-lookup"><span data-stu-id="1ea86-117">-Job</span></span>
<span data-ttu-id="1ea86-118">指定要等候的工作。</span><span class="sxs-lookup"><span data-stu-id="1ea86-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="1ea86-119">若要取得 **BackupJob** 物件，請使用 Get-AzRecoveryServicesBackupJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ea86-119">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="1ea86-120">-超時</span><span class="sxs-lookup"><span data-stu-id="1ea86-120">-Timeout</span></span>
<span data-ttu-id="1ea86-121">指定此 Cmdlet 等候作業完成所需的最長時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="1ea86-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="1ea86-122">建議您指定一個超時值。</span><span class="sxs-lookup"><span data-stu-id="1ea86-122">It is recommended to specify a time-out value.</span></span>

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

### <span data-ttu-id="1ea86-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="1ea86-123">-VaultId</span></span>
<span data-ttu-id="1ea86-124">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="1ea86-124">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ea86-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ea86-125">CommonParameters</span></span>
<span data-ttu-id="1ea86-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1ea86-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ea86-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1ea86-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ea86-128">輸入</span><span class="sxs-lookup"><span data-stu-id="1ea86-128">INPUTS</span></span>

### <span data-ttu-id="1ea86-129">System.object</span><span class="sxs-lookup"><span data-stu-id="1ea86-129">System.Object</span></span>

### <span data-ttu-id="1ea86-130">System.object</span><span class="sxs-lookup"><span data-stu-id="1ea86-130">System.String</span></span>

## <span data-ttu-id="1ea86-131">輸出</span><span class="sxs-lookup"><span data-stu-id="1ea86-131">OUTPUTS</span></span>

### <span data-ttu-id="1ea86-132">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="1ea86-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="1ea86-133">筆記</span><span class="sxs-lookup"><span data-stu-id="1ea86-133">NOTES</span></span>

## <span data-ttu-id="1ea86-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ea86-134">RELATED LINKS</span></span>

[<span data-ttu-id="1ea86-135">AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="1ea86-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)


