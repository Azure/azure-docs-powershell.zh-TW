---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: E33F9131-9240-4D50-972D-810775AF1506
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Start-AzureRmSiteRecoveryTestFailoverJob.md
ms.openlocfilehash: 330af3701741cbc83573afbbe7e283fdee294cdf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454820"
---
# <span data-ttu-id="0a010-101">Start-AzureRmSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="0a010-101">Start-AzureRmSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="0a010-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a010-102">SYNOPSIS</span></span>
<span data-ttu-id="0a010-103">針對網站恢復保護實體啟動測試容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="0a010-103">Starts a test failover for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a010-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a010-104">SYNTAX</span></span>

### <span data-ttu-id="0a010-105">ByPEObject (預設) </span><span class="sxs-lookup"><span data-stu-id="0a010-105">ByPEObject (Default)</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a010-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="0a010-106">ByRPObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a010-107">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="0a010-107">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a010-108">ByRPObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="0a010-108">ByRPObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a010-109">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="0a010-109">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a010-110">ByPEObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="0a010-110">ByPEObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a010-111">ByRPIObject</span><span class="sxs-lookup"><span data-stu-id="0a010-111">ByRPIObject</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DataEncryptionPrimaryCertFile <String>] [-DataEncryptionSecondaryCertFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a010-112">ByRPIObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="0a010-112">ByRPIObjectWithVMNetwork</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -VMNetwork <ASRNetwork> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a010-113">ByRPIObjectWithAzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="0a010-113">ByRPIObjectWithAzureVMNetworkId</span></span>
```
Start-AzureRmSiteRecoveryTestFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> -AzureVMNetworkId <String> [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a010-114">說明</span><span class="sxs-lookup"><span data-stu-id="0a010-114">DESCRIPTION</span></span>
<span data-ttu-id="0a010-115">**Start-AzureRmSiteRecoveryTestFailoverJob** Cmdlet 會開始測試 Azure Site Recovery 保護實體或復原方案的容錯移轉。</span><span class="sxs-lookup"><span data-stu-id="0a010-115">The **Start-AzureRmSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="0a010-116">您可以使用 Get-AzureRmSiteRecoveryJob Cmdlet 來檢查作業是否已成功完成。</span><span class="sxs-lookup"><span data-stu-id="0a010-116">You can check whether the job succeeded by using the Get-AzureRmSiteRecoveryJob cmdlet.</span></span>

## <span data-ttu-id="0a010-117">示例</span><span class="sxs-lookup"><span data-stu-id="0a010-117">EXAMPLES</span></span>

## <span data-ttu-id="0a010-118">參數</span><span class="sxs-lookup"><span data-stu-id="0a010-118">PARAMETERS</span></span>

### <span data-ttu-id="0a010-119">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="0a010-119">-AzureVMNetworkId</span></span>
<span data-ttu-id="0a010-120">指定 Azure 虛擬網路識別碼。</span><span class="sxs-lookup"><span data-stu-id="0a010-120">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObjectWithAzureVMNetworkId, ByPEObjectWithAzureVMNetworkId, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a010-121">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="0a010-121">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="0a010-122">指定主要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="0a010-122">Specifies the primary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a010-123">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="0a010-123">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="0a010-124">指定次要憑證檔案。</span><span class="sxs-lookup"><span data-stu-id="0a010-124">Specifies the secondary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a010-125">方向</span><span class="sxs-lookup"><span data-stu-id="0a010-125">-Direction</span></span>
<span data-ttu-id="0a010-126">指定容錯移轉方向。</span><span class="sxs-lookup"><span data-stu-id="0a010-126">Specifies the failover direction.</span></span>
<span data-ttu-id="0a010-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0a010-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0a010-128">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="0a010-128">PrimaryToRecovery</span></span>
- <span data-ttu-id="0a010-129">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="0a010-129">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a010-130">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="0a010-130">-ProtectionEntity</span></span>
<span data-ttu-id="0a010-131">指定網站復原保護實體物件。</span><span class="sxs-lookup"><span data-stu-id="0a010-131">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject, ByPEObjectWithVMNetwork, ByPEObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a010-132">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0a010-132">-RecoveryPlan</span></span>
<span data-ttu-id="0a010-133">指定復原方案物件。</span><span class="sxs-lookup"><span data-stu-id="0a010-133">Specifies a recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject, ByRPObjectWithVMNetwork, ByRPObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a010-134">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0a010-134">-ReplicationProtectedItem</span></span>
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithVMNetwork, ByRPIObjectWithAzureVMNetworkId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a010-135">-VMNetwork</span><span class="sxs-lookup"><span data-stu-id="0a010-135">-VMNetwork</span></span>
<span data-ttu-id="0a010-136">指定網站復原虛擬機器網路。</span><span class="sxs-lookup"><span data-stu-id="0a010-136">Specifies the Site Recovery virtual machine network.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetwork
Parameter Sets: ByRPObjectWithVMNetwork, ByPEObjectWithVMNetwork, ByRPIObjectWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a010-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a010-137">-DefaultProfile</span></span>
<span data-ttu-id="0a010-138">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a010-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a010-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a010-139">CommonParameters</span></span>
<span data-ttu-id="0a010-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a010-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a010-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0a010-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a010-142">輸入</span><span class="sxs-lookup"><span data-stu-id="0a010-142">INPUTS</span></span>

### <span data-ttu-id="0a010-143">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="0a010-143">ASRProtectionEntity</span></span>
<span data-ttu-id="0a010-144">形參 "ProtectionEntity" 接受管線中 "ASRProtectionEntity" 類型的值</span><span class="sxs-lookup"><span data-stu-id="0a010-144">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

### <span data-ttu-id="0a010-145">ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0a010-145">ASRRecoveryPlan</span></span>
<span data-ttu-id="0a010-146">形參 "RecoveryPlan" 接受管線中 "ASRRecoveryPlan" 類型的值</span><span class="sxs-lookup"><span data-stu-id="0a010-146">Parameter 'RecoveryPlan' accepts value of type 'ASRRecoveryPlan' from the pipeline</span></span>

### <span data-ttu-id="0a010-147">ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="0a010-147">ASRReplicationProtectedItem</span></span>
<span data-ttu-id="0a010-148">形參 "ReplicationProtectedItem" 接受管線中 "ASRReplicationProtectedItem" 類型的值</span><span class="sxs-lookup"><span data-stu-id="0a010-148">Parameter 'ReplicationProtectedItem' accepts value of type 'ASRReplicationProtectedItem' from the pipeline</span></span>

## <span data-ttu-id="0a010-149">輸出</span><span class="sxs-lookup"><span data-stu-id="0a010-149">OUTPUTS</span></span>

### <span data-ttu-id="0a010-150">ASRJob 中的 SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="0a010-150">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0a010-151">筆記</span><span class="sxs-lookup"><span data-stu-id="0a010-151">NOTES</span></span>

## <span data-ttu-id="0a010-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a010-152">RELATED LINKS</span></span>

[<span data-ttu-id="0a010-153">AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="0a010-153">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)
