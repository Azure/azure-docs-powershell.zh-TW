---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: d494169c989096ce562858c500289527479d42dd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98275116"
---
# <span data-ttu-id="53451-101">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="53451-101">Wait-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="53451-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53451-102">SYNOPSIS</span></span>

<span data-ttu-id="53451-103">等待備份作業完成。</span><span class="sxs-lookup"><span data-stu-id="53451-103">Waits for a Backup job to finish.</span></span>

## <span data-ttu-id="53451-104">句法</span><span class="sxs-lookup"><span data-stu-id="53451-104">SYNTAX</span></span>

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53451-105">說明</span><span class="sxs-lookup"><span data-stu-id="53451-105">DESCRIPTION</span></span>

<span data-ttu-id="53451-106">**AzRecoveryServicesBackupJob** Cmdlet 會等待 Azure 備份作業完成。</span><span class="sxs-lookup"><span data-stu-id="53451-106">The **Wait-AzRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="53451-107">備份作業可能需要花很長的時間。</span><span class="sxs-lookup"><span data-stu-id="53451-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="53451-108">如果您執行的是腳本的一部份備份作業，您可能會想要強制腳本在作業完成後再繼續其他工作。</span><span class="sxs-lookup"><span data-stu-id="53451-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="53451-109">包含此 Cmdlet 的腳本可能比輪詢備份服務的作業狀態更簡單。</span><span class="sxs-lookup"><span data-stu-id="53451-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="53451-110">使用-VaultId 參數來設定 vault 內容。</span><span class="sxs-lookup"><span data-stu-id="53451-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="53451-111">示例</span><span class="sxs-lookup"><span data-stu-id="53451-111">EXAMPLES</span></span>

### <span data-ttu-id="53451-112">範例1：等候作業完成</span><span class="sxs-lookup"><span data-stu-id="53451-112">Example 1: Wait for a job to finish</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

<span data-ttu-id="53451-113">此腳本會輪詢目前正在進行中的第一個作業，直到該作業已完成或超時期間超過1小時為止。</span><span class="sxs-lookup"><span data-stu-id="53451-113">This script polls the first job that is currently in progress until the job has completed or timeout period of 1 hour expired.</span></span>

## <span data-ttu-id="53451-114">參數</span><span class="sxs-lookup"><span data-stu-id="53451-114">PARAMETERS</span></span>

### <span data-ttu-id="53451-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53451-115">-DefaultProfile</span></span>

<span data-ttu-id="53451-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="53451-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53451-117">-工作</span><span class="sxs-lookup"><span data-stu-id="53451-117">-Job</span></span>

<span data-ttu-id="53451-118">指定要等候的工作。</span><span class="sxs-lookup"><span data-stu-id="53451-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="53451-119">若要取得 **BackupJob** 物件，請使用 **AzRecoveryServicesBackupJob** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="53451-119">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="53451-120">-超時</span><span class="sxs-lookup"><span data-stu-id="53451-120">-Timeout</span></span>

<span data-ttu-id="53451-121">指定此 Cmdlet 等候作業完成所需的最長時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="53451-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="53451-122">建議您指定一個超時值。</span><span class="sxs-lookup"><span data-stu-id="53451-122">It is recommended to specify a time-out value.</span></span>

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

### <span data-ttu-id="53451-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="53451-123">-VaultId</span></span>

<span data-ttu-id="53451-124">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="53451-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="53451-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53451-125">CommonParameters</span></span>
<span data-ttu-id="53451-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53451-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53451-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="53451-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53451-128">輸入</span><span class="sxs-lookup"><span data-stu-id="53451-128">INPUTS</span></span>

### <span data-ttu-id="53451-129">System.object</span><span class="sxs-lookup"><span data-stu-id="53451-129">System.Object</span></span>

### <span data-ttu-id="53451-130">System.object</span><span class="sxs-lookup"><span data-stu-id="53451-130">System.String</span></span>

## <span data-ttu-id="53451-131">輸出</span><span class="sxs-lookup"><span data-stu-id="53451-131">OUTPUTS</span></span>

### <span data-ttu-id="53451-132">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="53451-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="53451-133">筆記</span><span class="sxs-lookup"><span data-stu-id="53451-133">NOTES</span></span>

## <span data-ttu-id="53451-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="53451-134">RELATED LINKS</span></span>

[<span data-ttu-id="53451-135">AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="53451-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
