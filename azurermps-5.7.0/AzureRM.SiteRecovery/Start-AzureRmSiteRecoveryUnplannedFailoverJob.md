---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 48494D81-A138-4D20-9286-D6A989AE70C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/start-azurermsiterecoveryunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryUnplannedFailoverJob.md
ms.openlocfilehash: 1776ec34517d613daf805fac97ecda93c1afe542
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444312"
---
# <span data-ttu-id="53992-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="53992-101">Start-AzureRmSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="53992-102">摘要</span><span class="sxs-lookup"><span data-stu-id="53992-102">SYNOPSIS</span></span>
<span data-ttu-id="53992-103">針對網站恢復保護實體或復原方案啟動未計畫的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="53992-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53992-104">句法</span><span class="sxs-lookup"><span data-stu-id="53992-104">SYNTAX</span></span>

### <span data-ttu-id="53992-105">ByPEObject (預設) </span><span class="sxs-lookup"><span data-stu-id="53992-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53992-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="53992-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53992-107">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="53992-107">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideActions] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53992-108">說明</span><span class="sxs-lookup"><span data-stu-id="53992-108">DESCRIPTION</span></span>
<span data-ttu-id="53992-109">**Start AzureRmSiteRecoveryUnplannedFailoverJob** Cmdlet 會啟動 Azure Site Recovery 保護實體或復原方案的未計畫式容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="53992-109">The **Start-AzureRmSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="53992-110">您可以使用 Get-AzureRmSiteRecoveryJob Cmdlet 來檢查作業是否成功完成。</span><span class="sxs-lookup"><span data-stu-id="53992-110">You can check whether the job succeeds by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="53992-111">示例</span><span class="sxs-lookup"><span data-stu-id="53992-111">EXAMPLES</span></span>

## <span data-ttu-id="53992-112">參數</span><span class="sxs-lookup"><span data-stu-id="53992-112">PARAMETERS</span></span>

### <span data-ttu-id="53992-113">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="53992-113">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="53992-114">指定主要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="53992-114">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="53992-115">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="53992-115">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="53992-116">指定次要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="53992-116">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="53992-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53992-117">-DefaultProfile</span></span>
<span data-ttu-id="53992-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="53992-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53992-119">方向</span><span class="sxs-lookup"><span data-stu-id="53992-119">-Direction</span></span>
<span data-ttu-id="53992-120">指定容錯移轉的方向。</span><span class="sxs-lookup"><span data-stu-id="53992-120">Specifies the direction of the failover.</span></span>
<span data-ttu-id="53992-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="53992-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="53992-122">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="53992-122">PrimaryToRecovery</span></span>
- <span data-ttu-id="53992-123">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="53992-123">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53992-124">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="53992-124">-PerformSourceSideActions</span></span>
<span data-ttu-id="53992-125">表示動作可以執行來源網站作業。</span><span class="sxs-lookup"><span data-stu-id="53992-125">Indicates that the action can perform source site operations.</span></span>

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

### <span data-ttu-id="53992-126">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="53992-126">-ProtectionEntity</span></span>
<span data-ttu-id="53992-127">指定網站復原保護實體物件。</span><span class="sxs-lookup"><span data-stu-id="53992-127">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53992-128">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="53992-128">-RecoveryPlan</span></span>
<span data-ttu-id="53992-129">指定復原方案物件。</span><span class="sxs-lookup"><span data-stu-id="53992-129">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53992-130">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="53992-130">-ReplicationProtectedItem</span></span>
```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53992-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53992-131">CommonParameters</span></span>
<span data-ttu-id="53992-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="53992-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53992-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="53992-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53992-134">輸入</span><span class="sxs-lookup"><span data-stu-id="53992-134">INPUTS</span></span>

### <span data-ttu-id="53992-135">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="53992-135">ASRProtectionEntity</span></span>
<span data-ttu-id="53992-136">形參 "ProtectionEntity" 接受管線中 "ASRProtectionEntity" 類型的值</span><span class="sxs-lookup"><span data-stu-id="53992-136">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="53992-137">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="53992-137">ASRRecoveryPlan</span></span>
<span data-ttu-id="53992-138">形參 "RecoveryPlan" 接受管線中 "ASRRecoveryPlan" 類型的值</span><span class="sxs-lookup"><span data-stu-id="53992-138">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="53992-139">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="53992-139">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="53992-140">形參 "ReplicationProtectedItem" 接受管線中 "ASRReplicationProtectedItem" 類型的值</span><span class="sxs-lookup"><span data-stu-id="53992-140">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="53992-141">輸出</span><span class="sxs-lookup"><span data-stu-id="53992-141">OUTPUTS</span></span>

### <span data-ttu-id="53992-142">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="53992-142">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="53992-143">筆記</span><span class="sxs-lookup"><span data-stu-id="53992-143">NOTES</span></span>

## <span data-ttu-id="53992-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="53992-144">RELATED LINKS</span></span>

[<span data-ttu-id="53992-145">AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="53992-145">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)


