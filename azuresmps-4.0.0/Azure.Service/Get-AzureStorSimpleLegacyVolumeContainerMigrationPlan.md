---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E4F6D096-E265-49CF-AA73-E9C807F8383B
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0207d4b7eddfe56a8e4e86aac6899d19c10f44e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967002"
---
# <span data-ttu-id="198ae-101">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="198ae-101">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>

## <span data-ttu-id="198ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="198ae-102">SYNOPSIS</span></span>
<span data-ttu-id="198ae-103">取得舊版容器的遷移方案。</span><span class="sxs-lookup"><span data-stu-id="198ae-103">Gets migration plans for legacy containers.</span></span>

## <span data-ttu-id="198ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="198ae-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan [-LegacyConfigId <String>]
 [-LegacyContainerNames <String[]>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="198ae-105">說明</span><span class="sxs-lookup"><span data-stu-id="198ae-105">DESCRIPTION</span></span>
<span data-ttu-id="198ae-106">**AzureStorSimpleLEgacyVolumeContainerMigrationPlan** Cmdlet 會取得舊版容器的遷移方案。</span><span class="sxs-lookup"><span data-stu-id="198ae-106">The **Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** cmdlet gets migration plans for legacy containers.</span></span>
<span data-ttu-id="198ae-107">依其舊版配置識別碼來指定遷移方案。</span><span class="sxs-lookup"><span data-stu-id="198ae-107">Specify a migration plan by its legacy configuration ID.</span></span>
<span data-ttu-id="198ae-108">如果遷移方案的建立仍在進行中，此 Cmdlet 會取得遷移方案的狀態。</span><span class="sxs-lookup"><span data-stu-id="198ae-108">If creation of the migration plan is still in progress, this cmdlet gets the status of the migration plan.</span></span>
<span data-ttu-id="198ae-109">如果遷移方案已完成，此 Cmdlet 會傳回舊版容器的實際遷移方案。</span><span class="sxs-lookup"><span data-stu-id="198ae-109">If the migration plan is completed, this cmdlet returns the actual migration plan for the set of legacy containers.</span></span>
<span data-ttu-id="198ae-110">如果您沒有指定 *LegacyConfigId* 參數，這個 Cmdlet 會傳回配置識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="198ae-110">If you do not specify the *LegacyConfigId* parameter, this cmdlet returns a list of configuration IDs.</span></span>

## <span data-ttu-id="198ae-111">示例</span><span class="sxs-lookup"><span data-stu-id="198ae-111">EXAMPLES</span></span>

### <span data-ttu-id="198ae-112">範例1：取得方案的狀態</span><span class="sxs-lookup"><span data-stu-id="198ae-112">Example 1: Get the status of a plan</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 51e413fd-c2c9-4108-88cd-a0e792eab80a_PS
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 4c6398ef-35a0-4d1c-931e-d9d45599a97a_PS
VERBOSE: 2015-04-08 13:48:17 ClientRequestId: ef7a7e35-6dff-46cd-9df3-cb5fa25d149e_PS
VERBOSE: Request Id : fd7e502f273885468f633a44567bcb3f, HttpResponse OK
VERBOSE: List of volume containers: 


LegacyConfigId                    : f16463bd-94a9-4c3c-91c2-7a3ba7120087
DeviceName                        : ARUNKM-N4
MigrationTimeEstimationCompleted  : CloudConfigurationName        : OneSDKAzureCloud
                                    EstimatedTimeForLatestBackup  : 15Minutes
                                    EstimatedTimeForAllBackups    : 15Minutes
                                    These estimates are assuming 20 MBps bandwidth. Refer to migration guide to re-calculate for lower bandwidths. 



MigrationTimeEstimationInProgress : None
MigrationTimeEstimationFailed     : None
MigrationTimeEstimationNotStarted : None
```

<span data-ttu-id="198ae-113">這個命令會取得遷移方案的狀態。</span><span class="sxs-lookup"><span data-stu-id="198ae-113">This command gets the status of the migration plan.</span></span>
<span data-ttu-id="198ae-114">狀態包括 [假設的頻寬]、[估計時間] 和 [相關資訊]。</span><span class="sxs-lookup"><span data-stu-id="198ae-114">The status includes assumed bandwidth, estimated time and, related information.</span></span>

### <span data-ttu-id="198ae-115">範例2：取得現有方案的識別碼</span><span class="sxs-lookup"><span data-stu-id="198ae-115">Example 2: Get the IDs of existing plans</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 813da56c-0cfc-4325-80db-08ef32bdde1e_PS
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 9e7cf244-1894-490a-be02-749834a99318_PS
VERBOSE: List of LegacyConfig Ids on the resource: 

LegacyConfigId                                              DeviceName
--------------                                              ----------
1e1f10a0-3dff-4249-b847-4930061cd87a                        ARUNKM-N4
26d4096d-49b6-4102-b188-0446ece73c8b                        ARUNKM-N4
```

<span data-ttu-id="198ae-116">這個命令會取得所有遷移方案的配置識別碼。</span><span class="sxs-lookup"><span data-stu-id="198ae-116">This command gets all the configuration IDs of migration plans.</span></span>

## <span data-ttu-id="198ae-117">參數</span><span class="sxs-lookup"><span data-stu-id="198ae-117">PARAMETERS</span></span>

### <span data-ttu-id="198ae-118">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="198ae-118">-LegacyConfigId</span></span>
<span data-ttu-id="198ae-119">指定舊版裝置之設定的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="198ae-119">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="198ae-120">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="198ae-120">-LegacyContainerNames</span></span>
<span data-ttu-id="198ae-121">指定此 Cmdlet 取得其遷移方案之卷容器名稱的陣列。</span><span class="sxs-lookup"><span data-stu-id="198ae-121">Specifies an array of volume container names for which this cmdlet gets a migration plan.</span></span>

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

### <span data-ttu-id="198ae-122">-設定檔</span><span class="sxs-lookup"><span data-stu-id="198ae-122">-Profile</span></span>
<span data-ttu-id="198ae-123">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="198ae-123">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="198ae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="198ae-124">CommonParameters</span></span>
<span data-ttu-id="198ae-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="198ae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="198ae-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="198ae-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="198ae-127">輸入</span><span class="sxs-lookup"><span data-stu-id="198ae-127">INPUTS</span></span>

### <span data-ttu-id="198ae-128">所有</span><span class="sxs-lookup"><span data-stu-id="198ae-128">None</span></span>

## <span data-ttu-id="198ae-129">輸出</span><span class="sxs-lookup"><span data-stu-id="198ae-129">OUTPUTS</span></span>

### <span data-ttu-id="198ae-130">MigrationPlanMsg</span><span class="sxs-lookup"><span data-stu-id="198ae-130">MigrationPlanMsg</span></span>
<span data-ttu-id="198ae-131">這個 Cmdlet 會傳回一個 **MigrationPlanMsg** 物件，其中包含遷移方案作業的狀態、假設的頻寬（以百萬位元/秒為單位），以及估計時間（以分鐘為單位）。</span><span class="sxs-lookup"><span data-stu-id="198ae-131">This cmdlet returns a **MigrationPlanMsg** object that contains the status of the migration plan job, assumed bandwidth in megabits per second, and estimated time in minutes.</span></span>

## <span data-ttu-id="198ae-132">筆記</span><span class="sxs-lookup"><span data-stu-id="198ae-132">NOTES</span></span>

## <span data-ttu-id="198ae-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="198ae-133">RELATED LINKS</span></span>

[<span data-ttu-id="198ae-134">開始-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="198ae-134">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


