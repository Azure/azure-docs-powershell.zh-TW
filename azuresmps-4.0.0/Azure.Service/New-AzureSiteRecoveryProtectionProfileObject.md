---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 853D5585-2A92-4B65-BA8C-EC06BEE8C237
online version: ''
schema: 2.0.0
ms.openlocfilehash: 63274c772c6085fc8c491557851673a38056aa77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967337"
---
# <span data-ttu-id="b6de2-101">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="b6de2-101">New-AzureSiteRecoveryProtectionProfileObject</span></span>

## <span data-ttu-id="b6de2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b6de2-102">SYNOPSIS</span></span>
<span data-ttu-id="b6de2-103">建立網站復原保護設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="b6de2-103">Creates a Site Recovery protection profile object.</span></span>

## <span data-ttu-id="b6de2-104">句法</span><span class="sxs-lookup"><span data-stu-id="b6de2-104">SYNTAX</span></span>

### <span data-ttu-id="b6de2-105">EnterpriseToAzure (預設) </span><span class="sxs-lookup"><span data-stu-id="b6de2-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 -RecoveryAzureSubscription <String> -RecoveryAzureStorageAccount <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b6de2-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="b6de2-106">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-CompressionEnabled] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-AllowReplicaDeletion] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b6de2-107">說明</span><span class="sxs-lookup"><span data-stu-id="b6de2-107">DESCRIPTION</span></span>
<span data-ttu-id="b6de2-108">**新的-AzureSiteRecoveryProtectionProfileObject** Cmdlet 會建立 Azure Site Recovery 保護設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="b6de2-108">The **New-AzureSiteRecoveryProtectionProfileObject** cmdlet creates an Azure Site Recovery protection profile object.</span></span>
<span data-ttu-id="b6de2-109">這個 Cmdlet 會建立要與其他 Cmdlet 搭配使用的 **ASRProtectionProfile** 物件。</span><span class="sxs-lookup"><span data-stu-id="b6de2-109">This cmdlet creates an **ASRProtectionProfile** object to use with other cmdlets.</span></span>

## <span data-ttu-id="b6de2-110">示例</span><span class="sxs-lookup"><span data-stu-id="b6de2-110">EXAMPLES</span></span>

### <span data-ttu-id="b6de2-111">範例1：建立保護設定檔</span><span class="sxs-lookup"><span data-stu-id="b6de2-111">Example 1: Create a protection profile</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
Name                                     : 
ID                                       : 
ReplicationProvider                      : HyperVReplica
HyperVReplicaProviderSettingsObject      : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaProviderSettings
HyperVReplicaAzureProviderSettingsObject :
```

<span data-ttu-id="b6de2-112">這個命令會建立保護設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="b6de2-112">This command creates a protection profile object.</span></span>

### <span data-ttu-id="b6de2-113">範例2：建立 HyperVReplicaAzure 提供者的保護設定檔</span><span class="sxs-lookup"><span data-stu-id="b6de2-113">Example 2: Create a protection profile for HyperVReplicaAzure provider</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -Name "ProtectionProfile" -ReplicationProvider "HyperVReplicaAzure" -RecoveryAzureSubscription "cb53d0c3-bd59-4721-89bc-06916a9147ef" -RecoveryAzureStorageAccount "Contoso01" -ReplicationFrequencyInSeconds 30 -RecoveryPoints 1 -Force
Name                                     : ProtectionProfile
ID                                       : 
ReplicationProvider                      : HyperVReplicaAzure
HyperVReplicaProviderSettingsObject      : 
HyperVReplicaAzureProviderSettingsObject : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaAzureProviderSettings
```

<span data-ttu-id="b6de2-114">這個命令會建立 HyperVReplicaAzure 提供者的保護設定檔。</span><span class="sxs-lookup"><span data-stu-id="b6de2-114">This command creates a protection profile for a HyperVReplicaAzure provider.</span></span>

## <span data-ttu-id="b6de2-115">參數</span><span class="sxs-lookup"><span data-stu-id="b6de2-115">PARAMETERS</span></span>

### <span data-ttu-id="b6de2-116">-AllowReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="b6de2-116">-AllowReplicaDeletion</span></span>
<span data-ttu-id="b6de2-117">表示保護設定檔可讓您刪除複本實體。</span><span class="sxs-lookup"><span data-stu-id="b6de2-117">Indicates that the protection profile enables deletion of replica entities.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6de2-118">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="b6de2-118">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="b6de2-119">指定應用程式一致快照的頻率（以小時為單位）。</span><span class="sxs-lookup"><span data-stu-id="b6de2-119">Specifies the frequency, in hours, for application consistent snapshots.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6de2-120">-驗證</span><span class="sxs-lookup"><span data-stu-id="b6de2-120">-Authentication</span></span>
<span data-ttu-id="b6de2-121">指定要使用的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="b6de2-121">Specifies the type of authentication to use.</span></span>
<span data-ttu-id="b6de2-122">此參數可接受的值為： [憑證] 和 [Kerberos]。</span><span class="sxs-lookup"><span data-stu-id="b6de2-122">The acceptable values for this parameter are: Certificate and Kerberos.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6de2-123">-CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="b6de2-123">-CompressionEnabled</span></span>
<span data-ttu-id="b6de2-124">表示保護設定檔可讓您壓縮。</span><span class="sxs-lookup"><span data-stu-id="b6de2-124">Indicates that the protection profile enables compression.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6de2-125">-Force</span><span class="sxs-lookup"><span data-stu-id="b6de2-125">-Force</span></span>
<span data-ttu-id="b6de2-126">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b6de2-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b6de2-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="b6de2-127">-Name</span></span>
<span data-ttu-id="b6de2-128">指定保護設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6de2-128">Specifies a name for the protection profile.</span></span>

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

### <span data-ttu-id="b6de2-129">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b6de2-129">-Profile</span></span>
<span data-ttu-id="b6de2-130">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b6de2-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b6de2-131">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b6de2-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b6de2-132">-RecoveryAzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b6de2-132">-RecoveryAzureStorageAccount</span></span>
<span data-ttu-id="b6de2-133">指定要儲存 Azure 副本實體之 Azure 儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6de2-133">Specifies the name of an Azure Storage account on which to store the Azure replica entity.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6de2-134">-RecoveryAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="b6de2-134">-RecoveryAzureSubscription</span></span>
<span data-ttu-id="b6de2-135">指定儲存空間帳戶的 Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="b6de2-135">Specifies the ID for an Azure Subscription for a storage account.</span></span>
<span data-ttu-id="b6de2-136">此參數會參照要儲存 Azure 副本實體的帳戶。</span><span class="sxs-lookup"><span data-stu-id="b6de2-136">This parameter refers to the account on which to store the Azure replica entity.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6de2-137">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="b6de2-137">-RecoveryPoints</span></span>
<span data-ttu-id="b6de2-138">指定要保留復原點數的小時數。</span><span class="sxs-lookup"><span data-stu-id="b6de2-138">Specifies the number of hours to retain recovery points.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6de2-139">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="b6de2-139">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="b6de2-140">指定複製的頻率間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="b6de2-140">Specifies the frequency interval, in seconds, for replication.</span></span> <span data-ttu-id="b6de2-141">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b6de2-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b6de2-142">為期</span><span class="sxs-lookup"><span data-stu-id="b6de2-142">30</span></span> 
- <span data-ttu-id="b6de2-143">300</span><span class="sxs-lookup"><span data-stu-id="b6de2-143">300</span></span> 
- <span data-ttu-id="b6de2-144">900</span><span class="sxs-lookup"><span data-stu-id="b6de2-144">900</span></span>

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

### <span data-ttu-id="b6de2-145">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="b6de2-145">-ReplicationMethod</span></span>
<span data-ttu-id="b6de2-146">指定複製方法。</span><span class="sxs-lookup"><span data-stu-id="b6de2-146">Specifies the replication method.</span></span> <span data-ttu-id="b6de2-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b6de2-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b6de2-148">Online.</span><span class="sxs-lookup"><span data-stu-id="b6de2-148">Online.</span></span>
<span data-ttu-id="b6de2-149">在網路上複製。</span><span class="sxs-lookup"><span data-stu-id="b6de2-149">Replication over the network.</span></span>
- <span data-ttu-id="b6de2-150">處於.</span><span class="sxs-lookup"><span data-stu-id="b6de2-150">Offline.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6de2-151">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="b6de2-151">-ReplicationPort</span></span>
<span data-ttu-id="b6de2-152">指定發生複製的埠號碼。</span><span class="sxs-lookup"><span data-stu-id="b6de2-152">Specifies the number of the port on which the replication occurs.</span></span>

```yaml
Type: UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6de2-153">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="b6de2-153">-ReplicationProvider</span></span>
<span data-ttu-id="b6de2-154">指定複製提供者的類型。</span><span class="sxs-lookup"><span data-stu-id="b6de2-154">Specifies the type of replication provider.</span></span> <span data-ttu-id="b6de2-155">此參數可接受的值為： HyperVReplica 和 HyperVReplicaAzure。</span><span class="sxs-lookup"><span data-stu-id="b6de2-155">The acceptable values for this parameter are: HyperVReplica and HyperVReplicaAzure.</span></span>

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

### <span data-ttu-id="b6de2-156">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="b6de2-156">-ReplicationStartTime</span></span>
<span data-ttu-id="b6de2-157">指定複製的開始時間。</span><span class="sxs-lookup"><span data-stu-id="b6de2-157">Specifies the start time of the replication.</span></span>
<span data-ttu-id="b6de2-158">在您開始工作後的24小時內指定時間。</span><span class="sxs-lookup"><span data-stu-id="b6de2-158">Specify a time within 24 hours after you start the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6de2-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6de2-159">CommonParameters</span></span>
<span data-ttu-id="b6de2-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b6de2-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6de2-161">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b6de2-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6de2-162">輸入</span><span class="sxs-lookup"><span data-stu-id="b6de2-162">INPUTS</span></span>

## <span data-ttu-id="b6de2-163">輸出</span><span class="sxs-lookup"><span data-stu-id="b6de2-163">OUTPUTS</span></span>

## <span data-ttu-id="b6de2-164">筆記</span><span class="sxs-lookup"><span data-stu-id="b6de2-164">NOTES</span></span>

## <span data-ttu-id="b6de2-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6de2-165">RELATED LINKS</span></span>

[<span data-ttu-id="b6de2-166">Azure Site Recovery 服務 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b6de2-166">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)


