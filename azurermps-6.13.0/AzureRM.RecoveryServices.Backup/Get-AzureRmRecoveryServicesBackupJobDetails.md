---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 7d39ce49a76d8519f2eacf0649c52051290274f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445580"
---
# <span data-ttu-id="09126-101">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="09126-101">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>

## <span data-ttu-id="09126-102">摘要</span><span class="sxs-lookup"><span data-stu-id="09126-102">SYNOPSIS</span></span>
<span data-ttu-id="09126-103">取得備份作業的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="09126-103">Gets details for a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09126-104">句法</span><span class="sxs-lookup"><span data-stu-id="09126-104">SYNTAX</span></span>

### <span data-ttu-id="09126-105">JobFilterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="09126-105">JobFilterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09126-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="09126-106">IdFilterSet</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09126-107">說明</span><span class="sxs-lookup"><span data-stu-id="09126-107">DESCRIPTION</span></span>
<span data-ttu-id="09126-108">**AzureRmRecoveryServicesBackupJobDetails** Cmdlet 會取得指定作業的 Azure 備份作業詳細資料。</span><span class="sxs-lookup"><span data-stu-id="09126-108">The **Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="09126-109">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="09126-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="09126-110">示例</span><span class="sxs-lookup"><span data-stu-id="09126-110">EXAMPLES</span></span>

### <span data-ttu-id="09126-111">範例1：取得失敗作業的備份作業詳細資料</span><span class="sxs-lookup"><span data-stu-id="09126-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="09126-112">第一個命令會在 vault 中取得失敗作業的陣列，然後將它們儲存在 $Jobs 陣列中。</span><span class="sxs-lookup"><span data-stu-id="09126-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="09126-113">第二個命令會在 $Jobs 中取得失敗作業的作業詳細資料，然後將它們儲存在 $JobDetails 變數中。</span><span class="sxs-lookup"><span data-stu-id="09126-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="09126-114">最後一個命令會顯示失敗作業的錯誤詳細資料。</span><span class="sxs-lookup"><span data-stu-id="09126-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="09126-115">參數</span><span class="sxs-lookup"><span data-stu-id="09126-115">PARAMETERS</span></span>

### <span data-ttu-id="09126-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09126-116">-DefaultProfile</span></span>
<span data-ttu-id="09126-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="09126-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09126-118">-工作</span><span class="sxs-lookup"><span data-stu-id="09126-118">-Job</span></span>
<span data-ttu-id="09126-119">指定要取得的工作。</span><span class="sxs-lookup"><span data-stu-id="09126-119">Specifies the job to get.</span></span>
<span data-ttu-id="09126-120">若要取得 **BackupJob** 物件，請使用 Get-AzureRmRecoveryServicesBackupJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="09126-120">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="09126-121">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="09126-121">-JobId</span></span>
<span data-ttu-id="09126-122">指定備份作業的 ID。</span><span class="sxs-lookup"><span data-stu-id="09126-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="09126-123">識別碼是 **BackupJob** 物件的 InstanceId 屬性。</span><span class="sxs-lookup"><span data-stu-id="09126-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

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

### <span data-ttu-id="09126-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="09126-124">-VaultId</span></span>
<span data-ttu-id="09126-125">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="09126-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="09126-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09126-126">CommonParameters</span></span>
<span data-ttu-id="09126-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="09126-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09126-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="09126-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09126-129">輸入</span><span class="sxs-lookup"><span data-stu-id="09126-129">INPUTS</span></span>

### <span data-ttu-id="09126-130">System.object</span><span class="sxs-lookup"><span data-stu-id="09126-130">System.String</span></span>
<span data-ttu-id="09126-131">參數： VaultId (ByValue) </span><span class="sxs-lookup"><span data-stu-id="09126-131">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="09126-132">輸出</span><span class="sxs-lookup"><span data-stu-id="09126-132">OUTPUTS</span></span>

### <span data-ttu-id="09126-133">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="09126-133">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="09126-134">筆記</span><span class="sxs-lookup"><span data-stu-id="09126-134">NOTES</span></span>

## <span data-ttu-id="09126-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="09126-135">RELATED LINKS</span></span>

[<span data-ttu-id="09126-136">AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="09126-136">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


