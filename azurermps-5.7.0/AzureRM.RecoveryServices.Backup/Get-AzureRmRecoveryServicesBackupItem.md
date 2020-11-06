---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 9b836a4c4c056699e2c74bcb4d5b373f5bfe170e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446139"
---
# <span data-ttu-id="45288-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="45288-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="45288-102">摘要</span><span class="sxs-lookup"><span data-stu-id="45288-102">SYNOPSIS</span></span>
<span data-ttu-id="45288-103">從 [備份] 中的容器取得專案。</span><span class="sxs-lookup"><span data-stu-id="45288-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45288-104">句法</span><span class="sxs-lookup"><span data-stu-id="45288-104">SYNTAX</span></span>

### <span data-ttu-id="45288-105">GetItemsForContainer (預設) </span><span class="sxs-lookup"><span data-stu-id="45288-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45288-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="45288-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45288-107">說明</span><span class="sxs-lookup"><span data-stu-id="45288-107">DESCRIPTION</span></span>
<span data-ttu-id="45288-108">**AzureRmRecoveryServicesBackupItem** Cmdlet 會取得容器中的專案，或是 Azure 備份中的值，以及專案的保護狀態。</span><span class="sxs-lookup"><span data-stu-id="45288-108">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>

<span data-ttu-id="45288-109">已登錄至 Azure 恢復服務保存庫的容器可以有一或多個可受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="45288-109">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="45288-110">針對 Azure 虛擬機器，虛擬機器容器中只能有一個備份專案。</span><span class="sxs-lookup"><span data-stu-id="45288-110">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>

<span data-ttu-id="45288-111">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45288-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="45288-112">示例</span><span class="sxs-lookup"><span data-stu-id="45288-112">EXAMPLES</span></span>

### <span data-ttu-id="45288-113">範例1：從備份容器取得專案</span><span class="sxs-lookup"><span data-stu-id="45288-113">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="45288-114">第一個命令會取得類型為「Add-azurevm」的容器，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="45288-114">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="45288-115">第二個命令會在 $Container 中取得名為 V2VM 的備份專案，然後將它儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="45288-115">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="45288-116">參數</span><span class="sxs-lookup"><span data-stu-id="45288-116">PARAMETERS</span></span>

### <span data-ttu-id="45288-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="45288-117">-BackupManagementType</span></span>
<span data-ttu-id="45288-118">指定備份管理類型。</span><span class="sxs-lookup"><span data-stu-id="45288-118">Specifies the Backup management type.</span></span>
<span data-ttu-id="45288-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="45288-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="45288-120">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="45288-120">AzureVM</span></span> 
- <span data-ttu-id="45288-121">MARS</span><span class="sxs-lookup"><span data-stu-id="45288-121">MARS</span></span> 
- <span data-ttu-id="45288-122">SCDPM</span><span class="sxs-lookup"><span data-stu-id="45288-122">SCDPM</span></span> 
- <span data-ttu-id="45288-123">AzureBackupServer AzureSQL</span><span class="sxs-lookup"><span data-stu-id="45288-123">AzureBackupServer AzureSQL</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: GetItemsForVault
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45288-124">-容器</span><span class="sxs-lookup"><span data-stu-id="45288-124">-Container</span></span>
<span data-ttu-id="45288-125">指定由此 Cmdlet 取得備份專案的容器物件。</span><span class="sxs-lookup"><span data-stu-id="45288-125">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="45288-126">若要取得 **AzureRmRecoveryServicesBackupContainer** ，請使用 Get-AzureRmRecoveryServicesBackupContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="45288-126">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: ContainerBase
Parameter Sets: GetItemsForContainer
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45288-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45288-127">-DefaultProfile</span></span>
<span data-ttu-id="45288-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="45288-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45288-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="45288-129">-Name</span></span>
<span data-ttu-id="45288-130">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="45288-130">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45288-131">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="45288-131">-ProtectionState</span></span>
<span data-ttu-id="45288-132">指定保護的狀態。</span><span class="sxs-lookup"><span data-stu-id="45288-132">Specifies the state of protection.</span></span>
<span data-ttu-id="45288-133">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="45288-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="45288-134">IRPending.</span><span class="sxs-lookup"><span data-stu-id="45288-134">IRPending.</span></span>
<span data-ttu-id="45288-135">初始同步處理尚未開始，而且尚未有任何復原點。</span><span class="sxs-lookup"><span data-stu-id="45288-135">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="45288-136">受.</span><span class="sxs-lookup"><span data-stu-id="45288-136">Protected.</span></span>
<span data-ttu-id="45288-137">正在進行保護。</span><span class="sxs-lookup"><span data-stu-id="45288-137">Protection is ongoing.</span></span> 
- <span data-ttu-id="45288-138">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="45288-138">ProtectionError.</span></span>
<span data-ttu-id="45288-139">出現保護錯誤。</span><span class="sxs-lookup"><span data-stu-id="45288-139">There is a protection error.</span></span>
- <span data-ttu-id="45288-140">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="45288-140">ProtectionStopped.</span></span>
<span data-ttu-id="45288-141">已停用保護功能。</span><span class="sxs-lookup"><span data-stu-id="45288-141">Protection is disabled.</span></span>

```yaml
Type: ItemProtectionState
Parameter Sets: (All)
Aliases: 
Accepted values: IRPending, ProtectionError, Protected, ProtectionStopped

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45288-142">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="45288-142">-ProtectionStatus</span></span>
<span data-ttu-id="45288-143">指定容器中某個專案的整體保護狀態。</span><span class="sxs-lookup"><span data-stu-id="45288-143">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="45288-144">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="45288-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="45288-145">健全</span><span class="sxs-lookup"><span data-stu-id="45288-145">Healthy</span></span>
- <span data-ttu-id="45288-146">不</span><span class="sxs-lookup"><span data-stu-id="45288-146">Unhealthy</span></span>

```yaml
Type: ItemProtectionStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45288-147">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="45288-147">-WorkloadType</span></span>
<span data-ttu-id="45288-148">指定工作負荷類型。</span><span class="sxs-lookup"><span data-stu-id="45288-148">Specifies the workload type.</span></span> <span data-ttu-id="45288-149">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="45288-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="45288-150">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="45288-150">AzureVM</span></span> 
- <span data-ttu-id="45288-151">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="45288-151">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45288-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45288-152">CommonParameters</span></span>
<span data-ttu-id="45288-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="45288-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45288-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="45288-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45288-155">輸入</span><span class="sxs-lookup"><span data-stu-id="45288-155">INPUTS</span></span>

### <span data-ttu-id="45288-156">所有</span><span class="sxs-lookup"><span data-stu-id="45288-156">None</span></span>
<span data-ttu-id="45288-157">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="45288-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="45288-158">輸出</span><span class="sxs-lookup"><span data-stu-id="45288-158">OUTPUTS</span></span>

### <span data-ttu-id="45288-159">ItemBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="45288-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="45288-160">[System.object]. RecoveryServices [ItemBase] 的 [] （.]）</span><span class="sxs-lookup"><span data-stu-id="45288-160">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase]</span></span>

## <span data-ttu-id="45288-161">筆記</span><span class="sxs-lookup"><span data-stu-id="45288-161">NOTES</span></span>

## <span data-ttu-id="45288-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="45288-162">RELATED LINKS</span></span>

[<span data-ttu-id="45288-163">備份-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="45288-163">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="45288-164">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="45288-164">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="45288-165">AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="45288-165">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="45288-166">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="45288-166">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


