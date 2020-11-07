---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 4c023de04cb431e18dc027c0ca3563aa6a2410e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791945"
---
# <span data-ttu-id="ee802-101">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="ee802-101">Disable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="ee802-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ee802-102">SYNOPSIS</span></span>
<span data-ttu-id="ee802-103">針對受備份保護的專案停用保護。</span><span class="sxs-lookup"><span data-stu-id="ee802-103">Disables protection for a Backup-protected item.</span></span>

## <span data-ttu-id="ee802-104">句法</span><span class="sxs-lookup"><span data-stu-id="ee802-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee802-105">說明</span><span class="sxs-lookup"><span data-stu-id="ee802-105">DESCRIPTION</span></span>
<span data-ttu-id="ee802-106">**Disable AzRecoveryServicesBackupProtection** Cmdlet 會針對 Azure 備份保護的專案停用保護。</span><span class="sxs-lookup"><span data-stu-id="ee802-106">The **Disable-AzRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="ee802-107">這個 Cmdlet 會停止定期排程的專案備份。</span><span class="sxs-lookup"><span data-stu-id="ee802-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="ee802-108">這個 Cmdlet 也可以刪除備份專案的現有復原點。</span><span class="sxs-lookup"><span data-stu-id="ee802-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>
<span data-ttu-id="ee802-109">使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ee802-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ee802-110">示例</span><span class="sxs-lookup"><span data-stu-id="ee802-110">EXAMPLES</span></span>

### <span data-ttu-id="ee802-111">範例1：停用備份保護</span><span class="sxs-lookup"><span data-stu-id="ee802-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="ee802-112">第一個命令會取得備份容器陣列，然後將其儲存在 $Cont 陣列中。</span><span class="sxs-lookup"><span data-stu-id="ee802-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="ee802-113">第二個命令會取得對應至第一個容器專案的備份專案，然後將它儲存在 $PI 變數中。</span><span class="sxs-lookup"><span data-stu-id="ee802-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="ee802-114">上一個命令會針對 $PI 0 中的專案停用備份保護 \[ \] ，但會保留資料。</span><span class="sxs-lookup"><span data-stu-id="ee802-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="ee802-115">參數</span><span class="sxs-lookup"><span data-stu-id="ee802-115">PARAMETERS</span></span>

### <span data-ttu-id="ee802-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee802-116">-DefaultProfile</span></span>
<span data-ttu-id="ee802-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ee802-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee802-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ee802-118">-Force</span></span>
<span data-ttu-id="ee802-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="ee802-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee802-120">-專案</span><span class="sxs-lookup"><span data-stu-id="ee802-120">-Item</span></span>
<span data-ttu-id="ee802-121">指定此 Cmdlet 停用保護的備份專案。</span><span class="sxs-lookup"><span data-stu-id="ee802-121">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="ee802-122">若要取得 **AzureRmRecoveryServicesBackupItem** ，請使用 Get-AzRecoveryServicesBackupItem Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ee802-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee802-123">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="ee802-123">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="ee802-124">表示此 Cmdlet 會刪除現有的復原點。</span><span class="sxs-lookup"><span data-stu-id="ee802-124">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="ee802-125">若要稍後刪除儲存的復原點，請再次執行此 Cmdlet，並指定此參數。</span><span class="sxs-lookup"><span data-stu-id="ee802-125">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee802-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ee802-126">-VaultId</span></span>
<span data-ttu-id="ee802-127">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="ee802-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ee802-128">-確認</span><span class="sxs-lookup"><span data-stu-id="ee802-128">-Confirm</span></span>
<span data-ttu-id="ee802-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ee802-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee802-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee802-130">-WhatIf</span></span>
<span data-ttu-id="ee802-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ee802-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee802-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ee802-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee802-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee802-133">CommonParameters</span></span>
<span data-ttu-id="ee802-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ee802-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee802-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ee802-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee802-136">輸入</span><span class="sxs-lookup"><span data-stu-id="ee802-136">INPUTS</span></span>

### <span data-ttu-id="ee802-137">ItemBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="ee802-137">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="ee802-138">System.object</span><span class="sxs-lookup"><span data-stu-id="ee802-138">System.String</span></span>

## <span data-ttu-id="ee802-139">輸出</span><span class="sxs-lookup"><span data-stu-id="ee802-139">OUTPUTS</span></span>

### <span data-ttu-id="ee802-140">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="ee802-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="ee802-141">筆記</span><span class="sxs-lookup"><span data-stu-id="ee802-141">NOTES</span></span>

## <span data-ttu-id="ee802-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="ee802-142">RELATED LINKS</span></span>

[<span data-ttu-id="ee802-143">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="ee802-143">Enable-AzRecoveryServicesBackupProtection</span></span>](./Enable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="ee802-144">AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ee802-144">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="ee802-145">AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ee802-145">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)


