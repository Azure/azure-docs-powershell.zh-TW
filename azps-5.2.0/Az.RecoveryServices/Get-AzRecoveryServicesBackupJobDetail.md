---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 7ebbb3cf53c422a3a4d5c73f156cd3890eaa41e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279041"
---
# <span data-ttu-id="0bef6-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="0bef6-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="0bef6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0bef6-102">SYNOPSIS</span></span>

<span data-ttu-id="0bef6-103">取得備份作業的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0bef6-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="0bef6-104">句法</span><span class="sxs-lookup"><span data-stu-id="0bef6-104">SYNTAX</span></span>

### <span data-ttu-id="0bef6-105">JobFilterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="0bef6-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bef6-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="0bef6-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bef6-107">說明</span><span class="sxs-lookup"><span data-stu-id="0bef6-107">DESCRIPTION</span></span>

<span data-ttu-id="0bef6-108">**AzRecoveryServicesBackupJobDetail** Cmdlet 會取得指定作業的 Azure 備份作業詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0bef6-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="0bef6-109">使用-VaultId 參數來設定 vault 內容。</span><span class="sxs-lookup"><span data-stu-id="0bef6-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="0bef6-110">警告： **我們** 會在未來的重大變更發行中移除 AzRecoveryServicesBackupJobDetails 別名。</span><span class="sxs-lookup"><span data-stu-id="0bef6-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="0bef6-111">示例</span><span class="sxs-lookup"><span data-stu-id="0bef6-111">EXAMPLES</span></span>

### <span data-ttu-id="0bef6-112">範例1：取得失敗作業的備份作業詳細資料</span><span class="sxs-lookup"><span data-stu-id="0bef6-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="0bef6-113">第一個命令會提取相關的電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="0bef6-113">The first command fetches the relevant vault.</span></span> <span data-ttu-id="0bef6-114">第二個命令會在 vault 中取得失敗作業的陣列，然後將它們儲存在 $Jobs 陣列中。</span><span class="sxs-lookup"><span data-stu-id="0bef6-114">The second command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="0bef6-115">第三個命令會在 $Jobs 中取得第一項失敗作業的工作詳細資料，然後將它們儲存在 $JobDetails 變數中。</span><span class="sxs-lookup"><span data-stu-id="0bef6-115">The third command gets the job details for the 1st failed job in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="0bef6-116">最後一個命令會顯示失敗作業的錯誤詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0bef6-116">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="0bef6-117">參數</span><span class="sxs-lookup"><span data-stu-id="0bef6-117">PARAMETERS</span></span>

### <span data-ttu-id="0bef6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bef6-118">-DefaultProfile</span></span>

<span data-ttu-id="0bef6-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0bef6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bef6-120">-工作</span><span class="sxs-lookup"><span data-stu-id="0bef6-120">-Job</span></span>

<span data-ttu-id="0bef6-121">指定要取得的工作。</span><span class="sxs-lookup"><span data-stu-id="0bef6-121">Specifies the job to get.</span></span>
<span data-ttu-id="0bef6-122">若要取得 **BackupJob** 物件，請使用 **AzRecoveryServicesBackupJob** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0bef6-122">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="0bef6-123">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="0bef6-123">-JobId</span></span>

<span data-ttu-id="0bef6-124">指定備份作業的 ID。</span><span class="sxs-lookup"><span data-stu-id="0bef6-124">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="0bef6-125">[識別碼] 是 **RecoveryServices JobBase** 物件的 [JobId] 屬性（property）。</span><span class="sxs-lookup"><span data-stu-id="0bef6-125">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="0bef6-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0bef6-126">-VaultId</span></span>

<span data-ttu-id="0bef6-127">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="0bef6-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0bef6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bef6-128">CommonParameters</span></span>
<span data-ttu-id="0bef6-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0bef6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bef6-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0bef6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bef6-131">輸入</span><span class="sxs-lookup"><span data-stu-id="0bef6-131">INPUTS</span></span>

### <span data-ttu-id="0bef6-132">System.object</span><span class="sxs-lookup"><span data-stu-id="0bef6-132">System.String</span></span>

## <span data-ttu-id="0bef6-133">輸出</span><span class="sxs-lookup"><span data-stu-id="0bef6-133">OUTPUTS</span></span>

### <span data-ttu-id="0bef6-134">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="0bef6-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="0bef6-135">筆記</span><span class="sxs-lookup"><span data-stu-id="0bef6-135">NOTES</span></span>

## <span data-ttu-id="0bef6-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="0bef6-136">RELATED LINKS</span></span>

[<span data-ttu-id="0bef6-137">AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="0bef6-137">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
