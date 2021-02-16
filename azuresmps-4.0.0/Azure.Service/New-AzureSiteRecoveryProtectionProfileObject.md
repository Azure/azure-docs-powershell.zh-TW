---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 853D5585-2A92-4B65-BA8C-EC06BEE8C237
online version: ''
schema: 2.0.0
ms.openlocfilehash: d7681631d98f80def1076a04ab57f1774bad245c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403641"
---
# <span data-ttu-id="ffb6b-101">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="ffb6b-101">New-AzureSiteRecoveryProtectionProfileObject</span></span>

## <span data-ttu-id="ffb6b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ffb6b-102">SYNOPSIS</span></span>
<span data-ttu-id="ffb6b-103">建立網站復原保護設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-103">Creates a Site Recovery protection profile object.</span></span>

## <span data-ttu-id="ffb6b-104">語法</span><span class="sxs-lookup"><span data-stu-id="ffb6b-104">SYNTAX</span></span>

### <span data-ttu-id="ffb6b-105">EnterpriseToAzure (預設) </span><span class="sxs-lookup"><span data-stu-id="ffb6b-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 -RecoveryAzureSubscription <String> -RecoveryAzureStorageAccount <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="ffb6b-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="ffb6b-106">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-CompressionEnabled] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-AllowReplicaDeletion] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ffb6b-107">描述</span><span class="sxs-lookup"><span data-stu-id="ffb6b-107">DESCRIPTION</span></span>
<span data-ttu-id="ffb6b-108">**New-AzureSiteRecoveryProtectionProfileObject** Cmdlet 會建立 Azure 網站復原保護設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-108">The **New-AzureSiteRecoveryProtectionProfileObject** cmdlet creates an Azure Site Recovery protection profile object.</span></span>
<span data-ttu-id="ffb6b-109">此 Cmdlet 會建立 **一個 ASRProtectionProfile** 物件，以與其他 Cmdlet 一起使用。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-109">This cmdlet creates an **ASRProtectionProfile** object to use with other cmdlets.</span></span>

## <span data-ttu-id="ffb6b-110">例子</span><span class="sxs-lookup"><span data-stu-id="ffb6b-110">EXAMPLES</span></span>

### <span data-ttu-id="ffb6b-111">範例 1：建立保護設定檔</span><span class="sxs-lookup"><span data-stu-id="ffb6b-111">Example 1: Create a protection profile</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
Name                                     : 
ID                                       : 
ReplicationProvider                      : HyperVReplica
HyperVReplicaProviderSettingsObject      : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaProviderSettings
HyperVReplicaAzureProviderSettingsObject :
```

<span data-ttu-id="ffb6b-112">此命令會建立保護設定檔物件。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-112">This command creates a protection profile object.</span></span>

### <span data-ttu-id="ffb6b-113">範例 2：建立 HyperVReplicaAzure 提供者的保護設定檔</span><span class="sxs-lookup"><span data-stu-id="ffb6b-113">Example 2: Create a protection profile for HyperVReplicaAzure provider</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -Name "ProtectionProfile" -ReplicationProvider "HyperVReplicaAzure" -RecoveryAzureSubscription "cb53d0c3-bd59-4721-89bc-06916a9147ef" -RecoveryAzureStorageAccount "Contoso01" -ReplicationFrequencyInSeconds 30 -RecoveryPoints 1 -Force
Name                                     : ProtectionProfile
ID                                       : 
ReplicationProvider                      : HyperVReplicaAzure
HyperVReplicaProviderSettingsObject      : 
HyperVReplicaAzureProviderSettingsObject : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaAzureProviderSettings
```

<span data-ttu-id="ffb6b-114">此命令會為 HyperVReplicaAzure 提供者建立保護設定檔。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-114">This command creates a protection profile for a HyperVReplicaAzure provider.</span></span>

## <span data-ttu-id="ffb6b-115">參數</span><span class="sxs-lookup"><span data-stu-id="ffb6b-115">PARAMETERS</span></span>

### <span data-ttu-id="ffb6b-116">-AllowReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="ffb6b-116">-AllowReplicaDeletion</span></span>
<span data-ttu-id="ffb6b-117">表示保護設定檔可刪除複本實體。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-117">Indicates that the protection profile enables deletion of replica entities.</span></span>

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

### <span data-ttu-id="ffb6b-118">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="ffb6b-118">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="ffb6b-119">指定應用程式一致快照的頻率 ，以小時表示。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-119">Specifies the frequency, in hours, for application consistent snapshots.</span></span>

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

### <span data-ttu-id="ffb6b-120">-驗證</span><span class="sxs-lookup"><span data-stu-id="ffb6b-120">-Authentication</span></span>
<span data-ttu-id="ffb6b-121">指定要使用的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-121">Specifies the type of authentication to use.</span></span>
<span data-ttu-id="ffb6b-122">此參數可接受的值為：憑證和 Kerberos。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-122">The acceptable values for this parameter are: Certificate and Kerberos.</span></span>

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

### <span data-ttu-id="ffb6b-123">-CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="ffb6b-123">-CompressionEnabled</span></span>
<span data-ttu-id="ffb6b-124">表示保護設定檔啟用壓縮。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-124">Indicates that the protection profile enables compression.</span></span>

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

### <span data-ttu-id="ffb6b-125">-強制</span><span class="sxs-lookup"><span data-stu-id="ffb6b-125">-Force</span></span>
<span data-ttu-id="ffb6b-126">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ffb6b-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="ffb6b-127">-Name</span></span>
<span data-ttu-id="ffb6b-128">指定保護設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-128">Specifies a name for the protection profile.</span></span>

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

### <span data-ttu-id="ffb6b-129">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ffb6b-129">-Profile</span></span>
<span data-ttu-id="ffb6b-130">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ffb6b-131">如果您未指定設定檔，此 Cmdlet 會從本地預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ffb6b-132">-RecoveryAzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ffb6b-132">-RecoveryAzureStorageAccount</span></span>
<span data-ttu-id="ffb6b-133">指定要儲存 Azure 複本實體的 Azure 儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-133">Specifies the name of an Azure Storage account on which to store the Azure replica entity.</span></span>

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

### <span data-ttu-id="ffb6b-134">-RecoveryAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="ffb6b-134">-RecoveryAzureSubscription</span></span>
<span data-ttu-id="ffb6b-135">指定儲存帳戶的 Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-135">Specifies the ID for an Azure Subscription for a storage account.</span></span>
<span data-ttu-id="ffb6b-136">此參數參照儲存 Azure 複本實體的帳戶。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-136">This parameter refers to the account on which to store the Azure replica entity.</span></span>

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

### <span data-ttu-id="ffb6b-137">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="ffb6b-137">-RecoveryPoints</span></span>
<span data-ttu-id="ffb6b-138">指定要保留修復點的時數。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-138">Specifies the number of hours to retain recovery points.</span></span>

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

### <span data-ttu-id="ffb6b-139">-ReplicationFrequencyIn自秒鐘</span><span class="sxs-lookup"><span data-stu-id="ffb6b-139">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="ffb6b-140">指定複製的頻率間隔 ，以秒為單位。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-140">Specifies the frequency interval, in seconds, for replication.</span></span> <span data-ttu-id="ffb6b-141">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ffb6b-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ffb6b-142">30</span><span class="sxs-lookup"><span data-stu-id="ffb6b-142">30</span></span> 
- <span data-ttu-id="ffb6b-143">300</span><span class="sxs-lookup"><span data-stu-id="ffb6b-143">300</span></span> 
- <span data-ttu-id="ffb6b-144">900</span><span class="sxs-lookup"><span data-stu-id="ffb6b-144">900</span></span>

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

### <span data-ttu-id="ffb6b-145">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="ffb6b-145">-ReplicationMethod</span></span>
<span data-ttu-id="ffb6b-146">指定複製方法。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-146">Specifies the replication method.</span></span> <span data-ttu-id="ffb6b-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ffb6b-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ffb6b-148">線上。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-148">Online.</span></span>
<span data-ttu-id="ffb6b-149">複製網路。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-149">Replication over the network.</span></span>
- <span data-ttu-id="ffb6b-150">離線。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-150">Offline.</span></span>

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

### <span data-ttu-id="ffb6b-151">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="ffb6b-151">-ReplicationPort</span></span>
<span data-ttu-id="ffb6b-152">指定進行複製的埠數目。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-152">Specifies the number of the port on which the replication occurs.</span></span>

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

### <span data-ttu-id="ffb6b-153">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="ffb6b-153">-ReplicationProvider</span></span>
<span data-ttu-id="ffb6b-154">指定複製提供者的類型。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-154">Specifies the type of replication provider.</span></span> <span data-ttu-id="ffb6b-155">此參數可接受的值為：HyperVReplica 和 HyperVReplicaAzure。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-155">The acceptable values for this parameter are: HyperVReplica and HyperVReplicaAzure.</span></span>

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

### <span data-ttu-id="ffb6b-156">-複製啟動時間</span><span class="sxs-lookup"><span data-stu-id="ffb6b-156">-ReplicationStartTime</span></span>
<span data-ttu-id="ffb6b-157">指定複製的開始時間。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-157">Specifies the start time of the replication.</span></span>
<span data-ttu-id="ffb6b-158">指定工作開始後的 24 小時內的時間。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-158">Specify a time within 24 hours after you start the job.</span></span>

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

### <span data-ttu-id="ffb6b-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffb6b-159">CommonParameters</span></span>
<span data-ttu-id="ffb6b-160">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffb6b-161">詳細資訊請參閱 https://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ffb6b-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffb6b-162">輸入</span><span class="sxs-lookup"><span data-stu-id="ffb6b-162">INPUTS</span></span>

## <span data-ttu-id="ffb6b-163">輸出</span><span class="sxs-lookup"><span data-stu-id="ffb6b-163">OUTPUTS</span></span>

## <span data-ttu-id="ffb6b-164">筆記</span><span class="sxs-lookup"><span data-stu-id="ffb6b-164">NOTES</span></span>

## <span data-ttu-id="ffb6b-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="ffb6b-165">RELATED LINKS</span></span>




