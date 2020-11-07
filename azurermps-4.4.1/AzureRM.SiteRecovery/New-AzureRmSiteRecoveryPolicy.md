---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 85C543FE-BBC1-4A1B-9974-1D3BF520085C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: e876e1a7beeee19cd68ac629eb08d48356f98da8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625951"
---
# <span data-ttu-id="6a464-101">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="6a464-101">New-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="6a464-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6a464-102">SYNOPSIS</span></span>
<span data-ttu-id="6a464-103">建立網站復原複製原則。</span><span class="sxs-lookup"><span data-stu-id="6a464-103">Creates a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a464-104">句法</span><span class="sxs-lookup"><span data-stu-id="6a464-104">SYNTAX</span></span>

### <span data-ttu-id="6a464-105">EnterpriseToAzure (預設) </span><span class="sxs-lookup"><span data-stu-id="6a464-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6a464-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="6a464-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a464-107">說明</span><span class="sxs-lookup"><span data-stu-id="6a464-107">DESCRIPTION</span></span>
<span data-ttu-id="6a464-108">**新的-AzureRmSiteRecoveryPolicy** Cmdlet 會建立 Azure Site Recovery 複製原則。</span><span class="sxs-lookup"><span data-stu-id="6a464-108">The **New-AzureRmSiteRecoveryPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="6a464-109">複製原則是用來指定複製設定，例如複製頻率和復原點數的數量。</span><span class="sxs-lookup"><span data-stu-id="6a464-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="6a464-110">示例</span><span class="sxs-lookup"><span data-stu-id="6a464-110">EXAMPLES</span></span>

## <span data-ttu-id="6a464-111">參數</span><span class="sxs-lookup"><span data-stu-id="6a464-111">PARAMETERS</span></span>

### <span data-ttu-id="6a464-112">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="6a464-112">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="6a464-113">指定應用程式一致快照的頻率（以小時為單位）。</span><span class="sxs-lookup"><span data-stu-id="6a464-113">Specifies the frequency of the application consistent snapshot in hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a464-114">-驗證</span><span class="sxs-lookup"><span data-stu-id="6a464-114">-Authentication</span></span>
<span data-ttu-id="6a464-115">指定所使用的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="6a464-115">Specifies the type of authentication used.</span></span>
<span data-ttu-id="6a464-116">有效值為：</span><span class="sxs-lookup"><span data-stu-id="6a464-116">Valid values are:</span></span>

- <span data-ttu-id="6a464-117">憑證</span><span class="sxs-lookup"><span data-stu-id="6a464-117">Certificate</span></span>
-  <span data-ttu-id="6a464-118">V5</span><span class="sxs-lookup"><span data-stu-id="6a464-118">Kerberos</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a464-119">壓縮</span><span class="sxs-lookup"><span data-stu-id="6a464-119">-Compression</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a464-120">-加密</span><span class="sxs-lookup"><span data-stu-id="6a464-120">-Encryption</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a464-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="6a464-121">-Name</span></span>
<span data-ttu-id="6a464-122">指定識別網站復原複製原則的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="6a464-122">Specifies a friendly name which identifies the Site Recovery replication policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a464-123">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6a464-123">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="6a464-124">指定複製目標的 Azure 儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="6a464-124">Specifies the Azure storage account ID of the replication target.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a464-125">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="6a464-125">-RecoveryPoints</span></span>
<span data-ttu-id="6a464-126">指定要保留復原點數的小時數。</span><span class="sxs-lookup"><span data-stu-id="6a464-126">Specifies the number of hours to retain recovery points.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a464-127">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="6a464-127">-ReplicaDeletion</span></span>
```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a464-128">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="6a464-128">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="6a464-129">指定複製頻率間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6a464-129">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="6a464-130">有效值為：</span><span class="sxs-lookup"><span data-stu-id="6a464-130">Valid values are:</span></span>

- <span data-ttu-id="6a464-131">為期</span><span class="sxs-lookup"><span data-stu-id="6a464-131">30</span></span>
- <span data-ttu-id="6a464-132">300</span><span class="sxs-lookup"><span data-stu-id="6a464-132">300</span></span>
- <span data-ttu-id="6a464-133">900</span><span class="sxs-lookup"><span data-stu-id="6a464-133">900</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a464-134">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="6a464-134">-ReplicationMethod</span></span>
<span data-ttu-id="6a464-135">指定複製方法。</span><span class="sxs-lookup"><span data-stu-id="6a464-135">Specifies the replication method.</span></span>
<span data-ttu-id="6a464-136">有效值為：</span><span class="sxs-lookup"><span data-stu-id="6a464-136">Valid values are:</span></span>

- <span data-ttu-id="6a464-137">Online</span><span class="sxs-lookup"><span data-stu-id="6a464-137">Online</span></span>
- <span data-ttu-id="6a464-138">處於</span><span class="sxs-lookup"><span data-stu-id="6a464-138">Offline</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a464-139">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="6a464-139">-ReplicationPort</span></span>
<span data-ttu-id="6a464-140">指定用於複製的埠。</span><span class="sxs-lookup"><span data-stu-id="6a464-140">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a464-141">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="6a464-141">-ReplicationProvider</span></span>
<span data-ttu-id="6a464-142">指定複製提供者。</span><span class="sxs-lookup"><span data-stu-id="6a464-142">Specifies the replication provider.</span></span>
<span data-ttu-id="6a464-143">有效值為：</span><span class="sxs-lookup"><span data-stu-id="6a464-143">Valid values are:</span></span>

- <span data-ttu-id="6a464-144">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="6a464-144">HyperVReplica2012R2</span></span>
- <span data-ttu-id="6a464-145">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="6a464-145">HyperVReplica2012</span></span>
- <span data-ttu-id="6a464-146">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="6a464-146">HyperVReplicaAzure</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a464-147">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="6a464-147">-ReplicationStartTime</span></span>
<span data-ttu-id="6a464-148">指定複製開始時間。</span><span class="sxs-lookup"><span data-stu-id="6a464-148">Specifies the replication start time.</span></span>
<span data-ttu-id="6a464-149">從工作開始，該作業不能遲于24小時。</span><span class="sxs-lookup"><span data-stu-id="6a464-149">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a464-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a464-150">-DefaultProfile</span></span>
<span data-ttu-id="6a464-151">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6a464-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a464-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a464-152">CommonParameters</span></span>
<span data-ttu-id="6a464-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6a464-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a464-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6a464-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a464-155">輸入</span><span class="sxs-lookup"><span data-stu-id="6a464-155">INPUTS</span></span>

## <span data-ttu-id="6a464-156">輸出</span><span class="sxs-lookup"><span data-stu-id="6a464-156">OUTPUTS</span></span>

## <span data-ttu-id="6a464-157">筆記</span><span class="sxs-lookup"><span data-stu-id="6a464-157">NOTES</span></span>

## <span data-ttu-id="6a464-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="6a464-158">RELATED LINKS</span></span>

[<span data-ttu-id="6a464-159">AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="6a464-159">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="6a464-160">移除-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="6a464-160">Remove-AzureRmSiteRecoveryPolicy</span></span>](./Remove-AzureRmSiteRecoveryPolicy.md)
