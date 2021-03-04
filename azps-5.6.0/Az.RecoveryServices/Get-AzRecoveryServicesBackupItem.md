---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 084f18e1091059680e0c59b234b295120049cef6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909985"
---
# <span data-ttu-id="03a53-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="03a53-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="03a53-102">簡介</span><span class="sxs-lookup"><span data-stu-id="03a53-102">SYNOPSIS</span></span>

<span data-ttu-id="03a53-103">從備份中的容器獲得專案。</span><span class="sxs-lookup"><span data-stu-id="03a53-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="03a53-104">語法</span><span class="sxs-lookup"><span data-stu-id="03a53-104">SYNTAX</span></span>

### <span data-ttu-id="03a53-105">GetItemsForContainer (預設) </span><span class="sxs-lookup"><span data-stu-id="03a53-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>]  [-UseSecondaryRegion] [<CommonParameters>]
```

### <span data-ttu-id="03a53-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="03a53-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>]  [-UseSecondaryRegion] [<CommonParameters>]
```

### <span data-ttu-id="03a53-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="03a53-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>]  [-UseSecondaryRegion] [<CommonParameters>]
```

## <span data-ttu-id="03a53-108">描述</span><span class="sxs-lookup"><span data-stu-id="03a53-108">DESCRIPTION</span></span>

<span data-ttu-id="03a53-109">**Get-AzRecoveryServicesBackupItem** Cmdlet 會取得容器中受保護的專案清單，以及專案的保護狀態。</span><span class="sxs-lookup"><span data-stu-id="03a53-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the list of protected items in a container and the protection status of the items.</span></span>
<span data-ttu-id="03a53-110">已註冊至 Azure 修復服務儲存庫的容器可以有一或多個可受到保護的專案。</span><span class="sxs-lookup"><span data-stu-id="03a53-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="03a53-111">對於 Azure 虛擬機器，虛擬機器容器中只能有一個備份專案。</span><span class="sxs-lookup"><span data-stu-id="03a53-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="03a53-112">使用 -VaultId 參數設定庫上下文。</span><span class="sxs-lookup"><span data-stu-id="03a53-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="03a53-113">例子</span><span class="sxs-lookup"><span data-stu-id="03a53-113">EXAMPLES</span></span>

### <span data-ttu-id="03a53-114">範例 1：從備份容器取得專案</span><span class="sxs-lookup"><span data-stu-id="03a53-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -FriendlyName "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="03a53-115">第一個命令會獲得 AzureMS 類型的容器，然後將它儲存在$Container變數中。</span><span class="sxs-lookup"><span data-stu-id="03a53-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="03a53-116">第二個命令會于 $Container 中，獲得名為 V2 VM 的備份專案，然後將它儲存在$BackupItem變數中。</span><span class="sxs-lookup"><span data-stu-id="03a53-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="03a53-117">範例 2：從 FriendlyName 取得 Azure 檔案共用專案</span><span class="sxs-lookup"><span data-stu-id="03a53-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -FriendlyName "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="03a53-118">第一個命令會獲得 AzureStorage 類型的容器，然後將它儲存在$Container變數。</span><span class="sxs-lookup"><span data-stu-id="03a53-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="03a53-119">第二個命令會獲得 Backup 專案，其 friendlyName 會符合 FriendlyName Parameter 中傳遞的值，然後將它儲存在$BackupItem變數中。</span><span class="sxs-lookup"><span data-stu-id="03a53-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="03a53-120">使用 FriendlyName 參數可能會導致返回多個 Azure 檔案共用。</span><span class="sxs-lookup"><span data-stu-id="03a53-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="03a53-121">在這種情況下，請傳遞 -Name 參數的值做為傳回結果集的 Name 屬性來執行 Cmdlet $BackupItem。</span><span class="sxs-lookup"><span data-stu-id="03a53-121">In such cases, execute the cmdlet by passing value for -Name parameter as the Name property returned in the result set of $BackupItem.</span></span>

## <span data-ttu-id="03a53-122">參數</span><span class="sxs-lookup"><span data-stu-id="03a53-122">PARAMETERS</span></span>

### <span data-ttu-id="03a53-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="03a53-123">-BackupManagementType</span></span>

<span data-ttu-id="03a53-124">受保護的資源類別。</span><span class="sxs-lookup"><span data-stu-id="03a53-124">The class of resources being protected.</span></span> <span data-ttu-id="03a53-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="03a53-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="03a53-126">AzureAZM</span><span class="sxs-lookup"><span data-stu-id="03a53-126">AzureVM</span></span>
- <span data-ttu-id="03a53-127">MAB</span><span class="sxs-lookup"><span data-stu-id="03a53-127">MAB</span></span>
- <span data-ttu-id="03a53-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="03a53-128">AzureStorage</span></span>
- <span data-ttu-id="03a53-129">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="03a53-129">AzureWorkload</span></span>

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

### <span data-ttu-id="03a53-130">-Container</span><span class="sxs-lookup"><span data-stu-id="03a53-130">-Container</span></span>

<span data-ttu-id="03a53-131">指定此 Cmdlet 會從其中獲得備份專案的容器物件。</span><span class="sxs-lookup"><span data-stu-id="03a53-131">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="03a53-132">若要取得 **AzureRmRecoveryServicesBackupContainer，** 請使用 **Get-AzRecoveryServicesBackupContainer** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03a53-132">To obtain an **AzureRmRecoveryServicesBackupContainer**, use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="03a53-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03a53-133">-DefaultProfile</span></span>

<span data-ttu-id="03a53-134">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="03a53-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03a53-135">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="03a53-135">-DeleteState</span></span>
<span data-ttu-id="03a53-136">指定專案的刪除狀態 此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="03a53-136">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="03a53-137">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="03a53-137">ToBeDeleted</span></span>
- <span data-ttu-id="03a53-138">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="03a53-138">NotDeleted</span></span>

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

### <span data-ttu-id="03a53-139">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="03a53-139">-FriendlyName</span></span>
<span data-ttu-id="03a53-140">備份專案的 FriendlyName</span><span class="sxs-lookup"><span data-stu-id="03a53-140">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="03a53-141">-名稱</span><span class="sxs-lookup"><span data-stu-id="03a53-141">-Name</span></span>

<span data-ttu-id="03a53-142">指定備份專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="03a53-142">Specifies the name of backup item.</span></span> <span data-ttu-id="03a53-143">針對檔案共用，請指定受保護的檔案共用的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="03a53-143">For file share, specify the unique ID of protected file share.</span></span>

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

### <span data-ttu-id="03a53-144">-策略</span><span class="sxs-lookup"><span data-stu-id="03a53-144">-Policy</span></span>

<span data-ttu-id="03a53-145">保護原則物件。</span><span class="sxs-lookup"><span data-stu-id="03a53-145">Protection policy object.</span></span>

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

### <span data-ttu-id="03a53-146">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="03a53-146">-ProtectionState</span></span>

<span data-ttu-id="03a53-147">指定保護狀態。</span><span class="sxs-lookup"><span data-stu-id="03a53-147">Specifies the state of protection.</span></span>
<span data-ttu-id="03a53-148">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="03a53-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="03a53-149">IRPending.</span><span class="sxs-lookup"><span data-stu-id="03a53-149">IRPending.</span></span>
<span data-ttu-id="03a53-150">初始同步處理尚未啟動，而且還沒有修復點。</span><span class="sxs-lookup"><span data-stu-id="03a53-150">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="03a53-151">保護。</span><span class="sxs-lookup"><span data-stu-id="03a53-151">Protected.</span></span>
<span data-ttu-id="03a53-152">保護正在進行中。</span><span class="sxs-lookup"><span data-stu-id="03a53-152">Protection is ongoing.</span></span>
- <span data-ttu-id="03a53-153">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="03a53-153">ProtectionError.</span></span>
<span data-ttu-id="03a53-154">發生保護錯誤。</span><span class="sxs-lookup"><span data-stu-id="03a53-154">There is a protection error.</span></span>
- <span data-ttu-id="03a53-155">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="03a53-155">ProtectionStopped.</span></span>
<span data-ttu-id="03a53-156">保護已停用。</span><span class="sxs-lookup"><span data-stu-id="03a53-156">Protection is disabled.</span></span>

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

### <span data-ttu-id="03a53-157">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="03a53-157">-ProtectionStatus</span></span>

<span data-ttu-id="03a53-158">指定容器內專案的整體保護狀態。</span><span class="sxs-lookup"><span data-stu-id="03a53-158">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="03a53-159">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="03a53-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="03a53-160">健康</span><span class="sxs-lookup"><span data-stu-id="03a53-160">Healthy</span></span>
- <span data-ttu-id="03a53-161">不良</span><span class="sxs-lookup"><span data-stu-id="03a53-161">Unhealthy</span></span>

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

### <span data-ttu-id="03a53-162">-VaultId</span><span class="sxs-lookup"><span data-stu-id="03a53-162">-VaultId</span></span>

<span data-ttu-id="03a53-163">復原服務庫的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="03a53-163">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="03a53-164">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="03a53-164">-WorkloadType</span></span>

<span data-ttu-id="03a53-165">資源的工作量類型。</span><span class="sxs-lookup"><span data-stu-id="03a53-165">Workload type of the resource.</span></span> <span data-ttu-id="03a53-166">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="03a53-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="03a53-167">AzureAZM</span><span class="sxs-lookup"><span data-stu-id="03a53-167">AzureVM</span></span>
- <span data-ttu-id="03a53-168">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="03a53-168">AzureFiles</span></span>
- <span data-ttu-id="03a53-169">MSSQL</span><span class="sxs-lookup"><span data-stu-id="03a53-169">MSSQL</span></span>

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

### <span data-ttu-id="03a53-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03a53-170">CommonParameters</span></span>
<span data-ttu-id="03a53-171">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="03a53-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03a53-172">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03a53-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03a53-173">輸入</span><span class="sxs-lookup"><span data-stu-id="03a53-173">INPUTS</span></span>

### <span data-ttu-id="03a53-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="03a53-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="03a53-175">System.String</span><span class="sxs-lookup"><span data-stu-id="03a53-175">System.String</span></span>

## <span data-ttu-id="03a53-176">輸出</span><span class="sxs-lookup"><span data-stu-id="03a53-176">OUTPUTS</span></span>

### <span data-ttu-id="03a53-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="03a53-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="03a53-178">筆記</span><span class="sxs-lookup"><span data-stu-id="03a53-178">NOTES</span></span>

## <span data-ttu-id="03a53-179">相關連結</span><span class="sxs-lookup"><span data-stu-id="03a53-179">RELATED LINKS</span></span>

[<span data-ttu-id="03a53-180">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="03a53-180">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="03a53-181">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="03a53-181">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="03a53-182">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="03a53-182">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="03a53-183">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="03a53-183">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
