---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: f0147cea03d4b535102efd53af1a4d5f88338530
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286427"
---
# <span data-ttu-id="29dfd-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="29dfd-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="29dfd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="29dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="29dfd-103">啟用具有指定備份保護原則之專案的備份。</span><span class="sxs-lookup"><span data-stu-id="29dfd-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="29dfd-104">句法</span><span class="sxs-lookup"><span data-stu-id="29dfd-104">SYNTAX</span></span>

### <span data-ttu-id="29dfd-105">AzureVMComputeEnableProtection (預設) </span><span class="sxs-lookup"><span data-stu-id="29dfd-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29dfd-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="29dfd-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29dfd-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="29dfd-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29dfd-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="29dfd-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29dfd-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="29dfd-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29dfd-110">說明</span><span class="sxs-lookup"><span data-stu-id="29dfd-110">DESCRIPTION</span></span>
<span data-ttu-id="29dfd-111">**Enable-AzRecoveryServicesBackupProtection** Cmdlet 會將保護原則與專案建立關聯，以啟用備份。</span><span class="sxs-lookup"><span data-stu-id="29dfd-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet enables the backup by associating a protection policy with the item.</span></span>
<span data-ttu-id="29dfd-112">使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29dfd-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="29dfd-113">示例</span><span class="sxs-lookup"><span data-stu-id="29dfd-113">EXAMPLES</span></span>

### <span data-ttu-id="29dfd-114">範例1：為專案啟用備份保護</span><span class="sxs-lookup"><span data-stu-id="29dfd-114">Example 1: Enable Backup protection for an item</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="29dfd-115">第一個 Cmdlet 會取得預設原則物件，然後將它儲存在 $Pol 變數中。</span><span class="sxs-lookup"><span data-stu-id="29dfd-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="29dfd-116">第二個 Cmdlet 會指定要備份的磁片 Lun，並將其儲存在 $inclusionDiskLUNS 變數中。</span><span class="sxs-lookup"><span data-stu-id="29dfd-116">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="29dfd-117">第三個 Cmdlet 會使用 $Pol 中的原則，為名為 V2VM 的 ARM 虛擬機器設定備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="29dfd-117">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

### <span data-ttu-id="29dfd-118">範例2</span><span class="sxs-lookup"><span data-stu-id="29dfd-118">Example 2</span></span>

<span data-ttu-id="29dfd-119">啟用具有指定備份保護原則之專案的備份。</span><span class="sxs-lookup"><span data-stu-id="29dfd-119">Enables backup for an item with a specified Backup protection policy.</span></span> <span data-ttu-id="29dfd-120"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="29dfd-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupProtection -Item $Item -Policy $Pol -VaultId $vault
```

## <span data-ttu-id="29dfd-121">參數</span><span class="sxs-lookup"><span data-stu-id="29dfd-121">PARAMETERS</span></span>

### <span data-ttu-id="29dfd-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29dfd-122">-DefaultProfile</span></span>
<span data-ttu-id="29dfd-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="29dfd-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29dfd-124">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="29dfd-124">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="29dfd-125">僅指定備份 OS 磁片的選項</span><span class="sxs-lookup"><span data-stu-id="29dfd-125">Option to specify to backup OS disks only</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29dfd-126">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="29dfd-126">-ExclusionDisksList</span></span>
<span data-ttu-id="29dfd-127">要在備份中排除的磁片 Lun 清單，其餘部分會自動包含在其中。</span><span class="sxs-lookup"><span data-stu-id="29dfd-127">List of Disk LUNs to be excluded in backup and the rest are automatically included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29dfd-128">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="29dfd-128">-InclusionDisksList</span></span>
<span data-ttu-id="29dfd-129">在 [備份] 中包含的磁片 Lun 清單，其餘部分會自動排除在作業系統磁片以外。</span><span class="sxs-lookup"><span data-stu-id="29dfd-129">List of Disk LUNs to be included in backup and the rest are automatically excluded except OS disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29dfd-130">-專案</span><span class="sxs-lookup"><span data-stu-id="29dfd-130">-Item</span></span>
<span data-ttu-id="29dfd-131">指定此 Cmdlet 針對其啟用保護的備份專案。</span><span class="sxs-lookup"><span data-stu-id="29dfd-131">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="29dfd-132">若要取得 **AzureRmRecoveryServicesBackupItem** ，請使用 Get-AzRecoveryServicesBackupItem Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29dfd-132">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29dfd-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="29dfd-133">-Name</span></span>
<span data-ttu-id="29dfd-134">指定備份專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="29dfd-134">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, AzureFileShareEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29dfd-135">-原則</span><span class="sxs-lookup"><span data-stu-id="29dfd-135">-Policy</span></span>
<span data-ttu-id="29dfd-136">指定此 Cmdlet 與專案相關聯的保護原則。</span><span class="sxs-lookup"><span data-stu-id="29dfd-136">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="29dfd-137">若要取得 **AzureRmRecoveryServicesBackupProtectionPolicy** 物件，請使用 Get-AzRecoveryServicesBackupProtectionPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="29dfd-137">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29dfd-138">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="29dfd-138">-ProtectableItem</span></span>
<span data-ttu-id="29dfd-139">指定要使用指定原則保護的專案。</span><span class="sxs-lookup"><span data-stu-id="29dfd-139">Specifies the item to be protected with the given policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: AzureWorkloadEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29dfd-140">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="29dfd-140">-ResetExclusionSettings</span></span>
<span data-ttu-id="29dfd-141">指定重設與專案相關聯的磁片排除設定</span><span class="sxs-lookup"><span data-stu-id="29dfd-141">Specifies to reset disk exclusion setting associated with the item</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29dfd-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29dfd-142">-ResourceGroupName</span></span>
<span data-ttu-id="29dfd-143">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="29dfd-143">Specifies the name of the resource group.</span></span>
<span data-ttu-id="29dfd-144">請僅針對 ARM 虛擬機器指定此參數。</span><span class="sxs-lookup"><span data-stu-id="29dfd-144">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29dfd-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="29dfd-145">-StorageAccountName</span></span>
<span data-ttu-id="29dfd-146">Azure 檔案共用儲存空間帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="29dfd-146">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29dfd-147">-VaultId</span><span class="sxs-lookup"><span data-stu-id="29dfd-147">-VaultId</span></span>
<span data-ttu-id="29dfd-148">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="29dfd-148">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29dfd-149">-確認</span><span class="sxs-lookup"><span data-stu-id="29dfd-149">-Confirm</span></span>
<span data-ttu-id="29dfd-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="29dfd-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29dfd-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29dfd-151">-WhatIf</span></span>
<span data-ttu-id="29dfd-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="29dfd-152">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="29dfd-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29dfd-153">CommonParameters</span></span>
<span data-ttu-id="29dfd-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="29dfd-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29dfd-155">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="29dfd-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29dfd-156">輸入</span><span class="sxs-lookup"><span data-stu-id="29dfd-156">INPUTS</span></span>

### <span data-ttu-id="29dfd-157">System.object</span><span class="sxs-lookup"><span data-stu-id="29dfd-157">System.String</span></span>

### <span data-ttu-id="29dfd-158">ItemBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="29dfd-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="29dfd-159">輸出</span><span class="sxs-lookup"><span data-stu-id="29dfd-159">OUTPUTS</span></span>

### <span data-ttu-id="29dfd-160">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="29dfd-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="29dfd-161">筆記</span><span class="sxs-lookup"><span data-stu-id="29dfd-161">NOTES</span></span>

## <span data-ttu-id="29dfd-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="29dfd-162">RELATED LINKS</span></span>

[<span data-ttu-id="29dfd-163">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="29dfd-163">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="29dfd-164">AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="29dfd-164">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


