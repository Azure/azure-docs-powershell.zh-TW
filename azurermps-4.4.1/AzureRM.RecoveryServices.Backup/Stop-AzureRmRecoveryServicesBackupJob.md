---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 63d90aa5f98f6710702a70e9609c7625626e34c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455643"
---
# <span data-ttu-id="39c48-101">Stop-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="39c48-101">Stop-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="39c48-102">摘要</span><span class="sxs-lookup"><span data-stu-id="39c48-102">SYNOPSIS</span></span>
<span data-ttu-id="39c48-103">取消正在執行的工作。</span><span class="sxs-lookup"><span data-stu-id="39c48-103">Cancels a running job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39c48-104">句法</span><span class="sxs-lookup"><span data-stu-id="39c48-104">SYNTAX</span></span>

### <span data-ttu-id="39c48-105">JobFilterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="39c48-105">JobFilterSet (Default)</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="39c48-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="39c48-106">IdFilterSet</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39c48-107">說明</span><span class="sxs-lookup"><span data-stu-id="39c48-107">DESCRIPTION</span></span>
<span data-ttu-id="39c48-108">**AzureRmRecoveryServicesBackupJob** Cmdlet 會取消現有的 Azure 備份作業。</span><span class="sxs-lookup"><span data-stu-id="39c48-108">The **Stop-AzureRmRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="39c48-109">使用這個 Cmdlet 來停止耗時太長的工作，並封鎖其他活動。</span><span class="sxs-lookup"><span data-stu-id="39c48-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>

<span data-ttu-id="39c48-110">您只能取消備份及還原作業類型。</span><span class="sxs-lookup"><span data-stu-id="39c48-110">You can cancel only Backup and Restore job types.</span></span>

<span data-ttu-id="39c48-111">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="39c48-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="39c48-112">示例</span><span class="sxs-lookup"><span data-stu-id="39c48-112">EXAMPLES</span></span>

### <span data-ttu-id="39c48-113">範例1：停止備份作業</span><span class="sxs-lookup"><span data-stu-id="39c48-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzureRmRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzureRmRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="39c48-114">第一個命令會取得備份作業，然後將作業儲存在 $Job 變數中。</span><span class="sxs-lookup"><span data-stu-id="39c48-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>

<span data-ttu-id="39c48-115">最後一個命令會在 $Job 中指定備份作業的實例識別碼，以停止作業。</span><span class="sxs-lookup"><span data-stu-id="39c48-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="39c48-116">參數</span><span class="sxs-lookup"><span data-stu-id="39c48-116">PARAMETERS</span></span>

### <span data-ttu-id="39c48-117">-工作</span><span class="sxs-lookup"><span data-stu-id="39c48-117">-Job</span></span>
<span data-ttu-id="39c48-118">指定此 Cmdlet 取消的作業。</span><span class="sxs-lookup"><span data-stu-id="39c48-118">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="39c48-119">若要取得 **BackupJob** 物件，請使用 Get-AzureRmRecoveryServicesBackupJob Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="39c48-119">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="39c48-120">-作業 Id</span><span class="sxs-lookup"><span data-stu-id="39c48-120">-JobId</span></span>
<span data-ttu-id="39c48-121">指定要取消的作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="39c48-121">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="39c48-122">識別碼是 **BackupJob** 物件的 InstanceId 屬性。</span><span class="sxs-lookup"><span data-stu-id="39c48-122">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="39c48-123">若要取得 **BackupJob** 物件，請使用 AzureRmRecoveryServicesBackupJob。</span><span class="sxs-lookup"><span data-stu-id="39c48-123">To obtain an **BackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="39c48-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39c48-124">-DefaultProfile</span></span>
<span data-ttu-id="39c48-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="39c48-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39c48-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39c48-126">CommonParameters</span></span>
<span data-ttu-id="39c48-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="39c48-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39c48-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="39c48-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39c48-129">輸入</span><span class="sxs-lookup"><span data-stu-id="39c48-129">INPUTS</span></span>

## <span data-ttu-id="39c48-130">輸出</span><span class="sxs-lookup"><span data-stu-id="39c48-130">OUTPUTS</span></span>

### <span data-ttu-id="39c48-131">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="39c48-131">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="39c48-132">筆記</span><span class="sxs-lookup"><span data-stu-id="39c48-132">NOTES</span></span>

## <span data-ttu-id="39c48-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="39c48-133">RELATED LINKS</span></span>

[<span data-ttu-id="39c48-134">AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="39c48-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="39c48-135">稍候-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="39c48-135">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


