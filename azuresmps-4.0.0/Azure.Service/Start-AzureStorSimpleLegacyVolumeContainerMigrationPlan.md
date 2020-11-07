---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 6F31F2B4-6131-4B11-B074-CA05CE3A56F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: f928ecba8f92badc1eb87e47aee16515f1684fce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967219"
---
# <span data-ttu-id="5ac8a-101">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="5ac8a-101">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>

## <span data-ttu-id="5ac8a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5ac8a-102">SYNOPSIS</span></span>
<span data-ttu-id="5ac8a-103">開始建立遷移方案。</span><span class="sxs-lookup"><span data-stu-id="5ac8a-103">Starts the creation of a migration plan.</span></span>

## <span data-ttu-id="5ac8a-104">句法</span><span class="sxs-lookup"><span data-stu-id="5ac8a-104">SYNTAX</span></span>

### <span data-ttu-id="5ac8a-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="5ac8a-105">MigrateSpecificContainer</span></span>
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5ac8a-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="5ac8a-106">MigrateAllContainer</span></span>
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5ac8a-107">說明</span><span class="sxs-lookup"><span data-stu-id="5ac8a-107">DESCRIPTION</span></span>
<span data-ttu-id="5ac8a-108">**開始 AzureStorSimpleLegacyVolumeContainerMigrationPlan** Cmdlet 會開始建立遷移方案。</span><span class="sxs-lookup"><span data-stu-id="5ac8a-108">The **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet starts the creation of a migration plan.</span></span>
<span data-ttu-id="5ac8a-109">遷移方案的建立是非同步。</span><span class="sxs-lookup"><span data-stu-id="5ac8a-109">The creation of a migration plan is asynchronous.</span></span>
<span data-ttu-id="5ac8a-110">若要查看遷移方案的狀態，請使用 **AzureStorSimpleLegacyVolumeContainerMigrationPlan** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5ac8a-110">To see the status of the migration plan, use the **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet.</span></span>

## <span data-ttu-id="5ac8a-111">示例</span><span class="sxs-lookup"><span data-stu-id="5ac8a-111">EXAMPLES</span></span>

### <span data-ttu-id="5ac8a-112">範例1：啟動遷移方案</span><span class="sxs-lookup"><span data-stu-id="5ac8a-112">Example 1: Start a migration plan</span></span>
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

<span data-ttu-id="5ac8a-113">這個命令會為舊版容器（名為 OneSDKAzureCloud）開始建立遷移方案。</span><span class="sxs-lookup"><span data-stu-id="5ac8a-113">This command starts creation of a migration plan for the legacy container named OneSDKAzureCloud.</span></span>
<span data-ttu-id="5ac8a-114">此命令會傳回有關計畫狀態的訊息，並使用 **AzureStorSimpleLegacyVolumeContainerMigrationPlan** Cmdlet 取得最新資訊。</span><span class="sxs-lookup"><span data-stu-id="5ac8a-114">The command returns a message about the status of the plan, and to use the **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet for up to date information.</span></span>

### <span data-ttu-id="5ac8a-115">範例2：針對所有的磁片容器啟動遷移方案</span><span class="sxs-lookup"><span data-stu-id="5ac8a-115">Example 2: Start migration plan for all volume containers</span></span>
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

<span data-ttu-id="5ac8a-116">這個命令會針對匯入的設定檔中的所有舊版卷容器，開始建立遷移方案。</span><span class="sxs-lookup"><span data-stu-id="5ac8a-116">This command starts creation of migration plan for all legacy volume containers in the configuration file that is imported.</span></span>

## <span data-ttu-id="5ac8a-117">參數</span><span class="sxs-lookup"><span data-stu-id="5ac8a-117">PARAMETERS</span></span>

### <span data-ttu-id="5ac8a-118">-全部</span><span class="sxs-lookup"><span data-stu-id="5ac8a-118">-All</span></span>
<span data-ttu-id="5ac8a-119">表示此 Cmdlet 會針對匯入的設定檔案中的所有大量容器開始進行遷移時間估計。</span><span class="sxs-lookup"><span data-stu-id="5ac8a-119">Indicates that this cmdlet starts migration time estimates for all volume containers in the imported configuration file.</span></span>

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

### <span data-ttu-id="5ac8a-120">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="5ac8a-120">-LegacyConfigId</span></span>
<span data-ttu-id="5ac8a-121">指定舊版裝置之設定的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="5ac8a-121">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="5ac8a-122">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="5ac8a-122">-LegacyContainerNames</span></span>
<span data-ttu-id="5ac8a-123">指定要為其建立遷移方案之卷容器名稱的陣列。</span><span class="sxs-lookup"><span data-stu-id="5ac8a-123">Specifies an array of volume container names for which to create a migration plan.</span></span>

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

### <span data-ttu-id="5ac8a-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="5ac8a-124">-Profile</span></span>
<span data-ttu-id="5ac8a-125">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="5ac8a-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5ac8a-126">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="5ac8a-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5ac8a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ac8a-127">CommonParameters</span></span>
<span data-ttu-id="5ac8a-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5ac8a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ac8a-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5ac8a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ac8a-130">輸入</span><span class="sxs-lookup"><span data-stu-id="5ac8a-130">INPUTS</span></span>

### <span data-ttu-id="5ac8a-131">所有</span><span class="sxs-lookup"><span data-stu-id="5ac8a-131">None</span></span>

## <span data-ttu-id="5ac8a-132">輸出</span><span class="sxs-lookup"><span data-stu-id="5ac8a-132">OUTPUTS</span></span>

### <span data-ttu-id="5ac8a-133">字串</span><span class="sxs-lookup"><span data-stu-id="5ac8a-133">String</span></span>
<span data-ttu-id="5ac8a-134">如果您已在裝置中成功啟動遷移方案作業，這個 Cmdlet 會傳回它的狀態。</span><span class="sxs-lookup"><span data-stu-id="5ac8a-134">This cmdlet returns the status of the migration plan job if it has been successfully started in the appliance.</span></span>

## <span data-ttu-id="5ac8a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="5ac8a-135">NOTES</span></span>

## <span data-ttu-id="5ac8a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="5ac8a-136">RELATED LINKS</span></span>

[<span data-ttu-id="5ac8a-137">AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="5ac8a-137">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


