---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 75eb9975a578e1114e994b08949eda8d3dafda0e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956832"
---
# <span data-ttu-id="35b2a-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="35b2a-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="35b2a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="35b2a-102">SYNOPSIS</span></span>

<span data-ttu-id="35b2a-103">從 [備份] 中的容器取得專案。</span><span class="sxs-lookup"><span data-stu-id="35b2a-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="35b2a-104">句法</span><span class="sxs-lookup"><span data-stu-id="35b2a-104">SYNTAX</span></span>

### <span data-ttu-id="35b2a-105">GetItemsForContainer (預設) </span><span class="sxs-lookup"><span data-stu-id="35b2a-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35b2a-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="35b2a-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35b2a-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="35b2a-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35b2a-108">說明</span><span class="sxs-lookup"><span data-stu-id="35b2a-108">DESCRIPTION</span></span>

<span data-ttu-id="35b2a-109">**AzRecoveryServicesBackupItem** Cmdlet 會取得容器中的專案，或是 Azure 備份中的值，以及專案的保護狀態。</span><span class="sxs-lookup"><span data-stu-id="35b2a-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="35b2a-110">已登錄至 Azure 恢復服務保存庫的容器可以有一或多個可受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="35b2a-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="35b2a-111">針對 Azure 虛擬機器，虛擬機器容器中只能有一個備份專案。</span><span class="sxs-lookup"><span data-stu-id="35b2a-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="35b2a-112">使用-VaultId 參數來設定 vault 內容。</span><span class="sxs-lookup"><span data-stu-id="35b2a-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="35b2a-113">示例</span><span class="sxs-lookup"><span data-stu-id="35b2a-113">EXAMPLES</span></span>

### <span data-ttu-id="35b2a-114">範例1：從備份容器取得專案</span><span class="sxs-lookup"><span data-stu-id="35b2a-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="35b2a-115">第一個命令會取得類型為「Add-azurevm」的容器，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="35b2a-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="35b2a-116">第二個命令會在 $Container 中取得名為 V2VM 的備份專案，然後將它儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="35b2a-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="35b2a-117">範例2：從 FriendlyName 取得 Azure 檔案共用專案</span><span class="sxs-lookup"><span data-stu-id="35b2a-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -Name "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="35b2a-118">第一個命令會取得類型 AzureStorage 的容器，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="35b2a-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="35b2a-119">第二個命令會取得其 friendlyName 符合 FriendlyName 參數中傳遞之值的備份專案，然後將其儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="35b2a-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="35b2a-120">使用 FriendlyName 參數可能會導致傳回一個以上的 Azure 檔案共用。</span><span class="sxs-lookup"><span data-stu-id="35b2a-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="35b2a-121">在這種情況下，請使用 Name 參數，將參數值設為 $BackupItem 變數中傳回的 Name 屬性。</span><span class="sxs-lookup"><span data-stu-id="35b2a-121">In such cases use -Name parameter with parameter value as the Name property returned in $BackupItem variable.</span></span>

## <span data-ttu-id="35b2a-122">參數</span><span class="sxs-lookup"><span data-stu-id="35b2a-122">PARAMETERS</span></span>

### <span data-ttu-id="35b2a-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="35b2a-123">-BackupManagementType</span></span>

<span data-ttu-id="35b2a-124">指定備份管理類型。</span><span class="sxs-lookup"><span data-stu-id="35b2a-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="35b2a-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="35b2a-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35b2a-126">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="35b2a-126">AzureVM</span></span>
- <span data-ttu-id="35b2a-127">MARS</span><span class="sxs-lookup"><span data-stu-id="35b2a-127">MARS</span></span>
- <span data-ttu-id="35b2a-128">SCDPM</span><span class="sxs-lookup"><span data-stu-id="35b2a-128">SCDPM</span></span>
- <span data-ttu-id="35b2a-129">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="35b2a-129">AzureBackupServer</span></span>
- <span data-ttu-id="35b2a-130">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="35b2a-130">AzureSQL</span></span>
- <span data-ttu-id="35b2a-131">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="35b2a-131">AzureStorage</span></span>
- <span data-ttu-id="35b2a-132">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="35b2a-132">AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b2a-133">-容器</span><span class="sxs-lookup"><span data-stu-id="35b2a-133">-Container</span></span>

<span data-ttu-id="35b2a-134">指定由此 Cmdlet 取得備份專案的容器物件。</span><span class="sxs-lookup"><span data-stu-id="35b2a-134">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="35b2a-135">若要取得 **AzureRmRecoveryServicesBackupContainer** ，請使用 **AzRecoveryServicesBackupContainer** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="35b2a-135">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="35b2a-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35b2a-136">-DefaultProfile</span></span>

<span data-ttu-id="35b2a-137">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="35b2a-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35b2a-138">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="35b2a-138">-DeleteState</span></span>
<span data-ttu-id="35b2a-139">指定專案的 deletestate 此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="35b2a-139">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35b2a-140">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="35b2a-140">ToBeDeleted</span></span>
- <span data-ttu-id="35b2a-141">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="35b2a-141">NotDeleted</span></span>

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

### <span data-ttu-id="35b2a-142">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="35b2a-142">-FriendlyName</span></span>
<span data-ttu-id="35b2a-143">已備份專案的 FriendlyName</span><span class="sxs-lookup"><span data-stu-id="35b2a-143">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="35b2a-144">-名稱</span><span class="sxs-lookup"><span data-stu-id="35b2a-144">-Name</span></span>

<span data-ttu-id="35b2a-145">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="35b2a-145">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="35b2a-146">-原則</span><span class="sxs-lookup"><span data-stu-id="35b2a-146">-Policy</span></span>

<span data-ttu-id="35b2a-147">保護原則物件。</span><span class="sxs-lookup"><span data-stu-id="35b2a-147">Protection policy object.</span></span>

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

### <span data-ttu-id="35b2a-148">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="35b2a-148">-ProtectionState</span></span>

<span data-ttu-id="35b2a-149">指定保護的狀態。</span><span class="sxs-lookup"><span data-stu-id="35b2a-149">Specifies the state of protection.</span></span>
<span data-ttu-id="35b2a-150">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="35b2a-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35b2a-151">IRPending.</span><span class="sxs-lookup"><span data-stu-id="35b2a-151">IRPending.</span></span>
<span data-ttu-id="35b2a-152">初始同步處理尚未開始，而且尚未有任何復原點。</span><span class="sxs-lookup"><span data-stu-id="35b2a-152">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="35b2a-153">受.</span><span class="sxs-lookup"><span data-stu-id="35b2a-153">Protected.</span></span>
<span data-ttu-id="35b2a-154">正在進行保護。</span><span class="sxs-lookup"><span data-stu-id="35b2a-154">Protection is ongoing.</span></span>
- <span data-ttu-id="35b2a-155">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="35b2a-155">ProtectionError.</span></span>
<span data-ttu-id="35b2a-156">出現保護錯誤。</span><span class="sxs-lookup"><span data-stu-id="35b2a-156">There is a protection error.</span></span>
- <span data-ttu-id="35b2a-157">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="35b2a-157">ProtectionStopped.</span></span>
<span data-ttu-id="35b2a-158">已停用保護功能。</span><span class="sxs-lookup"><span data-stu-id="35b2a-158">Protection is disabled.</span></span>

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

### <span data-ttu-id="35b2a-159">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="35b2a-159">-ProtectionStatus</span></span>

<span data-ttu-id="35b2a-160">指定容器中某個專案的整體保護狀態。</span><span class="sxs-lookup"><span data-stu-id="35b2a-160">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="35b2a-161">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="35b2a-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35b2a-162">健全</span><span class="sxs-lookup"><span data-stu-id="35b2a-162">Healthy</span></span>
- <span data-ttu-id="35b2a-163">不</span><span class="sxs-lookup"><span data-stu-id="35b2a-163">Unhealthy</span></span>

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

### <span data-ttu-id="35b2a-164">-VaultId</span><span class="sxs-lookup"><span data-stu-id="35b2a-164">-VaultId</span></span>

<span data-ttu-id="35b2a-165">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="35b2a-165">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="35b2a-166">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="35b2a-166">-WorkloadType</span></span>

<span data-ttu-id="35b2a-167">指定工作負荷類型。</span><span class="sxs-lookup"><span data-stu-id="35b2a-167">Specifies the workload type.</span></span>
<span data-ttu-id="35b2a-168">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="35b2a-168">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="35b2a-169">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="35b2a-169">AzureVM</span></span>
- <span data-ttu-id="35b2a-170">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="35b2a-170">AzureSQLDatabase</span></span>
- <span data-ttu-id="35b2a-171">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="35b2a-171">AzureFiles</span></span>
- <span data-ttu-id="35b2a-172">MSSQL</span><span class="sxs-lookup"><span data-stu-id="35b2a-172">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35b2a-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35b2a-173">CommonParameters</span></span>
<span data-ttu-id="35b2a-174">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="35b2a-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35b2a-175">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="35b2a-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35b2a-176">輸入</span><span class="sxs-lookup"><span data-stu-id="35b2a-176">INPUTS</span></span>

### <span data-ttu-id="35b2a-177">ContainerBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="35b2a-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="35b2a-178">System.object</span><span class="sxs-lookup"><span data-stu-id="35b2a-178">System.String</span></span>

## <span data-ttu-id="35b2a-179">輸出</span><span class="sxs-lookup"><span data-stu-id="35b2a-179">OUTPUTS</span></span>

### <span data-ttu-id="35b2a-180">ItemBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="35b2a-180">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="35b2a-181">筆記</span><span class="sxs-lookup"><span data-stu-id="35b2a-181">NOTES</span></span>

## <span data-ttu-id="35b2a-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="35b2a-182">RELATED LINKS</span></span>

[<span data-ttu-id="35b2a-183">備份-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="35b2a-183">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="35b2a-184">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="35b2a-184">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="35b2a-185">AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="35b2a-185">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="35b2a-186">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="35b2a-186">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
