---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 81c1aeded9b4bb40998448d61a5edbf35742bfcc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956829"
---
# <span data-ttu-id="eac59-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="eac59-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="eac59-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eac59-102">SYNOPSIS</span></span>

<span data-ttu-id="eac59-103">取得備份作業的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="eac59-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="eac59-104">句法</span><span class="sxs-lookup"><span data-stu-id="eac59-104">SYNTAX</span></span>

### <span data-ttu-id="eac59-105">JobFilterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="eac59-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eac59-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="eac59-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eac59-107">說明</span><span class="sxs-lookup"><span data-stu-id="eac59-107">DESCRIPTION</span></span>

<span data-ttu-id="eac59-108">**AzRecoveryServicesBackupJobDetail** Cmdlet 會取得指定作業的 Azure 備份作業詳細資料。</span><span class="sxs-lookup"><span data-stu-id="eac59-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="eac59-109">使用-VaultId 參數來設定 vault 內容。</span><span class="sxs-lookup"><span data-stu-id="eac59-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="eac59-110">警告： **我們** 會在未來的重大變更發行中移除 AzRecoveryServicesBackupJobDetails 別名。</span><span class="sxs-lookup"><span data-stu-id="eac59-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="eac59-111">示例</span><span class="sxs-lookup"><span data-stu-id="eac59-111">EXAMPLES</span></span>

### <span data-ttu-id="eac59-112">範例1：取得失敗作業的備份作業詳細資料</span><span class="sxs-lookup"><span data-stu-id="eac59-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="eac59-113">第一個命令會在 vault 中取得失敗作業的陣列，然後將它們儲存在 $Jobs 陣列中。</span><span class="sxs-lookup"><span data-stu-id="eac59-113">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="eac59-114">第二個命令會在 $Jobs 中取得失敗作業的作業詳細資料，然後將它們儲存在 $JobDetails 變數中。</span><span class="sxs-lookup"><span data-stu-id="eac59-114">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="eac59-115">最後一個命令會顯示失敗作業的錯誤詳細資料。</span><span class="sxs-lookup"><span data-stu-id="eac59-115">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="eac59-116">參數</span><span class="sxs-lookup"><span data-stu-id="eac59-116">PARAMETERS</span></span>

### <span data-ttu-id="eac59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eac59-117">-DefaultProfile</span></span>

<span data-ttu-id="eac59-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eac59-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eac59-119">-工作</span><span class="sxs-lookup"><span data-stu-id="eac59-119">-Job</span></span>

<span data-ttu-id="eac59-120">指定要取得的工作。</span><span class="sxs-lookup"><span data-stu-id="eac59-120">Specifies the job to get.</span></span>
<span data-ttu-id="eac59-121">若要取得 **BackupJob** 物件，請使用 **AzRecoveryServicesBackupJob** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eac59-121">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="eac59-122">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="eac59-122">-JobId</span></span>

<span data-ttu-id="eac59-123">指定備份作業的 ID。</span><span class="sxs-lookup"><span data-stu-id="eac59-123">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="eac59-124">[識別碼] 是 **RecoveryServices JobBase** 物件的 [JobId] 屬性（property）。</span><span class="sxs-lookup"><span data-stu-id="eac59-124">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="eac59-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="eac59-125">-VaultId</span></span>

<span data-ttu-id="eac59-126">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="eac59-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="eac59-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eac59-127">CommonParameters</span></span>
<span data-ttu-id="eac59-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eac59-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eac59-129">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="eac59-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eac59-130">輸入</span><span class="sxs-lookup"><span data-stu-id="eac59-130">INPUTS</span></span>

### <span data-ttu-id="eac59-131">System.object</span><span class="sxs-lookup"><span data-stu-id="eac59-131">System.String</span></span>

## <span data-ttu-id="eac59-132">輸出</span><span class="sxs-lookup"><span data-stu-id="eac59-132">OUTPUTS</span></span>

### <span data-ttu-id="eac59-133">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="eac59-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="eac59-134">筆記</span><span class="sxs-lookup"><span data-stu-id="eac59-134">NOTES</span></span>

## <span data-ttu-id="eac59-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="eac59-135">RELATED LINKS</span></span>

[<span data-ttu-id="eac59-136">AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="eac59-136">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
