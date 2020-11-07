---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 3B4630C1-9885-4BE4-B41E-D98AF5CCD7C3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185072d1bc0d0895d4b6cfaea9470bac107d651a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967999"
---
# <span data-ttu-id="a8a41-101">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="a8a41-101">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>

## <span data-ttu-id="a8a41-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a8a41-102">SYNOPSIS</span></span>
<span data-ttu-id="a8a41-103">取得認可或回滾作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="a8a41-103">Gets the status of a commit or rollback operation.</span></span>

## <span data-ttu-id="a8a41-104">句法</span><span class="sxs-lookup"><span data-stu-id="a8a41-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId <String>
 [-LegacyContainerNames <String[]>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a8a41-105">說明</span><span class="sxs-lookup"><span data-stu-id="a8a41-105">DESCRIPTION</span></span>
<span data-ttu-id="a8a41-106">**AzureStorSimpleLegacyVolumeContainerConfirmStatus** Cmdlet 會取得 commit 或 rollback 作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="a8a41-106">The **Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus** cmdlet gets the status of the commit or rollback operation.</span></span>

## <span data-ttu-id="a8a41-107">示例</span><span class="sxs-lookup"><span data-stu-id="a8a41-107">EXAMPLES</span></span>

### <span data-ttu-id="a8a41-108">範例1：取得已完成的確認作業狀態</span><span class="sxs-lookup"><span data-stu-id="a8a41-108">Example 1: Get the status of a completed commit operation</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 2bda2b9b-1361-4787-bc04-1e081218ed76_PS
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 84bf18d8-c459-47a7-b4a8-f82ca8659672_PS
VERBOSE: 2015-04-08 13:51:12 ClientRequestId: e93f9cb7-df58-497e-bb9f-9a6a23e68925_PS


LegacyConfigId             : f16463bd-94a9-4c3c-91c2-7a3ba7120087
CommitComplete             : CloudConfigurationName : OneSDKAzureCloud
                             Operation              : Commit
                             PercentageCompleted    : 100
                             Messages               : 

CommitInProgress           : None
CommitFailed               : None
RollbackComplete           : None
RollbackInProgress         : None
RollbackFailed             : None
CommitOrRollbackNotStarted : None
```

<span data-ttu-id="a8a41-109">這個命令會取得指定容器的認可作業狀態。</span><span class="sxs-lookup"><span data-stu-id="a8a41-109">This command gets the status of a commit operation for the named container.</span></span>
<span data-ttu-id="a8a41-110">這個作業的狀態為 [已完成]。</span><span class="sxs-lookup"><span data-stu-id="a8a41-110">This operation has a status of completed.</span></span>

### <span data-ttu-id="a8a41-111">範例2：取得已完成復原作業的狀態</span><span class="sxs-lookup"><span data-stu-id="a8a41-111">Example 2: Get the status of a completed rollback operation</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 2bda2b9b-1361-4787-bc04-1e081218ed76_PS
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 84bf18d8-c459-47a7-b4a8-f82ca8659672_PS
VERBOSE: 2015-04-08 13:51:12 ClientRequestId: e93f9cb7-df58-497e-bb9f-9a6a23e68925_PS


LegacyConfigId             : f16463bd-94a9-4c3c-91c2-7a3ba7120087
CommitComplete             : None
CommitInProgress           : None
CommitFailed               : None
RollbackComplete           : CloudConfigurationName : OneSDKAzureCloud
                             Operation              : Rollback
                             PercentageCompleted    : 100
                             Messages               : 

RollbackInProgress         : None
RollbackFailed             : None
CommitOrRollbackNotStarted : None
```

<span data-ttu-id="a8a41-112">這個命令會取得指定容器的復原作業狀態。</span><span class="sxs-lookup"><span data-stu-id="a8a41-112">This command gets the status of a rollback operation for the named container.</span></span>
<span data-ttu-id="a8a41-113">這個作業的狀態為 [已完成]。</span><span class="sxs-lookup"><span data-stu-id="a8a41-113">This operation has a status of completed.</span></span>

## <span data-ttu-id="a8a41-114">參數</span><span class="sxs-lookup"><span data-stu-id="a8a41-114">PARAMETERS</span></span>

### <span data-ttu-id="a8a41-115">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="a8a41-115">-LegacyConfigId</span></span>
<span data-ttu-id="a8a41-116">指定舊版裝置之設定的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="a8a41-116">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="a8a41-117">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="a8a41-117">-LegacyContainerNames</span></span>
<span data-ttu-id="a8a41-118">指定要套用遷移方案之卷容器名稱的陣列。</span><span class="sxs-lookup"><span data-stu-id="a8a41-118">Specifies an array of volume container names for which the migration plan applies.</span></span>

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

### <span data-ttu-id="a8a41-119">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a8a41-119">-Profile</span></span>
<span data-ttu-id="a8a41-120">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a8a41-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="a8a41-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8a41-121">CommonParameters</span></span>
<span data-ttu-id="a8a41-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a8a41-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8a41-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a8a41-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8a41-124">輸入</span><span class="sxs-lookup"><span data-stu-id="a8a41-124">INPUTS</span></span>

### <span data-ttu-id="a8a41-125">所有</span><span class="sxs-lookup"><span data-stu-id="a8a41-125">None</span></span>

## <span data-ttu-id="a8a41-126">輸出</span><span class="sxs-lookup"><span data-stu-id="a8a41-126">OUTPUTS</span></span>

### <span data-ttu-id="a8a41-127">ConfirmMigrationStatusMsg</span><span class="sxs-lookup"><span data-stu-id="a8a41-127">ConfirmMigrationStatusMsg</span></span>
<span data-ttu-id="a8a41-128">這個 Cmdlet 會傳回所執行確認遷移作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="a8a41-128">This cmdlet returns the status of the confirm migration operation that is performed.</span></span>

## <span data-ttu-id="a8a41-129">筆記</span><span class="sxs-lookup"><span data-stu-id="a8a41-129">NOTES</span></span>

## <span data-ttu-id="a8a41-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="a8a41-130">RELATED LINKS</span></span>

[<span data-ttu-id="a8a41-131">確認-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="a8a41-131">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Confirm-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="a8a41-132">AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="a8a41-132">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)


