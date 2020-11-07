---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 23272A36-8F55-41A8-AFC9-2EEE0FA55DA3
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd341437019b6adbe6c2a5a93076baff61e1f0d7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967704"
---
# <span data-ttu-id="a3b3f-101">Import-AzureStorSimpleLegacyVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="a3b3f-101">Import-AzureStorSimpleLegacyVolumeContainer</span></span>

## <span data-ttu-id="a3b3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a3b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b3f-103">開始遷移大量容器。</span><span class="sxs-lookup"><span data-stu-id="a3b3f-103">Starts the migration of volume containers.</span></span>

## <span data-ttu-id="a3b3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="a3b3f-104">SYNTAX</span></span>

### <span data-ttu-id="a3b3f-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="a3b3f-105">MigrateSpecificContainer</span></span>
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> -LegacyContainerNames <String[]>
 [-SkipACRs] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a3b3f-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="a3b3f-106">MigrateAllContainer</span></span>
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> [-All] [-SkipACRs] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a3b3f-107">說明</span><span class="sxs-lookup"><span data-stu-id="a3b3f-107">DESCRIPTION</span></span>
<span data-ttu-id="a3b3f-108">匯 **入-AzureStorSimpleLegacyVolumeContainer** Cmdlet 會開始從舊版裝置將大量容器遷移至目標裝置。</span><span class="sxs-lookup"><span data-stu-id="a3b3f-108">The **Import-AzureStorSimpleLegacyVolumeContainer** cmdlet starts the migration of volume containers from a legacy appliance to the target appliance.</span></span>

## <span data-ttu-id="a3b3f-109">示例</span><span class="sxs-lookup"><span data-stu-id="a3b3f-109">EXAMPLES</span></span>

### <span data-ttu-id="a3b3f-110">範例1：匯入舊版的磁片容器</span><span class="sxs-lookup"><span data-stu-id="a3b3f-110">Example 1: Import a legacy volume container</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

<span data-ttu-id="a3b3f-111">這個命令會為命名的容器匯入舊版的磁片容器。</span><span class="sxs-lookup"><span data-stu-id="a3b3f-111">This command imports a legacy volume container for the named container.</span></span>
<span data-ttu-id="a3b3f-112">這個 Cmdlet 會開始匯入，然後傳回一則訊息。</span><span class="sxs-lookup"><span data-stu-id="a3b3f-112">The cmdlet starts the import, and then returns a message.</span></span>

### <span data-ttu-id="a3b3f-113">範例2：匯入所有舊版的磁片容器</span><span class="sxs-lookup"><span data-stu-id="a3b3f-113">Example 2: Import all legacy volume containers</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

<span data-ttu-id="a3b3f-114">這個命令會從已匯入的配置檔案中匯入所有舊版的磁片容器。</span><span class="sxs-lookup"><span data-stu-id="a3b3f-114">This command imports all legacy volume containers from configuration file imported.</span></span>
<span data-ttu-id="a3b3f-115">這個 Cmdlet 會開始匯入，然後傳回一則訊息。</span><span class="sxs-lookup"><span data-stu-id="a3b3f-115">The cmdlet starts the import, and then returns a message.</span></span>

## <span data-ttu-id="a3b3f-116">參數</span><span class="sxs-lookup"><span data-stu-id="a3b3f-116">PARAMETERS</span></span>

### <span data-ttu-id="a3b3f-117">-全部</span><span class="sxs-lookup"><span data-stu-id="a3b3f-117">-All</span></span>
<span data-ttu-id="a3b3f-118">表示此 Cmdlet 會將匯入的設定檔案中的所有卷容器匯入至目標裝置。</span><span class="sxs-lookup"><span data-stu-id="a3b3f-118">Indicates that this cmdlet imports all volume containers in the imported configuration file to the target device.</span></span>

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

### <span data-ttu-id="a3b3f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a3b3f-119">-Force</span></span>
<span data-ttu-id="a3b3f-120">表示此 Cmdlet 會在不同的裝置上匯入音量容器，即使已在其他裝置上匯入了卷容器也一樣。</span><span class="sxs-lookup"><span data-stu-id="a3b3f-120">Indicates that this cmdlet imports volume container on a different device, even if volume container has been imported on a different device.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b3f-121">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="a3b3f-121">-LegacyConfigId</span></span>
<span data-ttu-id="a3b3f-122">指定舊版裝置之設定的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="a3b3f-122">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="a3b3f-123">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="a3b3f-123">-LegacyContainerNames</span></span>
<span data-ttu-id="a3b3f-124">指定要套用遷移方案之卷容器名稱的陣列。</span><span class="sxs-lookup"><span data-stu-id="a3b3f-124">Specifies an array of volume container names for which the migration plan applies.</span></span>

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

### <span data-ttu-id="a3b3f-125">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a3b3f-125">-Profile</span></span>
<span data-ttu-id="a3b3f-126">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a3b3f-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a3b3f-127">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a3b3f-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a3b3f-128">-SkipACRs</span><span class="sxs-lookup"><span data-stu-id="a3b3f-128">-SkipACRs</span></span>
<span data-ttu-id="a3b3f-129">表示匯入處理常式會跳過存取控制記錄以供遷移。</span><span class="sxs-lookup"><span data-stu-id="a3b3f-129">Indicates that the import process skips access control records for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3b3f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b3f-130">CommonParameters</span></span>
<span data-ttu-id="a3b3f-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a3b3f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3b3f-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a3b3f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b3f-133">輸入</span><span class="sxs-lookup"><span data-stu-id="a3b3f-133">INPUTS</span></span>

## <span data-ttu-id="a3b3f-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a3b3f-134">OUTPUTS</span></span>

### <span data-ttu-id="a3b3f-135">字串</span><span class="sxs-lookup"><span data-stu-id="a3b3f-135">String</span></span>
<span data-ttu-id="a3b3f-136">如果已在裝置中成功啟動，這個命令會傳回 [遷移匯入量] 容器工作的狀態。</span><span class="sxs-lookup"><span data-stu-id="a3b3f-136">This command returns the status of the migration import volume container job if it has been successfully started in the appliance.</span></span>

## <span data-ttu-id="a3b3f-137">筆記</span><span class="sxs-lookup"><span data-stu-id="a3b3f-137">NOTES</span></span>

## <span data-ttu-id="a3b3f-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="a3b3f-138">RELATED LINKS</span></span>

[<span data-ttu-id="a3b3f-139">AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="a3b3f-139">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="a3b3f-140">匯入-AzureStorSimpleLegacyApplianceConfig</span><span class="sxs-lookup"><span data-stu-id="a3b3f-140">Import-AzureStorSimpleLegacyApplianceConfig</span></span>](./Import-AzureStorSimpleLegacyApplianceConfig.md)


