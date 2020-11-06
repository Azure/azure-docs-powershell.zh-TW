---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 133a779a1227c74830fdae69b52db321a63a12e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446135"
---
# <span data-ttu-id="3b3ea-101">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="3b3ea-101">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>

## <span data-ttu-id="3b3ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3b3ea-102">SYNOPSIS</span></span>
<span data-ttu-id="3b3ea-103">取得備份作業的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3b3ea-103">Gets details for a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b3ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="3b3ea-104">SYNTAX</span></span>

### <span data-ttu-id="3b3ea-105">JobFilterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3b3ea-105">JobFilterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3b3ea-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="3b3ea-106">IdFilterSet</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3b3ea-107">說明</span><span class="sxs-lookup"><span data-stu-id="3b3ea-107">DESCRIPTION</span></span>
<span data-ttu-id="3b3ea-108">**AzureRmRecoveryServicesBackupJobDetails** Cmdlet 會取得指定作業的 Azure 備份作業詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3b3ea-108">The **Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet gets Azure Backup job details for a specified job.</span></span>

<span data-ttu-id="3b3ea-109">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b3ea-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="3b3ea-110">示例</span><span class="sxs-lookup"><span data-stu-id="3b3ea-110">EXAMPLES</span></span>

### <span data-ttu-id="3b3ea-111">範例1：取得失敗作業的備份作業詳細資料</span><span class="sxs-lookup"><span data-stu-id="3b3ea-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="3b3ea-112">第一個命令會在 vault 中取得失敗作業的陣列，然後將它們儲存在 $Jobs 陣列中。</span><span class="sxs-lookup"><span data-stu-id="3b3ea-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>

<span data-ttu-id="3b3ea-113">第二個命令會在 $Jobs 中取得失敗作業的作業詳細資料，然後將它們儲存在 $JobDetails 變數中。</span><span class="sxs-lookup"><span data-stu-id="3b3ea-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>

<span data-ttu-id="3b3ea-114">最後一個命令會顯示失敗作業的錯誤詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3b3ea-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="3b3ea-115">參數</span><span class="sxs-lookup"><span data-stu-id="3b3ea-115">PARAMETERS</span></span>

### <span data-ttu-id="3b3ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b3ea-116">-DefaultProfile</span></span>
<span data-ttu-id="3b3ea-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3b3ea-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b3ea-118">-工作</span><span class="sxs-lookup"><span data-stu-id="3b3ea-118">-Job</span></span>
<span data-ttu-id="3b3ea-119">指定要取得的工作。</span><span class="sxs-lookup"><span data-stu-id="3b3ea-119">Specifies the job to get.</span></span>
<span data-ttu-id="3b3ea-120">若要取得 **BackupJob** 物件，請使用 Get-AzureRmRecoveryServicesBackupJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3b3ea-120">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: JobBase
Parameter Sets: JobFilterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3ea-121">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="3b3ea-121">-JobId</span></span>
<span data-ttu-id="3b3ea-122">指定備份作業的 ID。</span><span class="sxs-lookup"><span data-stu-id="3b3ea-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="3b3ea-123">識別碼是 **BackupJob** 物件的 InstanceId 屬性。</span><span class="sxs-lookup"><span data-stu-id="3b3ea-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

```yaml
Type: String
Parameter Sets: IdFilterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b3ea-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b3ea-124">CommonParameters</span></span>
<span data-ttu-id="3b3ea-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3b3ea-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b3ea-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3b3ea-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b3ea-127">輸入</span><span class="sxs-lookup"><span data-stu-id="3b3ea-127">INPUTS</span></span>

### <span data-ttu-id="3b3ea-128">所有</span><span class="sxs-lookup"><span data-stu-id="3b3ea-128">None</span></span>
<span data-ttu-id="3b3ea-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3b3ea-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3b3ea-130">輸出</span><span class="sxs-lookup"><span data-stu-id="3b3ea-130">OUTPUTS</span></span>

### <span data-ttu-id="3b3ea-131">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="3b3ea-131">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="3b3ea-132">筆記</span><span class="sxs-lookup"><span data-stu-id="3b3ea-132">NOTES</span></span>

## <span data-ttu-id="3b3ea-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="3b3ea-133">RELATED LINKS</span></span>

[<span data-ttu-id="3b3ea-134">AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="3b3ea-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


