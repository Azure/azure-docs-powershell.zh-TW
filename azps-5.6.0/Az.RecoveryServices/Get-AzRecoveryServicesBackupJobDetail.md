---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: c7b213fd041718de1f4f8a6c21979a6c0e7af964
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909978"
---
# <span data-ttu-id="6c671-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="6c671-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="6c671-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6c671-102">SYNOPSIS</span></span>

<span data-ttu-id="6c671-103">獲得備份工作的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="6c671-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="6c671-104">語法</span><span class="sxs-lookup"><span data-stu-id="6c671-104">SYNTAX</span></span>

### <span data-ttu-id="6c671-105">JobFilterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6c671-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-UseSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c671-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="6c671-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-UseSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c671-107">描述</span><span class="sxs-lookup"><span data-stu-id="6c671-107">DESCRIPTION</span></span>

<span data-ttu-id="6c671-108">**Get-AzRecoveryServicesBackupJobDetail** Cmdlet 會取得指定工作的 Azure 備份工作詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6c671-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="6c671-109">使用 -VaultId 參數設定庫上下文。</span><span class="sxs-lookup"><span data-stu-id="6c671-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="6c671-110">警告 **：Get-AzRecoveryServicesBackupJobDetails 別名** 將會在未來中斷的變更版本中移除。</span><span class="sxs-lookup"><span data-stu-id="6c671-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="6c671-111">例子</span><span class="sxs-lookup"><span data-stu-id="6c671-111">EXAMPLES</span></span>

### <span data-ttu-id="6c671-112">範例 1：取得失敗工作的備份工作詳細資料</span><span class="sxs-lookup"><span data-stu-id="6c671-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="6c671-113">第一個命令會抓取相關的儲存庫。</span><span class="sxs-lookup"><span data-stu-id="6c671-113">The first command fetches the relevant vault.</span></span> <span data-ttu-id="6c671-114">第二個命令會獲得保存庫中失敗工作的陣列，然後將這些工作儲存在$Jobs陣列中。</span><span class="sxs-lookup"><span data-stu-id="6c671-114">The second command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="6c671-115">第三個命令會獲得 $Jobs 中第一個失敗工作的工作詳細資料，然後將它們儲存在 $JobDetails 變數中。</span><span class="sxs-lookup"><span data-stu-id="6c671-115">The third command gets the job details for the 1st failed job in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="6c671-116">最後一個命令會顯示失敗工作的錯誤詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6c671-116">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="6c671-117">參數</span><span class="sxs-lookup"><span data-stu-id="6c671-117">PARAMETERS</span></span>

### <span data-ttu-id="6c671-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c671-118">-DefaultProfile</span></span>

<span data-ttu-id="6c671-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6c671-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c671-120">-Job</span><span class="sxs-lookup"><span data-stu-id="6c671-120">-Job</span></span>

<span data-ttu-id="6c671-121">指定要取得的工作。</span><span class="sxs-lookup"><span data-stu-id="6c671-121">Specifies the job to get.</span></span>
<span data-ttu-id="6c671-122">若要取得 **BackupJob 物件** ，請使用 **Get-AzRecoveryServicesBackupJob** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6c671-122">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c671-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="6c671-123">-JobId</span></span>

<span data-ttu-id="6c671-124">指定備份工作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6c671-124">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="6c671-125">識別碼是 **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.JobBase 物件的 JobId** 屬性。</span><span class="sxs-lookup"><span data-stu-id="6c671-125">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c671-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6c671-126">-VaultId</span></span>

<span data-ttu-id="6c671-127">復原服務庫的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="6c671-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6c671-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c671-128">CommonParameters</span></span>
<span data-ttu-id="6c671-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6c671-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c671-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c671-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c671-131">輸入</span><span class="sxs-lookup"><span data-stu-id="6c671-131">INPUTS</span></span>

### <span data-ttu-id="6c671-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6c671-132">System.String</span></span>

## <span data-ttu-id="6c671-133">輸出</span><span class="sxs-lookup"><span data-stu-id="6c671-133">OUTPUTS</span></span>

### <span data-ttu-id="6c671-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.JobBase</span><span class="sxs-lookup"><span data-stu-id="6c671-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="6c671-135">筆記</span><span class="sxs-lookup"><span data-stu-id="6c671-135">NOTES</span></span>

## <span data-ttu-id="6c671-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="6c671-136">RELATED LINKS</span></span>

[<span data-ttu-id="6c671-137">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="6c671-137">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
