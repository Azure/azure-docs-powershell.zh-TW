---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A736738A-C6B3-4E5A-B9BA-D6559A27A667
online version: ''
schema: 2.0.0
ms.openlocfilehash: a95e604c6c3f6766ccfc89bd9018dbe2241fb5b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967996"
---
# <span data-ttu-id="a7416-101">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="a7416-101">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>

## <span data-ttu-id="a7416-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a7416-102">SYNOPSIS</span></span>
<span data-ttu-id="a7416-103">取得卷容器的遷移狀態。</span><span class="sxs-lookup"><span data-stu-id="a7416-103">Gets the migration status of the volume containers.</span></span>

## <span data-ttu-id="a7416-104">句法</span><span class="sxs-lookup"><span data-stu-id="a7416-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> [-LegacyContainerNames <String[]>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a7416-105">說明</span><span class="sxs-lookup"><span data-stu-id="a7416-105">DESCRIPTION</span></span>
<span data-ttu-id="a7416-106">**AzureStorSimpleLegacyVolumeContainerStatus** Cmdlet 會取得大量容器的遷移狀態。</span><span class="sxs-lookup"><span data-stu-id="a7416-106">The **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet gets the migration status of the volume containers.</span></span>
<span data-ttu-id="a7416-107">這個 Cmdlet 會傳回狀態資訊，包括是否仍在進行、完成或失敗的大量容器遷移。</span><span class="sxs-lookup"><span data-stu-id="a7416-107">This cmdlet returns status information which includes whether the volume container migration is still in progress, completed, or failed.</span></span>

## <span data-ttu-id="a7416-108">示例</span><span class="sxs-lookup"><span data-stu-id="a7416-108">EXAMPLES</span></span>

### <span data-ttu-id="a7416-109">範例1：取得失敗遷移的狀態</span><span class="sxs-lookup"><span data-stu-id="a7416-109">Example 1: Get status for a failed migration</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4" -LegacyContainerNames "OneSDKAzureCloud"
ConfigId             : dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4
MigrationCompleted   : No Cloud Configuration(s) are found to be in Completed state of Migration
MigrationInprogress  : No Cloud Configuration(s)  are found to be in InProgress state of Migration
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : Cloud Configuration Name: OneSDKAzureCloud
                       PercentageCompleted : 0
                       MigrationStatus : Failed
                       No Backup sets found
```

<span data-ttu-id="a7416-110">這個命令會取得已命名舊版容器的遷移狀態。</span><span class="sxs-lookup"><span data-stu-id="a7416-110">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="a7416-111">結果會顯示遷移失敗。</span><span class="sxs-lookup"><span data-stu-id="a7416-111">The results show that the migration failed.</span></span>

### <span data-ttu-id="a7416-112">範例2：取得進行中的遷移狀態</span><span class="sxs-lookup"><span data-stu-id="a7416-112">Example 2: Get status for a migration in progress</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4" -LegacyContainerNames "OneSDKAzureCloud"
ConfigId             : 5a83ec88-9e0a-4722-9fb0-9131caa7387a
MigrationCompleted   : No Cloud Configuration(s) are found to be in Completed state of Migration
MigrationInprogress  : CloudConfigurationName: OneSDKAzureCloud
                       PercentageCompleted : 10
                       MigrationStatus : InProgress
                       BackupSets : 
                           Policy : OneSDKBackupPolicy, Status : InProgress
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : No Cloud Configuration(s) are found to be in Failed state of Migration
```

<span data-ttu-id="a7416-113">這個命令會取得已命名舊版容器的遷移狀態。</span><span class="sxs-lookup"><span data-stu-id="a7416-113">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="a7416-114">結果會顯示遷移正在進行中。</span><span class="sxs-lookup"><span data-stu-id="a7416-114">The results show that the migration is in progress.</span></span>

### <span data-ttu-id="a7416-115">範例3：取得已完成的遷移的狀態</span><span class="sxs-lookup"><span data-stu-id="a7416-115">Example 3: Get status for a completed migration</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4 -LegacyContainerNames OneSDKAzureCloud
ConfigId             : 5a83ec88-9e0a-4722-9fb0-9131caa7387a
MigrationCompleted   : Cloud ConfigurationName: OneSDKAzureCloud
                       PercentageCompleted : 100
                       MigrationStatus : Completed
                       BackupSets : 
                          Policy : vg1p1, Created On : 04/06/2015 11:22:00, Status : Completed
                          Policy : vg1p1, Created On : 03/30/2015 11:22:00, Status : Completed
                          Policy : c1v1-Auto-Daily-CloudSnapshot, Created On : 03/30/2015 03:30:00, Status : Completed
MigrationInprogress  : No Cloud Configuration(s) are found to be in InProgress state of Migration
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : No Cloud Configuration(s) are found to be in Failed state of Migration
```

<span data-ttu-id="a7416-116">這個命令會取得已命名舊版容器的遷移狀態。</span><span class="sxs-lookup"><span data-stu-id="a7416-116">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="a7416-117">結果會顯示遷移已完成。</span><span class="sxs-lookup"><span data-stu-id="a7416-117">The results show that the migration is completed.</span></span>

## <span data-ttu-id="a7416-118">參數</span><span class="sxs-lookup"><span data-stu-id="a7416-118">PARAMETERS</span></span>

### <span data-ttu-id="a7416-119">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="a7416-119">-LegacyConfigId</span></span>
<span data-ttu-id="a7416-120">指定舊版裝置之設定的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="a7416-120">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7416-121">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="a7416-121">-LegacyContainerNames</span></span>
<span data-ttu-id="a7416-122">指定要套用遷移方案之卷容器名稱的陣列。</span><span class="sxs-lookup"><span data-stu-id="a7416-122">Specifies an array of volume container names for which the migration plan applies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7416-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a7416-123">-Profile</span></span>
<span data-ttu-id="a7416-124">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a7416-124">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7416-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7416-125">CommonParameters</span></span>
<span data-ttu-id="a7416-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a7416-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7416-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a7416-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7416-128">輸入</span><span class="sxs-lookup"><span data-stu-id="a7416-128">INPUTS</span></span>

## <span data-ttu-id="a7416-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a7416-129">OUTPUTS</span></span>

## <span data-ttu-id="a7416-130">筆記</span><span class="sxs-lookup"><span data-stu-id="a7416-130">NOTES</span></span>

## <span data-ttu-id="a7416-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7416-131">RELATED LINKS</span></span>

[<span data-ttu-id="a7416-132">確認-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="a7416-132">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Confirm-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="a7416-133">AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="a7416-133">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)


