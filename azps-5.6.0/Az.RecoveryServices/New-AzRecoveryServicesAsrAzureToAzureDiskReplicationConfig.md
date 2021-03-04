---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrazuretoazurediskreplicationconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig.md
ms.openlocfilehash: 6863c1c8b486784339cf0e1a52cc0793c0cc31f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915241"
---
# <span data-ttu-id="247f9-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="247f9-101">New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="247f9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="247f9-102">SYNOPSIS</span></span>
<span data-ttu-id="247f9-103">為要複製的 Azure 虛擬機器磁片建立磁片映射物件。</span><span class="sxs-lookup"><span data-stu-id="247f9-103">Creates a disk mapping object for Azure virtual machine disks to be replicated.</span></span>

## <span data-ttu-id="247f9-104">語法</span><span class="sxs-lookup"><span data-stu-id="247f9-104">SYNTAX</span></span>

### <span data-ttu-id="247f9-105">AzureToAzure (預設) </span><span class="sxs-lookup"><span data-stu-id="247f9-105">AzureToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri <String> -LogStorageAccountId <String>
 -RecoveryAzureStorageAccountId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="247f9-106">AzureToAzureManagedAz</span><span class="sxs-lookup"><span data-stu-id="247f9-106">AzureToAzureManagedDisk</span></span>
```
New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig [-ManagedDisk] -LogStorageAccountId <String>
 -DiskId <String> -RecoveryResourceGroupId <String> -RecoveryReplicaDiskAccountType <String>
 -RecoveryTargetDiskAccountType <String> [-RecoveryDiskEncryptionSetId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-FailoverDiskName <String>] [-TfoDiskName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="247f9-107">描述</span><span class="sxs-lookup"><span data-stu-id="247f9-107">DESCRIPTION</span></span>
<span data-ttu-id="247f9-108">建立一個磁片地圖物件，將 Azure 虛擬機器磁片與緩存儲存帳戶及目標儲存帳戶 (修復) 用於複本磁片。</span><span class="sxs-lookup"><span data-stu-id="247f9-108">Creates a disk mapping object that maps an Azure virtual machine disk to the cache storage account and target storage account (recovery region) to be used to replicate the disk.</span></span>

## <span data-ttu-id="247f9-109">例子</span><span class="sxs-lookup"><span data-stu-id="247f9-109">EXAMPLES</span></span>

### <span data-ttu-id="247f9-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="247f9-110">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -VhdUri  $vhdUri -RecoveryAzureStorageAccountId $recoveryStorageAccountId -LogStorageAccountId $logStorageAccountId
```

<span data-ttu-id="247f9-111">為要複製的 Azure 虛擬機器磁片建立磁片映射物件。在 Azure 期間用於 Azure EnableDr 及重新保護作業。</span><span class="sxs-lookup"><span data-stu-id="247f9-111">Create a disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="247f9-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="247f9-112">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType
```

<span data-ttu-id="247f9-113">為要複製的 Azure 虛擬機器磁片建立受管理的磁片地圖物件。在 Azure 期間用於 Azure EnableDr 及重新保護作業。</span><span class="sxs-lookup"><span data-stu-id="247f9-113">Create a managed disk mapping object for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="247f9-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="247f9-114">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -DiskEncryptionVaultId $keyVaultId -DiskEncryptionSecretUrl $secret `
-KeyEncryptionKeyUrl $keyUrl -KeyEncryptionVaultId $keyVaultId
```

<span data-ttu-id="247f9-115">針對要複製的 Azure 虛擬機器磁片，使用一次加密設定建立受管理的磁片地圖物件。在 Azure 期間用於 Azure EnableDr 及重新保護作業。</span><span class="sxs-lookup"><span data-stu-id="247f9-115">Create a managed disk mapping object with one pass encryption settings for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

### <span data-ttu-id="247f9-116">範例 4</span><span class="sxs-lookup"><span data-stu-id="247f9-116">Example 4</span></span>
```
PS C:\> New-AzRecoveryServicesAsrAzureToAzureDiskReplicationConfig -ManagedDisk -LogStorageAccountId $logStorageAccountId -DiskId $diskId -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryReplicaDiskAccountType $RecoveryReplicaDiskAccountType -RecoveryTargetDiskAccountType $RecoveryTargetDiskAccountType -RecoveryDiskEncryptionSetId $RecoveryDiskEncryptionSetId
```

<span data-ttu-id="247f9-117">使用目標磁片加密集 Id 建立受管理的磁片地圖物件，以複製 Azure 虛擬機器磁片。在 Azure 期間用於 Azure EnableDr 及重新保護作業。</span><span class="sxs-lookup"><span data-stu-id="247f9-117">Create a managed disk mapping object with target disk encryption set Id, for Azure virtual machine disks to be replicated.Used during Azure to Azure EnableDr and re-protect operation.</span></span>

## <span data-ttu-id="247f9-118">參數</span><span class="sxs-lookup"><span data-stu-id="247f9-118">PARAMETERS</span></span>

### <span data-ttu-id="247f9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="247f9-119">-DefaultProfile</span></span>
<span data-ttu-id="247f9-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="247f9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="247f9-121">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="247f9-121">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="247f9-122">指定磁片加密機密 URL。</span><span class="sxs-lookup"><span data-stu-id="247f9-122">Specifies the disk encryption secret url.</span></span>

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

### <span data-ttu-id="247f9-123">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="247f9-123">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="247f9-124">指定磁片加密金鑰庫 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="247f9-124">Specifies the disk encryption key vault ARM Id.</span></span>

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

### <span data-ttu-id="247f9-125">-DiskId</span><span class="sxs-lookup"><span data-stu-id="247f9-125">-DiskId</span></span>
<span data-ttu-id="247f9-126">指定受管理磁片的磁片識別碼。</span><span class="sxs-lookup"><span data-stu-id="247f9-126">Specifies the disk id of managed disk.</span></span>

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

### <span data-ttu-id="247f9-127">-Failover前名</span><span class="sxs-lookup"><span data-stu-id="247f9-127">-FailoverDiskName</span></span>
<span data-ttu-id="247f9-128">指定在容錯移轉期間所建立磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="247f9-128">Specifies the name of the disk created during failover.</span></span>

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

### <span data-ttu-id="247f9-129">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="247f9-129">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="247f9-130">指定金鑰加密 URL。</span><span class="sxs-lookup"><span data-stu-id="247f9-130">Specifies the key encryption Url.</span></span>

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

### <span data-ttu-id="247f9-131">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="247f9-131">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="247f9-132">指定金鑰加密金鑰庫 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="247f9-132">Specifies the key encryption key vault ARM Id.</span></span>

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

### <span data-ttu-id="247f9-133">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="247f9-133">-LogStorageAccountId</span></span>
<span data-ttu-id="247f9-134">指定要用來儲存複製記錄之記錄或緩存儲存帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="247f9-134">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

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

### <span data-ttu-id="247f9-135">-Managed前小分</span><span class="sxs-lookup"><span data-stu-id="247f9-135">-ManagedDisk</span></span>
<span data-ttu-id="247f9-136">指定用於受管理的磁片的輸入。</span><span class="sxs-lookup"><span data-stu-id="247f9-136">Specifies the input is for managed disk.</span></span>

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

### <span data-ttu-id="247f9-137">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="247f9-137">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="247f9-138">指定要複製到的 Azure 儲存空間帳戶識別碼。</span><span class="sxs-lookup"><span data-stu-id="247f9-138">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="247f9-139">-RecoveryCryptEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="247f9-139">-RecoveryDiskEncryptionSetId</span></span>
<span data-ttu-id="247f9-140">指定要用於修復磁片的 Azure 磁片加密集識別碼。</span><span class="sxs-lookup"><span data-stu-id="247f9-140">Specifies the ID of the Azure disk encryption set to be used for recovery disks.</span></span>

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

### <span data-ttu-id="247f9-141">-RecoveryReplicaCountType</span><span class="sxs-lookup"><span data-stu-id="247f9-141">-RecoveryReplicaDiskAccountType</span></span>
<span data-ttu-id="247f9-142">指定複製受管理的磁片的帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="247f9-142">Specifies the account type of replicated managed disk.</span></span>

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

### <span data-ttu-id="247f9-143">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="247f9-143">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="247f9-144">指定複本受管理磁片的復原資源群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="247f9-144">Specifies the recovery resource group id for replicated managed disk.</span></span>

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

### <span data-ttu-id="247f9-145">-RecoveryTargetCountAccountType</span><span class="sxs-lookup"><span data-stu-id="247f9-145">-RecoveryTargetDiskAccountType</span></span>
<span data-ttu-id="247f9-146">指定複本受管理磁片的復原目標磁片。</span><span class="sxs-lookup"><span data-stu-id="247f9-146">Specifies the recovery target disk for replicated managed disk.</span></span>

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

### <span data-ttu-id="247f9-147">-TfoNameName</span><span class="sxs-lookup"><span data-stu-id="247f9-147">-TfoDiskName</span></span>
<span data-ttu-id="247f9-148">指定測試容錯移轉期間所建立磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="247f9-148">Specifies the name of the disk created during test failover.</span></span>

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

### <span data-ttu-id="247f9-149">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="247f9-149">-VhdUri</span></span>
<span data-ttu-id="247f9-150">指定此對應對應之磁片的 VHD URI。</span><span class="sxs-lookup"><span data-stu-id="247f9-150">Specify the VHD URI of the disk that this mapping corresponds to.</span></span>

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

### <span data-ttu-id="247f9-151">-確認</span><span class="sxs-lookup"><span data-stu-id="247f9-151">-Confirm</span></span>
<span data-ttu-id="247f9-152">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="247f9-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="247f9-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="247f9-153">-WhatIf</span></span>
<span data-ttu-id="247f9-154">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="247f9-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="247f9-155">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="247f9-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="247f9-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="247f9-156">CommonParameters</span></span>
<span data-ttu-id="247f9-157">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="247f9-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="247f9-158">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="247f9-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="247f9-159">輸入</span><span class="sxs-lookup"><span data-stu-id="247f9-159">INPUTS</span></span>

### <span data-ttu-id="247f9-160">沒有</span><span class="sxs-lookup"><span data-stu-id="247f9-160">None</span></span>

## <span data-ttu-id="247f9-161">輸出</span><span class="sxs-lookup"><span data-stu-id="247f9-161">OUTPUTS</span></span>

### <span data-ttu-id="247f9-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureAzureReplicationConfig</span><span class="sxs-lookup"><span data-stu-id="247f9-162">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig</span></span>

## <span data-ttu-id="247f9-163">筆記</span><span class="sxs-lookup"><span data-stu-id="247f9-163">NOTES</span></span>

## <span data-ttu-id="247f9-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="247f9-164">RELATED LINKS</span></span>
