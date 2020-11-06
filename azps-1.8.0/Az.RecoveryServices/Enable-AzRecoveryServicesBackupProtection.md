---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 7f29c0bef53d75be4f5b253e3a15bf78cbacd04b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621196"
---
# <span data-ttu-id="94f2e-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="94f2e-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="94f2e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="94f2e-102">SYNOPSIS</span></span>
<span data-ttu-id="94f2e-103">啟用具有指定備份保護原則之專案的備份。</span><span class="sxs-lookup"><span data-stu-id="94f2e-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="94f2e-104">句法</span><span class="sxs-lookup"><span data-stu-id="94f2e-104">SYNTAX</span></span>

### <span data-ttu-id="94f2e-105">AzureVMComputeEnableProtection (預設) </span><span class="sxs-lookup"><span data-stu-id="94f2e-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ResourceGroupName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94f2e-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="94f2e-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94f2e-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="94f2e-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94f2e-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="94f2e-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94f2e-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="94f2e-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94f2e-110">說明</span><span class="sxs-lookup"><span data-stu-id="94f2e-110">DESCRIPTION</span></span>
<span data-ttu-id="94f2e-111">**Enable-AzRecoveryServicesBackupProtection** Cmdlet 會針對專案設定 Azure 備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="94f2e-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="94f2e-112">使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94f2e-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="94f2e-113">示例</span><span class="sxs-lookup"><span data-stu-id="94f2e-113">EXAMPLES</span></span>

### <span data-ttu-id="94f2e-114">範例1：為專案啟用備份保護</span><span class="sxs-lookup"><span data-stu-id="94f2e-114">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="94f2e-115">第一個 Cmdlet 會取得預設原則物件，然後將它儲存在 $Pol 變數中。</span><span class="sxs-lookup"><span data-stu-id="94f2e-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="94f2e-116">第二個 Cmdlet 會使用 $Pol 中的原則，為名為 V2VM 的 ARM 虛擬機器設定備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="94f2e-116">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="94f2e-117">參數</span><span class="sxs-lookup"><span data-stu-id="94f2e-117">PARAMETERS</span></span>

### <span data-ttu-id="94f2e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f2e-118">-DefaultProfile</span></span>
<span data-ttu-id="94f2e-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="94f2e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94f2e-120">-專案</span><span class="sxs-lookup"><span data-stu-id="94f2e-120">-Item</span></span>
<span data-ttu-id="94f2e-121">指定此 Cmdlet 針對其啟用保護的備份專案。</span><span class="sxs-lookup"><span data-stu-id="94f2e-121">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="94f2e-122">若要取得 **AzureRmRecoveryServicesBackupItem** ，請使用 Get-AzRecoveryServicesBackupItem Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94f2e-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="94f2e-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="94f2e-123">-Name</span></span>
<span data-ttu-id="94f2e-124">指定備份專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="94f2e-124">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="94f2e-125">-原則</span><span class="sxs-lookup"><span data-stu-id="94f2e-125">-Policy</span></span>
<span data-ttu-id="94f2e-126">指定此 Cmdlet 與專案相關聯的保護原則。</span><span class="sxs-lookup"><span data-stu-id="94f2e-126">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="94f2e-127">若要取得 **AzureRmRecoveryServicesBackupProtectionPolicy** 物件，請使用 Get-AzRecoveryServicesBackupProtectionPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94f2e-127">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94f2e-128">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="94f2e-128">-ProtectableItem</span></span>
<span data-ttu-id="94f2e-129">作業狀態的篩選值。</span><span class="sxs-lookup"><span data-stu-id="94f2e-129">Filter value for status of job.</span></span>

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

### <span data-ttu-id="94f2e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f2e-130">-ResourceGroupName</span></span>
<span data-ttu-id="94f2e-131">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="94f2e-131">Specifies the name of the resource group.</span></span>
<span data-ttu-id="94f2e-132">請僅針對 ARM 虛擬機器指定此參數。</span><span class="sxs-lookup"><span data-stu-id="94f2e-132">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="94f2e-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="94f2e-133">-ServiceName</span></span>
<span data-ttu-id="94f2e-134">指定服務名稱。</span><span class="sxs-lookup"><span data-stu-id="94f2e-134">Specifies the service name.</span></span>
<span data-ttu-id="94f2e-135">僅針對 ASM 虛擬機器指定此參數。</span><span class="sxs-lookup"><span data-stu-id="94f2e-135">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94f2e-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="94f2e-136">-StorageAccountName</span></span>
<span data-ttu-id="94f2e-137">Azure 檔案共用儲存空間帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="94f2e-137">Azure file share storage account name</span></span>

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

### <span data-ttu-id="94f2e-138">-VaultId</span><span class="sxs-lookup"><span data-stu-id="94f2e-138">-VaultId</span></span>
<span data-ttu-id="94f2e-139">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="94f2e-139">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="94f2e-140">-確認</span><span class="sxs-lookup"><span data-stu-id="94f2e-140">-Confirm</span></span>
<span data-ttu-id="94f2e-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="94f2e-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94f2e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94f2e-142">-WhatIf</span></span>
<span data-ttu-id="94f2e-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="94f2e-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94f2e-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94f2e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94f2e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f2e-145">CommonParameters</span></span>
<span data-ttu-id="94f2e-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="94f2e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f2e-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="94f2e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f2e-148">輸入</span><span class="sxs-lookup"><span data-stu-id="94f2e-148">INPUTS</span></span>

### <span data-ttu-id="94f2e-149">System.object</span><span class="sxs-lookup"><span data-stu-id="94f2e-149">System.String</span></span>

### <span data-ttu-id="94f2e-150">ItemBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="94f2e-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="94f2e-151">輸出</span><span class="sxs-lookup"><span data-stu-id="94f2e-151">OUTPUTS</span></span>

### <span data-ttu-id="94f2e-152">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="94f2e-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="94f2e-153">筆記</span><span class="sxs-lookup"><span data-stu-id="94f2e-153">NOTES</span></span>

## <span data-ttu-id="94f2e-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="94f2e-154">RELATED LINKS</span></span>

[<span data-ttu-id="94f2e-155">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="94f2e-155">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="94f2e-156">AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="94f2e-156">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


