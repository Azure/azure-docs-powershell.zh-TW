---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 97AC691F-3835-4CEE-B47E-430BE9962AF9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 26fcee5f6cb669ef49993a009aa76e9c9522b180
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967146"
---
# <span data-ttu-id="32d2e-101">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="32d2e-101">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>

## <span data-ttu-id="32d2e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="32d2e-103">開始提交或復原已遷移的卷容器。</span><span class="sxs-lookup"><span data-stu-id="32d2e-103">Initiates the commit or rollback of the volume containers that are migrated.</span></span>

## <span data-ttu-id="32d2e-104">句法</span><span class="sxs-lookup"><span data-stu-id="32d2e-104">SYNTAX</span></span>

### <span data-ttu-id="32d2e-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="32d2e-105">MigrateSpecificContainer</span></span>
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="32d2e-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="32d2e-106">MigrateAllContainer</span></span>
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="32d2e-107">說明</span><span class="sxs-lookup"><span data-stu-id="32d2e-107">DESCRIPTION</span></span>
<span data-ttu-id="32d2e-108">**Confirm AzureStorSimpleLegacyVolumeContainerStatus** Cmdlet 會啟動提交或復原作為舊版遷移的一部分而遷移的大量容器。</span><span class="sxs-lookup"><span data-stu-id="32d2e-108">The **Confirm-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet initiates the commit or rollback of the volume containers that are migrated as part of a legacy migration.</span></span>
<span data-ttu-id="32d2e-109">復原會將裝置還原為原始擁有權。</span><span class="sxs-lookup"><span data-stu-id="32d2e-109">The rollback restores the appliance to the original ownership.</span></span>
<span data-ttu-id="32d2e-110">Commit 會將擁有權指派給目標裝置。</span><span class="sxs-lookup"><span data-stu-id="32d2e-110">The commit assigns the ownership to the target appliance.</span></span>

## <span data-ttu-id="32d2e-111">示例</span><span class="sxs-lookup"><span data-stu-id="32d2e-111">EXAMPLES</span></span>

### <span data-ttu-id="32d2e-112">範例1：在特定的卷容器上啟動 commit 作業</span><span class="sxs-lookup"><span data-stu-id="32d2e-112">Example 1: Initiate a commit operation on a specific volume container</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Commit
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="32d2e-113">這個命令會針對指定的舊版配置 ID，在指定的卷容器上啟動 commit 作業。</span><span class="sxs-lookup"><span data-stu-id="32d2e-113">This command initiates a commit operation on the specified volume container for the specified legacy configuration ID.</span></span>
<span data-ttu-id="32d2e-114">若要查看操作的狀態，請使用 **AzureStorSimpleLegacyVolumeContainerStatus** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="32d2e-114">To see the status of the operation, use the **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet.</span></span>

### <span data-ttu-id="32d2e-115">範例2：在特定的卷容器上啟動復原操作</span><span class="sxs-lookup"><span data-stu-id="32d2e-115">Example 2: Initiate a rollback operation on a specific volume container</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Rollback
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="32d2e-116">這個命令會針對指定的舊版配置 ID，在指定的卷容器上啟動回滾作業。</span><span class="sxs-lookup"><span data-stu-id="32d2e-116">This command initiates a rollback operation on the specified volume container for the specified legacy configuration ID.</span></span>

### <span data-ttu-id="32d2e-117">範例3：在所有磁片容器上啟動 commit 作業</span><span class="sxs-lookup"><span data-stu-id="32d2e-117">Example 3: Initiate a commit operation on all volume containers</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Commit -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="32d2e-118">這個命令會針對指定的舊版設定識別碼，在所有卷容器上啟動 commit 作業。</span><span class="sxs-lookup"><span data-stu-id="32d2e-118">This command initiates a commit operation on all volume container for the specified legacy configuration ID.</span></span>

### <span data-ttu-id="32d2e-119">範例4：在所有磁片容器上啟動回滾作業</span><span class="sxs-lookup"><span data-stu-id="32d2e-119">Example 4: Initiate a rollback operation on all volume containers</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Rollback -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="32d2e-120">這個命令會針對指定的舊版配置 ID，在所有卷容器上啟動復原作業。</span><span class="sxs-lookup"><span data-stu-id="32d2e-120">This command initiates a rollback operation on all volume containers for the specified legacy configuration ID.</span></span>

## <span data-ttu-id="32d2e-121">參數</span><span class="sxs-lookup"><span data-stu-id="32d2e-121">PARAMETERS</span></span>

### <span data-ttu-id="32d2e-122">-全部</span><span class="sxs-lookup"><span data-stu-id="32d2e-122">-All</span></span>
<span data-ttu-id="32d2e-123">表示此 Cmdlet 會在匯入的設定檔案中的所有磁片容器上啟動回滾或確認作業。</span><span class="sxs-lookup"><span data-stu-id="32d2e-123">Indicates that this cmdlet initiates a roll back or commit operation on all volume containers in the imported configuration file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: MigrateAllContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d2e-124">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="32d2e-124">-LegacyConfigId</span></span>
<span data-ttu-id="32d2e-125">指定舊版裝置之設定的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="32d2e-125">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="32d2e-126">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="32d2e-126">-LegacyContainerNames</span></span>
<span data-ttu-id="32d2e-127">指定要套用遷移方案之卷容器名稱的陣列。</span><span class="sxs-lookup"><span data-stu-id="32d2e-127">Specifies an array of volume container names for which the migration plan applies.</span></span>

```yaml
Type: String[]
Parameter Sets: MigrateSpecificContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32d2e-128">-MigrationOperation</span><span class="sxs-lookup"><span data-stu-id="32d2e-128">-MigrationOperation</span></span>
<span data-ttu-id="32d2e-129">指定此 Cmdlet 是否執行 commit 或 rollback。</span><span class="sxs-lookup"><span data-stu-id="32d2e-129">Specifies whether this cmdlet performs a commit or rollback.</span></span>
<span data-ttu-id="32d2e-130">有效值為： Commit 與 Rollback。</span><span class="sxs-lookup"><span data-stu-id="32d2e-130">Valid values are: Commit and Rollback.</span></span>

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

### <span data-ttu-id="32d2e-131">-設定檔</span><span class="sxs-lookup"><span data-stu-id="32d2e-131">-Profile</span></span>
<span data-ttu-id="32d2e-132">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="32d2e-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="32d2e-133">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="32d2e-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="32d2e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32d2e-134">CommonParameters</span></span>
<span data-ttu-id="32d2e-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32d2e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32d2e-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="32d2e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32d2e-137">輸入</span><span class="sxs-lookup"><span data-stu-id="32d2e-137">INPUTS</span></span>

## <span data-ttu-id="32d2e-138">輸出</span><span class="sxs-lookup"><span data-stu-id="32d2e-138">OUTPUTS</span></span>

## <span data-ttu-id="32d2e-139">筆記</span><span class="sxs-lookup"><span data-stu-id="32d2e-139">NOTES</span></span>

## <span data-ttu-id="32d2e-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="32d2e-140">RELATED LINKS</span></span>

[<span data-ttu-id="32d2e-141">AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="32d2e-141">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="32d2e-142">AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="32d2e-142">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)

[<span data-ttu-id="32d2e-143">AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="32d2e-143">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


