---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: c94fbf200de5ce56cc3116b1dc7a60052f9c19f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970229"
---
# <span data-ttu-id="01548-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="01548-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="01548-102">摘要</span><span class="sxs-lookup"><span data-stu-id="01548-102">SYNOPSIS</span></span>
<span data-ttu-id="01548-103">建立要複製之 Azure 虛擬機器磁片的磁片對應物件。</span><span class="sxs-lookup"><span data-stu-id="01548-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="01548-104">句法</span><span class="sxs-lookup"><span data-stu-id="01548-104">SYNTAX</span></span>

### <span data-ttu-id="01548-105">AzureToAzure (預設) </span><span class="sxs-lookup"><span data-stu-id="01548-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="01548-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="01548-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-RecoveryDiskEncryptionSetId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-FailoverDiskName <String>] [-TfoDiskName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01548-107">說明</span><span class="sxs-lookup"><span data-stu-id="01548-107">DESCRIPTION</span></span>
<span data-ttu-id="01548-108">建立磁片對應物件，該物件會將 Azure 虛擬機器磁片對應至快取儲存空間帳戶，並將目標儲存空間帳戶 (復原區域) ，以用於複製磁片。</span><span class="sxs-lookup"><span data-stu-id="01548-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="01548-109">示例</span><span class="sxs-lookup"><span data-stu-id="01548-109">EXAMPLES</span></span>

### <span data-ttu-id="01548-110">範例1</span><span class="sxs-lookup"><span data-stu-id="01548-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="01548-111">建立要複製之 Azure 虛擬機器磁片的磁片對應物件。在 Azure to Azure EnableDr 期間使用並重新保護作業。</span><span class="sxs-lookup"><span data-stu-id="01548-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="01548-112">範例2</span><span class="sxs-lookup"><span data-stu-id="01548-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType
```

<span data-ttu-id="01548-113">針對要複製的 Azure 虛擬機器磁片，建立受管理的磁片對應物件。在 Azure to Azure EnableDr 期間使用並重新保護作業。</span><span class="sxs-lookup"><span data-stu-id="01548-113">Create a managed disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="01548-114">範例3</span><span class="sxs-lookup"><span data-stu-id="01548-114">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -DiskEncryptionVaultId $keyVaultId -DiskEncryptionSecretUrl $secret `
-KeyEncryptionKeyUrl $keyUrl -KeyEncryptionVaultId $keyVaultId
```

<span data-ttu-id="01548-115">建立受管理的磁片對應物件，並針對要複製的 Azure 虛擬機器磁片使用單一密碼加密設定。在 Azure to Azure EnableDr 期間使用並重新保護作業。</span><span class="sxs-lookup"><span data-stu-id="01548-115">Create a managed disk mapping object with one pass encryption settings for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="01548-116">範例4</span><span class="sxs-lookup"><span data-stu-id="01548-116">Example 4</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -RecoveryDiskEncryptionSetId $RecoveryDiskEncryptionSetId
```

<span data-ttu-id="01548-117">針對要複製的 Azure 虛擬機器磁片，建立具有目標磁片加密集識別碼的 managed 磁片對應物件。在 Azure to Azure EnableDr 期間使用並重新保護作業。</span><span class="sxs-lookup"><span data-stu-id="01548-117">Create a managed disk mapping object with target disk encryption set Id, for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

## <span data-ttu-id="01548-118">參數</span><span class="sxs-lookup"><span data-stu-id="01548-118">PARAMETERS</span></span>

### <span data-ttu-id="01548-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01548-119">-DefaultProfile</span></span>
<span data-ttu-id="01548-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="01548-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01548-121">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="01548-121">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="01548-122">指定磁片加密機密 url。</span><span class="sxs-lookup"><span data-stu-id="01548-122">Specifies the disk encryption secret url.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01548-123">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="01548-123">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="01548-124">指定磁片加密金鑰 vault ARM Id。</span><span class="sxs-lookup"><span data-stu-id="01548-124">Specifies the disk encryption key vault ARM Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01548-125">-DiskId</span><span class="sxs-lookup"><span data-stu-id="01548-125">-DiskId</span></span>
<span data-ttu-id="01548-126">指定受管理磁片的磁片識別碼。</span><span class="sxs-lookup"><span data-stu-id="01548-126">Specifies the disk id of managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01548-127">-FailoverDiskName</span><span class="sxs-lookup"><span data-stu-id="01548-127">-FailoverDiskName</span></span>
<span data-ttu-id="01548-128">指定在容錯移轉期間建立的磁片名稱。</span><span class="sxs-lookup"><span data-stu-id="01548-128">Specifies the name of the disk created during failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01548-129">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="01548-129">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="01548-130">指定金鑰加密 Url。</span><span class="sxs-lookup"><span data-stu-id="01548-130">Specifies the key encryption Url.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01548-131">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="01548-131">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="01548-132">指定金鑰加密金鑰 vault ARM Id。</span><span class="sxs-lookup"><span data-stu-id="01548-132">Specifies the key encryption key vault ARM Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01548-133">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="01548-133">-LogStorageAccountId</span></span>
<span data-ttu-id="01548-134">指定要用來儲存複製記錄的記錄或快取儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="01548-134">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="01548-135">-ManagedDisk</span><span class="sxs-lookup"><span data-stu-id="01548-135">-ManagedDisk</span></span>
<span data-ttu-id="01548-136">指定所管理磁片的輸入。</span><span class="sxs-lookup"><span data-stu-id="01548-136">Specifies the input is for managed disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01548-137">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="01548-137">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="01548-138">指定要複製的 Azure 儲存空間帳戶 ID。</span><span class="sxs-lookup"><span data-stu-id="01548-138">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01548-139">-RecoveryDiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="01548-139">-RecoveryDiskEncryptionSetId</span></span>
<span data-ttu-id="01548-140">指定要用於恢復磁片的 Azure 磁片加密集識別碼。</span><span class="sxs-lookup"><span data-stu-id="01548-140">Specifies the ID of the Azure disk encryption set to be used for recovery disks.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01548-141">-RecoveryReplicaDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="01548-141">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="01548-142">指定複製的受管理磁片的帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="01548-142">Specifies the account type of replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, StandardSSD_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01548-143">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="01548-143">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="01548-144">為已複製的受管理磁片指定復原資源群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="01548-144">Specifies the recovery resource group id for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01548-145">-RecoveryTargetDiskAccountType</span><span class="sxs-lookup"><span data-stu-id="01548-145">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="01548-146">指定複製的受管理磁片的復原目標磁片。</span><span class="sxs-lookup"><span data-stu-id="01548-146">Specifies the recovery target disk for replicated managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:
Accepted values: Premium_LRS, Standard_LRS, StandardSSD_LRS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01548-147">-TfoDiskName</span><span class="sxs-lookup"><span data-stu-id="01548-147">-TfoDiskName</span></span>
<span data-ttu-id="01548-148">指定在測試容錯移轉期間建立的磁片名稱。</span><span class="sxs-lookup"><span data-stu-id="01548-148">Specifies the name of the disk created during test failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01548-149">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="01548-149">-VhdUri</span></span>
<span data-ttu-id="01548-150">指定此對應對應之磁片的 VHD URI。</span><span class="sxs-lookup"><span data-stu-id="01548-150">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01548-151">-確認</span><span class="sxs-lookup"><span data-stu-id="01548-151">-Confirm</span></span>
<span data-ttu-id="01548-152">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="01548-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01548-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01548-153">-WhatIf</span></span>
<span data-ttu-id="01548-154">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="01548-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01548-155">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="01548-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01548-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01548-156">CommonParameters</span></span>
<span data-ttu-id="01548-157">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="01548-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01548-158">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="01548-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01548-159">輸入</span><span class="sxs-lookup"><span data-stu-id="01548-159">INPUTS</span></span>

### <span data-ttu-id="01548-160">所有</span><span class="sxs-lookup"><span data-stu-id="01548-160">None</span></span>

## <span data-ttu-id="01548-161">輸出</span><span class="sxs-lookup"><span data-stu-id="01548-161">OUTPUTS</span></span>

### <span data-ttu-id="01548-162">RecoveryServices. SiteRecovery. ASRAzuretoAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="01548-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="01548-163">筆記</span><span class="sxs-lookup"><span data-stu-id="01548-163">NOTES</span></span>

## <span data-ttu-id="01548-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="01548-164">RELATED LINKS</span></span>
