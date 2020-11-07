---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 03da361f8dd68d345782568dc243d4438cad1d77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625980"
---
# <span data-ttu-id="923b8-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="923b8-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="923b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="923b8-102">SYNOPSIS</span></span>
<span data-ttu-id="923b8-103">從 [備份] 中的容器取得專案。</span><span class="sxs-lookup"><span data-stu-id="923b8-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="923b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="923b8-104">SYNTAX</span></span>

### <span data-ttu-id="923b8-105">GetItemsForContainer (預設) </span><span class="sxs-lookup"><span data-stu-id="923b8-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="923b8-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="923b8-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="923b8-107">說明</span><span class="sxs-lookup"><span data-stu-id="923b8-107">DESCRIPTION</span></span>
<span data-ttu-id="923b8-108">**AzureRmRecoveryServicesBackupItem** Cmdlet 會取得容器中的專案，或是 Azure 備份中的值，以及專案的保護狀態。</span><span class="sxs-lookup"><span data-stu-id="923b8-108">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>

<span data-ttu-id="923b8-109">已登錄至 Azure 恢復服務保存庫的容器可以有一或多個可受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="923b8-109">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="923b8-110">針對 Azure 虛擬機器，虛擬機器容器中只能有一個備份專案。</span><span class="sxs-lookup"><span data-stu-id="923b8-110">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>

<span data-ttu-id="923b8-111">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="923b8-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="923b8-112">示例</span><span class="sxs-lookup"><span data-stu-id="923b8-112">EXAMPLES</span></span>

### <span data-ttu-id="923b8-113">範例1：從備份容器取得專案</span><span class="sxs-lookup"><span data-stu-id="923b8-113">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="923b8-114">第一個命令會取得類型為「Add-azurevm」的容器，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="923b8-114">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="923b8-115">第二個命令會在 $Container 中取得名為 V2VM 的備份專案，然後將它儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="923b8-115">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="923b8-116">參數</span><span class="sxs-lookup"><span data-stu-id="923b8-116">PARAMETERS</span></span>

### <span data-ttu-id="923b8-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="923b8-117">-BackupManagementType</span></span>
<span data-ttu-id="923b8-118">指定備份管理類型。</span><span class="sxs-lookup"><span data-stu-id="923b8-118">Specifies the Backup management type.</span></span>
<span data-ttu-id="923b8-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="923b8-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="923b8-120">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="923b8-120">AzureVM</span></span> 
- <span data-ttu-id="923b8-121">MARS</span><span class="sxs-lookup"><span data-stu-id="923b8-121">MARS</span></span> 
- <span data-ttu-id="923b8-122">SCDPM</span><span class="sxs-lookup"><span data-stu-id="923b8-122">SCDPM</span></span> 
- <span data-ttu-id="923b8-123">AzureBackupServer AzureSQL</span><span class="sxs-lookup"><span data-stu-id="923b8-123">AzureBackupServer AzureSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="923b8-124">-容器</span><span class="sxs-lookup"><span data-stu-id="923b8-124">-Container</span></span>
<span data-ttu-id="923b8-125">指定由此 Cmdlet 取得備份專案的容器物件。</span><span class="sxs-lookup"><span data-stu-id="923b8-125">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="923b8-126">若要取得 **AzureRmRecoveryServicesBackupContainer** ，請使用 Get-AzureRmRecoveryServicesBackupContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="923b8-126">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="923b8-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="923b8-127">-Name</span></span>
<span data-ttu-id="923b8-128">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="923b8-128">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="923b8-129">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="923b8-129">-ProtectionState</span></span>
<span data-ttu-id="923b8-130">指定保護的狀態。</span><span class="sxs-lookup"><span data-stu-id="923b8-130">Specifies the state of protection.</span></span>
<span data-ttu-id="923b8-131">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="923b8-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="923b8-132">IRPending.</span><span class="sxs-lookup"><span data-stu-id="923b8-132">IRPending.</span></span>
<span data-ttu-id="923b8-133">初始同步處理尚未開始，而且尚未有任何復原點。</span><span class="sxs-lookup"><span data-stu-id="923b8-133">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="923b8-134">受.</span><span class="sxs-lookup"><span data-stu-id="923b8-134">Protected.</span></span>
<span data-ttu-id="923b8-135">正在進行保護。</span><span class="sxs-lookup"><span data-stu-id="923b8-135">Protection is ongoing.</span></span> 
- <span data-ttu-id="923b8-136">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="923b8-136">ProtectionError.</span></span>
<span data-ttu-id="923b8-137">出現保護錯誤。</span><span class="sxs-lookup"><span data-stu-id="923b8-137">There is a protection error.</span></span>
- <span data-ttu-id="923b8-138">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="923b8-138">ProtectionStopped.</span></span>
<span data-ttu-id="923b8-139">已停用保護功能。</span><span class="sxs-lookup"><span data-stu-id="923b8-139">Protection is disabled.</span></span>

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

### <span data-ttu-id="923b8-140">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="923b8-140">-ProtectionStatus</span></span>
<span data-ttu-id="923b8-141">指定容器中某個專案的整體保護狀態。</span><span class="sxs-lookup"><span data-stu-id="923b8-141">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="923b8-142">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="923b8-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="923b8-143">健全</span><span class="sxs-lookup"><span data-stu-id="923b8-143">Healthy</span></span>
- <span data-ttu-id="923b8-144">不</span><span class="sxs-lookup"><span data-stu-id="923b8-144">Unhealthy</span></span>

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

### <span data-ttu-id="923b8-145">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="923b8-145">-WorkloadType</span></span>
<span data-ttu-id="923b8-146">指定工作負荷類型。</span><span class="sxs-lookup"><span data-stu-id="923b8-146">Specifies the workload type.</span></span> <span data-ttu-id="923b8-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="923b8-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="923b8-148">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="923b8-148">AzureVM</span></span> 
- <span data-ttu-id="923b8-149">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="923b8-149">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="923b8-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="923b8-150">-DefaultProfile</span></span>
<span data-ttu-id="923b8-151">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="923b8-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="923b8-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="923b8-152">CommonParameters</span></span>
<span data-ttu-id="923b8-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="923b8-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="923b8-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="923b8-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="923b8-155">輸入</span><span class="sxs-lookup"><span data-stu-id="923b8-155">INPUTS</span></span>

## <span data-ttu-id="923b8-156">輸出</span><span class="sxs-lookup"><span data-stu-id="923b8-156">OUTPUTS</span></span>

### <span data-ttu-id="923b8-157">ItemBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="923b8-157">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="923b8-158">[System.object]. RecoveryServices [ItemBase] 的 [] （.]）</span><span class="sxs-lookup"><span data-stu-id="923b8-158">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase]</span></span>

## <span data-ttu-id="923b8-159">筆記</span><span class="sxs-lookup"><span data-stu-id="923b8-159">NOTES</span></span>

## <span data-ttu-id="923b8-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="923b8-160">RELATED LINKS</span></span>

[<span data-ttu-id="923b8-161">備份-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="923b8-161">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="923b8-162">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="923b8-162">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="923b8-163">AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="923b8-163">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="923b8-164">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="923b8-164">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


