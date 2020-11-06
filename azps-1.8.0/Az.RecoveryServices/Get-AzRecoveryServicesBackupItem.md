---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: c861bbe3b422360f58f36cbe859343f7dcc7ed37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93621159"
---
# <span data-ttu-id="7dd98-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="7dd98-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="7dd98-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7dd98-102">SYNOPSIS</span></span>
<span data-ttu-id="7dd98-103">從 [備份] 中的容器取得專案。</span><span class="sxs-lookup"><span data-stu-id="7dd98-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="7dd98-104">句法</span><span class="sxs-lookup"><span data-stu-id="7dd98-104">SYNTAX</span></span>

### <span data-ttu-id="7dd98-105">GetItemsForContainer (預設) </span><span class="sxs-lookup"><span data-stu-id="7dd98-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7dd98-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="7dd98-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7dd98-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="7dd98-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dd98-108">說明</span><span class="sxs-lookup"><span data-stu-id="7dd98-108">DESCRIPTION</span></span>
<span data-ttu-id="7dd98-109">**AzRecoveryServicesBackupItem** Cmdlet 會取得容器中的專案，或是 Azure 備份中的值，以及專案的保護狀態。</span><span class="sxs-lookup"><span data-stu-id="7dd98-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="7dd98-110">已登錄至 Azure 恢復服務保存庫的容器可以有一或多個可受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="7dd98-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="7dd98-111">針對 Azure 虛擬機器，虛擬機器容器中只能有一個備份專案。</span><span class="sxs-lookup"><span data-stu-id="7dd98-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="7dd98-112">使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7dd98-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="7dd98-113">示例</span><span class="sxs-lookup"><span data-stu-id="7dd98-113">EXAMPLES</span></span>

### <span data-ttu-id="7dd98-114">範例1：從備份容器取得專案</span><span class="sxs-lookup"><span data-stu-id="7dd98-114">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="7dd98-115">第一個命令會取得類型為「Add-azurevm」的容器，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="7dd98-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="7dd98-116">第二個命令會在 $Container 中取得名為 V2VM 的備份專案，然後將它儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="7dd98-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="7dd98-117">參數</span><span class="sxs-lookup"><span data-stu-id="7dd98-117">PARAMETERS</span></span>

### <span data-ttu-id="7dd98-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="7dd98-118">-BackupManagementType</span></span>
<span data-ttu-id="7dd98-119">指定備份管理類型。</span><span class="sxs-lookup"><span data-stu-id="7dd98-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="7dd98-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7dd98-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7dd98-121">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="7dd98-121">AzureVM</span></span> 
- <span data-ttu-id="7dd98-122">MARS</span><span class="sxs-lookup"><span data-stu-id="7dd98-122">MARS</span></span> 
- <span data-ttu-id="7dd98-123">SCDPM</span><span class="sxs-lookup"><span data-stu-id="7dd98-123">SCDPM</span></span> 
- <span data-ttu-id="7dd98-124">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="7dd98-124">AzureBackupServer</span></span> 
- <span data-ttu-id="7dd98-125">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="7dd98-125">AzureSQL</span></span>
- <span data-ttu-id="7dd98-126">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="7dd98-126">AzureStorage</span></span>

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

### <span data-ttu-id="7dd98-127">-容器</span><span class="sxs-lookup"><span data-stu-id="7dd98-127">-Container</span></span>
<span data-ttu-id="7dd98-128">指定由此 Cmdlet 取得備份專案的容器物件。</span><span class="sxs-lookup"><span data-stu-id="7dd98-128">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="7dd98-129">若要取得 **AzureRmRecoveryServicesBackupContainer** ，請使用 Get-AzRecoveryServicesBackupContainer Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7dd98-129">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="7dd98-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dd98-130">-DefaultProfile</span></span>
<span data-ttu-id="7dd98-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7dd98-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dd98-132">-名稱</span><span class="sxs-lookup"><span data-stu-id="7dd98-132">-Name</span></span>
<span data-ttu-id="7dd98-133">指定容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="7dd98-133">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="7dd98-134">-原則</span><span class="sxs-lookup"><span data-stu-id="7dd98-134">-Policy</span></span>
<span data-ttu-id="7dd98-135">保護原則物件。</span><span class="sxs-lookup"><span data-stu-id="7dd98-135">Protection policy object.</span></span>

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

### <span data-ttu-id="7dd98-136">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="7dd98-136">-ProtectionState</span></span>
<span data-ttu-id="7dd98-137">指定保護的狀態。</span><span class="sxs-lookup"><span data-stu-id="7dd98-137">Specifies the state of protection.</span></span>
<span data-ttu-id="7dd98-138">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7dd98-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7dd98-139">IRPending.</span><span class="sxs-lookup"><span data-stu-id="7dd98-139">IRPending.</span></span>
<span data-ttu-id="7dd98-140">初始同步處理尚未開始，而且尚未有任何復原點。</span><span class="sxs-lookup"><span data-stu-id="7dd98-140">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="7dd98-141">受.</span><span class="sxs-lookup"><span data-stu-id="7dd98-141">Protected.</span></span>
<span data-ttu-id="7dd98-142">正在進行保護。</span><span class="sxs-lookup"><span data-stu-id="7dd98-142">Protection is ongoing.</span></span> 
- <span data-ttu-id="7dd98-143">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="7dd98-143">ProtectionError.</span></span>
<span data-ttu-id="7dd98-144">出現保護錯誤。</span><span class="sxs-lookup"><span data-stu-id="7dd98-144">There is a protection error.</span></span>
- <span data-ttu-id="7dd98-145">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="7dd98-145">ProtectionStopped.</span></span>
<span data-ttu-id="7dd98-146">已停用保護功能。</span><span class="sxs-lookup"><span data-stu-id="7dd98-146">Protection is disabled.</span></span>

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

### <span data-ttu-id="7dd98-147">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="7dd98-147">-ProtectionStatus</span></span>
<span data-ttu-id="7dd98-148">指定容器中某個專案的整體保護狀態。</span><span class="sxs-lookup"><span data-stu-id="7dd98-148">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="7dd98-149">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7dd98-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7dd98-150">健全</span><span class="sxs-lookup"><span data-stu-id="7dd98-150">Healthy</span></span>
- <span data-ttu-id="7dd98-151">不</span><span class="sxs-lookup"><span data-stu-id="7dd98-151">Unhealthy</span></span>

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

### <span data-ttu-id="7dd98-152">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7dd98-152">-VaultId</span></span>
<span data-ttu-id="7dd98-153">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="7dd98-153">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7dd98-154">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="7dd98-154">-WorkloadType</span></span>
<span data-ttu-id="7dd98-155">指定工作負荷類型。</span><span class="sxs-lookup"><span data-stu-id="7dd98-155">Specifies the workload type.</span></span> <span data-ttu-id="7dd98-156">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7dd98-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7dd98-157">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="7dd98-157">AzureVM</span></span> 
- <span data-ttu-id="7dd98-158">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="7dd98-158">AzureSQLDatabase</span></span>
- <span data-ttu-id="7dd98-159">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="7dd98-159">AzureFiles</span></span>

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

### <span data-ttu-id="7dd98-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dd98-160">CommonParameters</span></span>
<span data-ttu-id="7dd98-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7dd98-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dd98-162">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7dd98-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dd98-163">輸入</span><span class="sxs-lookup"><span data-stu-id="7dd98-163">INPUTS</span></span>

### <span data-ttu-id="7dd98-164">ContainerBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="7dd98-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="7dd98-165">System.object</span><span class="sxs-lookup"><span data-stu-id="7dd98-165">System.String</span></span>

## <span data-ttu-id="7dd98-166">輸出</span><span class="sxs-lookup"><span data-stu-id="7dd98-166">OUTPUTS</span></span>

### <span data-ttu-id="7dd98-167">ItemBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="7dd98-167">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="7dd98-168">筆記</span><span class="sxs-lookup"><span data-stu-id="7dd98-168">NOTES</span></span>

## <span data-ttu-id="7dd98-169">相關連結</span><span class="sxs-lookup"><span data-stu-id="7dd98-169">RELATED LINKS</span></span>

[<span data-ttu-id="7dd98-170">備份-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="7dd98-170">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="7dd98-171">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="7dd98-171">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="7dd98-172">AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="7dd98-172">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="7dd98-173">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="7dd98-173">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)


