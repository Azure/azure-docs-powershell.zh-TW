---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: e0b3dc87ffdfc86f39f201b6384f38ce8ca1c70a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903958"
---
# <span data-ttu-id="4c300-101">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="4c300-101">Wait-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="4c300-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4c300-102">SYNOPSIS</span></span>

<span data-ttu-id="4c300-103">等待備份工作完成。</span><span class="sxs-lookup"><span data-stu-id="4c300-103">Waits for a Backup job to finish.</span></span>

## <span data-ttu-id="4c300-104">語法</span><span class="sxs-lookup"><span data-stu-id="4c300-104">SYNTAX</span></span>

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c300-105">描述</span><span class="sxs-lookup"><span data-stu-id="4c300-105">DESCRIPTION</span></span>

<span data-ttu-id="4c300-106">**Wait-AzRecoveryServicesBackupJob** Cmdlet 會等待 Azure 備份工作完成。</span><span class="sxs-lookup"><span data-stu-id="4c300-106">The **Wait-AzRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="4c300-107">備份工作可能需要很長的時間。</span><span class="sxs-lookup"><span data-stu-id="4c300-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="4c300-108">如果您在腳本中執行備份工作，您可能會想要強制腳本等待工作完成，再繼續執行其他工作。</span><span class="sxs-lookup"><span data-stu-id="4c300-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="4c300-109">包含此 Cmdlet 的腳本比輪詢備份服務的工作狀態更簡單。</span><span class="sxs-lookup"><span data-stu-id="4c300-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="4c300-110">使用 -VaultId 參數設定庫上下文。</span><span class="sxs-lookup"><span data-stu-id="4c300-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="4c300-111">例子</span><span class="sxs-lookup"><span data-stu-id="4c300-111">EXAMPLES</span></span>

### <span data-ttu-id="4c300-112">範例 1：等待工作完成</span><span class="sxs-lookup"><span data-stu-id="4c300-112">Example 1: Wait for a job to finish</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

<span data-ttu-id="4c300-113">此腳本會輪詢目前進行中的第一個工作，直到該工作完成或超過 1 小時的超時期限為止。</span><span class="sxs-lookup"><span data-stu-id="4c300-113">This script polls the first job that is currently in progress until the job has completed or timeout period of 1 hour expired.</span></span>

## <span data-ttu-id="4c300-114">參數</span><span class="sxs-lookup"><span data-stu-id="4c300-114">PARAMETERS</span></span>

### <span data-ttu-id="4c300-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c300-115">-DefaultProfile</span></span>

<span data-ttu-id="4c300-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4c300-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c300-117">-Job</span><span class="sxs-lookup"><span data-stu-id="4c300-117">-Job</span></span>

<span data-ttu-id="4c300-118">指定要等待的工作。</span><span class="sxs-lookup"><span data-stu-id="4c300-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="4c300-119">若要取得 **BackupJob 物件** ，請使用 **Get-AzRecoveryServicesBackupJob** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4c300-119">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="4c300-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="4c300-120">-Timeout</span></span>

<span data-ttu-id="4c300-121">指定此 Cmdlet 等待工作完成的最大時間 ，以碼錶示。</span><span class="sxs-lookup"><span data-stu-id="4c300-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="4c300-122">建議您指定一個超值。</span><span class="sxs-lookup"><span data-stu-id="4c300-122">It is recommended to specify a time-out value.</span></span>

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

### <span data-ttu-id="4c300-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4c300-123">-VaultId</span></span>

<span data-ttu-id="4c300-124">復原服務庫的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="4c300-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4c300-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c300-125">CommonParameters</span></span>
<span data-ttu-id="4c300-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4c300-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c300-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c300-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c300-128">輸入</span><span class="sxs-lookup"><span data-stu-id="4c300-128">INPUTS</span></span>

### <span data-ttu-id="4c300-129">System.Object</span><span class="sxs-lookup"><span data-stu-id="4c300-129">System.Object</span></span>

### <span data-ttu-id="4c300-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4c300-130">System.String</span></span>

## <span data-ttu-id="4c300-131">輸出</span><span class="sxs-lookup"><span data-stu-id="4c300-131">OUTPUTS</span></span>

### <span data-ttu-id="4c300-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.JobBase</span><span class="sxs-lookup"><span data-stu-id="4c300-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="4c300-133">筆記</span><span class="sxs-lookup"><span data-stu-id="4c300-133">NOTES</span></span>

## <span data-ttu-id="4c300-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c300-134">RELATED LINKS</span></span>

[<span data-ttu-id="4c300-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="4c300-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
