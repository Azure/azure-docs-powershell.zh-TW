---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 358d3da36996c9b020db3a805889b7098b9c36ec
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281254"
---
# <span data-ttu-id="2cfd0-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="2cfd0-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="2cfd0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2cfd0-102">SYNOPSIS</span></span>

<span data-ttu-id="2cfd0-103">從 [備份] 中的容器取得專案。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="2cfd0-104">句法</span><span class="sxs-lookup"><span data-stu-id="2cfd0-104">SYNTAX</span></span>

### <span data-ttu-id="2cfd0-105">GetItemsForContainer (預設) </span><span class="sxs-lookup"><span data-stu-id="2cfd0-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cfd0-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="2cfd0-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cfd0-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="2cfd0-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cfd0-108">說明</span><span class="sxs-lookup"><span data-stu-id="2cfd0-108">DESCRIPTION</span></span>

<span data-ttu-id="2cfd0-109">**AzRecoveryServicesBackupItem** Cmdlet 會取得容器中受保護專案的清單，以及專案的保護狀態。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the list of protected items in a container and the protection status of the items.</span></span>
<span data-ttu-id="2cfd0-110">已登錄至 Azure 恢復服務保存庫的容器可以有一或多個可受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="2cfd0-111">針對 Azure 虛擬機器，虛擬機器容器中只能有一個備份專案。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="2cfd0-112">使用-VaultId 參數來設定 vault 內容。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="2cfd0-113">示例</span><span class="sxs-lookup"><span data-stu-id="2cfd0-113">EXAMPLES</span></span>

### <span data-ttu-id="2cfd0-114">範例1：從備份容器取得專案</span><span class="sxs-lookup"><span data-stu-id="2cfd0-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="2cfd0-115">第一個命令會取得類型為「Add-azurevm」的容器，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="2cfd0-116">第二個命令會在 $Container 中取得名為 V2VM 的備份專案，然後將它儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="2cfd0-117">範例2：從 FriendlyName 取得 Azure 檔案共用專案</span><span class="sxs-lookup"><span data-stu-id="2cfd0-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -Name "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="2cfd0-118">第一個命令會取得類型 AzureStorage 的容器，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="2cfd0-119">第二個命令會取得其 friendlyName 符合 FriendlyName 參數中傳遞之值的備份專案，然後將其儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="2cfd0-120">使用 FriendlyName 參數可能會導致傳回一個以上的 Azure 檔案共用。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="2cfd0-121">在這種情況下，請傳送 Name 參數的值作為 $BackupItem 結果集中傳回的 Name 屬性來執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-121">In such cases, execute the cmdlet by passing value for -Name parameter as the Name property returned in the result set of $BackupItem.</span></span>

## <span data-ttu-id="2cfd0-122">參數</span><span class="sxs-lookup"><span data-stu-id="2cfd0-122">PARAMETERS</span></span>

### <span data-ttu-id="2cfd0-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="2cfd0-123">-BackupManagementType</span></span>

<span data-ttu-id="2cfd0-124">受保護的資源類別。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-124">The class of resources being protected.</span></span> <span data-ttu-id="2cfd0-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2cfd0-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2cfd0-126">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="2cfd0-126">AzureVM</span></span>
- <span data-ttu-id="2cfd0-127">MAB</span><span class="sxs-lookup"><span data-stu-id="2cfd0-127">MAB</span></span>
- <span data-ttu-id="2cfd0-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="2cfd0-128">AzureStorage</span></span>
- <span data-ttu-id="2cfd0-129">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="2cfd0-129">AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfd0-130">-容器</span><span class="sxs-lookup"><span data-stu-id="2cfd0-130">-Container</span></span>

<span data-ttu-id="2cfd0-131">指定由此 Cmdlet 取得備份專案的容器物件。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-131">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="2cfd0-132">若要取得 **AzureRmRecoveryServicesBackupContainer**，請使用 **AzRecoveryServicesBackupContainer** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-132">To obtain an **AzureRmRecoveryServicesBackupContainer**, use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: GetItemsForContainer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2cfd0-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cfd0-133">-DefaultProfile</span></span>

<span data-ttu-id="2cfd0-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cfd0-135">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="2cfd0-135">-DeleteState</span></span>
<span data-ttu-id="2cfd0-136">指定專案的 deletestate 此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2cfd0-136">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2cfd0-137">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="2cfd0-137">ToBeDeleted</span></span>
- <span data-ttu-id="2cfd0-138">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="2cfd0-138">NotDeleted</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemDeleteState
Parameter Sets: (All)
Aliases:
Accepted values: ToBeDeleted, NotDeleted

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfd0-139">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2cfd0-139">-FriendlyName</span></span>
<span data-ttu-id="2cfd0-140">已備份專案的 FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2cfd0-140">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="2cfd0-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="2cfd0-141">-Name</span></span>

<span data-ttu-id="2cfd0-142">指定備份專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-142">Specifies the name of backup item.</span></span> <span data-ttu-id="2cfd0-143">針對 [檔案共用]，指定受保護檔案共用的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-143">For file share, specify the unique ID of protected file share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfd0-144">-原則</span><span class="sxs-lookup"><span data-stu-id="2cfd0-144">-Policy</span></span>

<span data-ttu-id="2cfd0-145">保護原則物件。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-145">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: GetItemsForPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfd0-146">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="2cfd0-146">-ProtectionState</span></span>

<span data-ttu-id="2cfd0-147">指定保護的狀態。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-147">Specifies the state of protection.</span></span>
<span data-ttu-id="2cfd0-148">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2cfd0-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2cfd0-149">IRPending.</span><span class="sxs-lookup"><span data-stu-id="2cfd0-149">IRPending.</span></span>
<span data-ttu-id="2cfd0-150">初始同步處理尚未開始，而且尚未有任何復原點。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-150">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="2cfd0-151">受.</span><span class="sxs-lookup"><span data-stu-id="2cfd0-151">Protected.</span></span>
<span data-ttu-id="2cfd0-152">正在進行保護。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-152">Protection is ongoing.</span></span>
- <span data-ttu-id="2cfd0-153">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="2cfd0-153">ProtectionError.</span></span>
<span data-ttu-id="2cfd0-154">出現保護錯誤。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-154">There is a protection error.</span></span>
- <span data-ttu-id="2cfd0-155">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="2cfd0-155">ProtectionStopped.</span></span>
<span data-ttu-id="2cfd0-156">已停用保護功能。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-156">Protection is disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionState
Parameter Sets: (All)
Aliases:
Accepted values: IRPending, ProtectionError, Protected, ProtectionStopped

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfd0-157">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="2cfd0-157">-ProtectionStatus</span></span>

<span data-ttu-id="2cfd0-158">指定容器中某個專案的整體保護狀態。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-158">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="2cfd0-159">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2cfd0-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2cfd0-160">健全</span><span class="sxs-lookup"><span data-stu-id="2cfd0-160">Healthy</span></span>
- <span data-ttu-id="2cfd0-161">不</span><span class="sxs-lookup"><span data-stu-id="2cfd0-161">Unhealthy</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionStatus
Parameter Sets: (All)
Aliases:
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfd0-162">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2cfd0-162">-VaultId</span></span>

<span data-ttu-id="2cfd0-163">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-163">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2cfd0-164">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="2cfd0-164">-WorkloadType</span></span>

<span data-ttu-id="2cfd0-165">資源的工作負荷類型。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-165">Workload type of the resource.</span></span> <span data-ttu-id="2cfd0-166">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2cfd0-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2cfd0-167">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="2cfd0-167">AzureVM</span></span>
- <span data-ttu-id="2cfd0-168">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="2cfd0-168">AzureFiles</span></span>
- <span data-ttu-id="2cfd0-169">MSSQL</span><span class="sxs-lookup"><span data-stu-id="2cfd0-169">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cfd0-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cfd0-170">CommonParameters</span></span>
<span data-ttu-id="2cfd0-171">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cfd0-172">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2cfd0-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cfd0-173">輸入</span><span class="sxs-lookup"><span data-stu-id="2cfd0-173">INPUTS</span></span>

### <span data-ttu-id="2cfd0-174">ContainerBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="2cfd0-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="2cfd0-175">System.object</span><span class="sxs-lookup"><span data-stu-id="2cfd0-175">System.String</span></span>

## <span data-ttu-id="2cfd0-176">輸出</span><span class="sxs-lookup"><span data-stu-id="2cfd0-176">OUTPUTS</span></span>

### <span data-ttu-id="2cfd0-177">ItemBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="2cfd0-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="2cfd0-178">筆記</span><span class="sxs-lookup"><span data-stu-id="2cfd0-178">NOTES</span></span>

## <span data-ttu-id="2cfd0-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="2cfd0-179">RELATED LINKS</span></span>

[<span data-ttu-id="2cfd0-180">備份-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="2cfd0-180">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="2cfd0-181">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="2cfd0-181">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="2cfd0-182">AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="2cfd0-182">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="2cfd0-183">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="2cfd0-183">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
