---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: f38029a85cac1b6771a546b120714823f5b02927
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621150"
---
# <span data-ttu-id="fb9ca-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="fb9ca-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="fb9ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fb9ca-102">SYNOPSIS</span></span>
<span data-ttu-id="fb9ca-103">取得備份作業的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fb9ca-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="fb9ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="fb9ca-104">SYNTAX</span></span>

### <span data-ttu-id="fb9ca-105">JobFilterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="fb9ca-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb9ca-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="fb9ca-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb9ca-107">說明</span><span class="sxs-lookup"><span data-stu-id="fb9ca-107">DESCRIPTION</span></span>
<span data-ttu-id="fb9ca-108">**AzRecoveryServicesBackupJobDetail** Cmdlet 會取得指定作業的 Azure 備份作業詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fb9ca-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="fb9ca-109">使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb9ca-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="fb9ca-110">示例</span><span class="sxs-lookup"><span data-stu-id="fb9ca-110">EXAMPLES</span></span>

### <span data-ttu-id="fb9ca-111">範例1：取得失敗作業的備份作業詳細資料</span><span class="sxs-lookup"><span data-stu-id="fb9ca-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="fb9ca-112">第一個命令會在 vault 中取得失敗作業的陣列，然後將它們儲存在 $Jobs 陣列中。</span><span class="sxs-lookup"><span data-stu-id="fb9ca-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="fb9ca-113">第二個命令會在 $Jobs 中取得失敗作業的作業詳細資料，然後將它們儲存在 $JobDetails 變數中。</span><span class="sxs-lookup"><span data-stu-id="fb9ca-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="fb9ca-114">最後一個命令會顯示失敗作業的錯誤詳細資料。</span><span class="sxs-lookup"><span data-stu-id="fb9ca-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="fb9ca-115">參數</span><span class="sxs-lookup"><span data-stu-id="fb9ca-115">PARAMETERS</span></span>

### <span data-ttu-id="fb9ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb9ca-116">-DefaultProfile</span></span>
<span data-ttu-id="fb9ca-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="fb9ca-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb9ca-118">-工作</span><span class="sxs-lookup"><span data-stu-id="fb9ca-118">-Job</span></span>
<span data-ttu-id="fb9ca-119">指定要取得的工作。</span><span class="sxs-lookup"><span data-stu-id="fb9ca-119">Specifies the job to get.</span></span>
<span data-ttu-id="fb9ca-120">若要取得 **BackupJob** 物件，請使用 Get-AzRecoveryServicesBackupJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fb9ca-120">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="fb9ca-121">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="fb9ca-121">-JobId</span></span>
<span data-ttu-id="fb9ca-122">指定備份作業的 ID。</span><span class="sxs-lookup"><span data-stu-id="fb9ca-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="fb9ca-123">識別碼是 **BackupJob** 物件的 InstanceId 屬性。</span><span class="sxs-lookup"><span data-stu-id="fb9ca-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

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

### <span data-ttu-id="fb9ca-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="fb9ca-124">-VaultId</span></span>
<span data-ttu-id="fb9ca-125">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="fb9ca-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="fb9ca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb9ca-126">CommonParameters</span></span>
<span data-ttu-id="fb9ca-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fb9ca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb9ca-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fb9ca-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb9ca-129">輸入</span><span class="sxs-lookup"><span data-stu-id="fb9ca-129">INPUTS</span></span>

### <span data-ttu-id="fb9ca-130">System.object</span><span class="sxs-lookup"><span data-stu-id="fb9ca-130">System.String</span></span>

## <span data-ttu-id="fb9ca-131">輸出</span><span class="sxs-lookup"><span data-stu-id="fb9ca-131">OUTPUTS</span></span>

### <span data-ttu-id="fb9ca-132">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="fb9ca-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="fb9ca-133">筆記</span><span class="sxs-lookup"><span data-stu-id="fb9ca-133">NOTES</span></span>

## <span data-ttu-id="fb9ca-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="fb9ca-134">RELATED LINKS</span></span>

[<span data-ttu-id="fb9ca-135">AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="fb9ca-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)


