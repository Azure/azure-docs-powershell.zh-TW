---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/enable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Enable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 357256d1c1a754915cbebc978e5c4ccf4440ccf4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625264"
---
# <span data-ttu-id="c31df-101">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="c31df-101">Enable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="c31df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c31df-102">SYNOPSIS</span></span>
<span data-ttu-id="c31df-103">啟用具有指定備份保護原則之專案的備份。</span><span class="sxs-lookup"><span data-stu-id="c31df-103">Enables backup for an item with a specified Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c31df-104">句法</span><span class="sxs-lookup"><span data-stu-id="c31df-104">SYNTAX</span></span>

### <span data-ttu-id="c31df-105">AzureVMComputeEnableProtection (預設) </span><span class="sxs-lookup"><span data-stu-id="c31df-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-ResourceGroupName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c31df-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="c31df-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c31df-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="c31df-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 -StorageAccountName <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c31df-108">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="c31df-108">ModifyProtection</span></span>
```
Enable-AzureRmRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c31df-109">說明</span><span class="sxs-lookup"><span data-stu-id="c31df-109">DESCRIPTION</span></span>
<span data-ttu-id="c31df-110">**Enable-AzureRmRecoveryServicesBackupProtection** Cmdlet 會針對專案設定 Azure 備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="c31df-110">The **Enable-AzureRmRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="c31df-111">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c31df-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="c31df-112">示例</span><span class="sxs-lookup"><span data-stu-id="c31df-112">EXAMPLES</span></span>

### <span data-ttu-id="c31df-113">範例1：為專案啟用備份保護</span><span class="sxs-lookup"><span data-stu-id="c31df-113">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzureRmRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="c31df-114">第一個 Cmdlet 會取得預設原則物件，然後將它儲存在 $Pol 變數中。</span><span class="sxs-lookup"><span data-stu-id="c31df-114">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="c31df-115">第二個 Cmdlet 會使用 $Pol 中的原則，為名為 V2VM 的 ARM 虛擬機器設定備份保護原則。</span><span class="sxs-lookup"><span data-stu-id="c31df-115">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="c31df-116">參數</span><span class="sxs-lookup"><span data-stu-id="c31df-116">PARAMETERS</span></span>

### <span data-ttu-id="c31df-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c31df-117">-DefaultProfile</span></span>
<span data-ttu-id="c31df-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c31df-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c31df-119">-專案</span><span class="sxs-lookup"><span data-stu-id="c31df-119">-Item</span></span>
<span data-ttu-id="c31df-120">指定此 Cmdlet 針對其啟用保護的備份專案。</span><span class="sxs-lookup"><span data-stu-id="c31df-120">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="c31df-121">若要取得 **AzureRmRecoveryServicesBackupItem** ，請使用 Get-AzureRmRecoveryServicesBackupItem Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c31df-121">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="c31df-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="c31df-122">-Name</span></span>
<span data-ttu-id="c31df-123">指定備份專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="c31df-123">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="c31df-124">-原則</span><span class="sxs-lookup"><span data-stu-id="c31df-124">-Policy</span></span>
<span data-ttu-id="c31df-125">指定此 Cmdlet 與專案相關聯的保護原則。</span><span class="sxs-lookup"><span data-stu-id="c31df-125">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="c31df-126">若要取得 **AzureRmRecoveryServicesBackupProtectionPolicy** 物件，請使用 Get-AzureRmRecoveryServicesBackupProtectionPolicy Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c31df-126">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzureRmRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="c31df-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c31df-127">-ResourceGroupName</span></span>
<span data-ttu-id="c31df-128">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c31df-128">Specifies the name of the resource group.</span></span>
<span data-ttu-id="c31df-129">請僅針對 ARM 虛擬機器指定此參數。</span><span class="sxs-lookup"><span data-stu-id="c31df-129">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="c31df-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c31df-130">-ServiceName</span></span>
<span data-ttu-id="c31df-131">指定服務名稱。</span><span class="sxs-lookup"><span data-stu-id="c31df-131">Specifies the service name.</span></span>
<span data-ttu-id="c31df-132">僅針對 ASM 虛擬機器指定此參數。</span><span class="sxs-lookup"><span data-stu-id="c31df-132">Specify this parameter only for ASM virtual machines.</span></span>

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

### <span data-ttu-id="c31df-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c31df-133">-StorageAccountName</span></span>
<span data-ttu-id="c31df-134">Azure 檔案共用儲存空間帳戶名稱</span><span class="sxs-lookup"><span data-stu-id="c31df-134">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c31df-135">-VaultId</span><span class="sxs-lookup"><span data-stu-id="c31df-135">-VaultId</span></span>
<span data-ttu-id="c31df-136">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="c31df-136">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="c31df-137">-確認</span><span class="sxs-lookup"><span data-stu-id="c31df-137">-Confirm</span></span>
<span data-ttu-id="c31df-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c31df-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c31df-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c31df-139">-WhatIf</span></span>
<span data-ttu-id="c31df-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c31df-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c31df-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c31df-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c31df-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c31df-142">CommonParameters</span></span>
<span data-ttu-id="c31df-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c31df-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c31df-144">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c31df-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c31df-145">輸入</span><span class="sxs-lookup"><span data-stu-id="c31df-145">INPUTS</span></span>

### <span data-ttu-id="c31df-146">System.object</span><span class="sxs-lookup"><span data-stu-id="c31df-146">System.String</span></span>
<span data-ttu-id="c31df-147">參數： VaultId (ByValue) </span><span class="sxs-lookup"><span data-stu-id="c31df-147">Parameters: VaultId (ByValue)</span></span>

### <span data-ttu-id="c31df-148">ItemBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="c31df-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>
<span data-ttu-id="c31df-149">參數： (ByValue 的專案) </span><span class="sxs-lookup"><span data-stu-id="c31df-149">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="c31df-150">輸出</span><span class="sxs-lookup"><span data-stu-id="c31df-150">OUTPUTS</span></span>

### <span data-ttu-id="c31df-151">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="c31df-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="c31df-152">筆記</span><span class="sxs-lookup"><span data-stu-id="c31df-152">NOTES</span></span>

## <span data-ttu-id="c31df-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="c31df-153">RELATED LINKS</span></span>

[<span data-ttu-id="c31df-154">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="c31df-154">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="c31df-155">AzureRmRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c31df-155">Get-AzureRmRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)


