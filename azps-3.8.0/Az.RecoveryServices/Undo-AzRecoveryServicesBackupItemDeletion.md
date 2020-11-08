---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/undo-azrecoveryservicesbackupitemdeletion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Undo-AzRecoveryServicesBackupItemDeletion.md
ms.openlocfilehash: 80d03117278073b7b80b9c910a5ee4101a9db09a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957553"
---
# <span data-ttu-id="f6c58-101">Undo-AzRecoveryServicesBackupItemDeletion</span><span class="sxs-lookup"><span data-stu-id="f6c58-101">Undo-AzRecoveryServicesBackupItemDeletion</span></span>

## <span data-ttu-id="f6c58-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6c58-102">SYNOPSIS</span></span>
<span data-ttu-id="f6c58-103">Rehydrates 柔刪除的專案</span><span class="sxs-lookup"><span data-stu-id="f6c58-103">Rehydrates a soft-deleted Item</span></span>

## <span data-ttu-id="f6c58-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6c58-104">SYNTAX</span></span>

```
Undo-AzRecoveryServicesBackupItemDeletion [-Item] <ItemBase> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6c58-105">說明</span><span class="sxs-lookup"><span data-stu-id="f6c58-105">DESCRIPTION</span></span>
<span data-ttu-id="f6c58-106">Undo-AzRecoveryServicesBackupItemDeletion Cmdlet 會 rehydrates 柔刪除的專案。</span><span class="sxs-lookup"><span data-stu-id="f6c58-106">The Undo-AzRecoveryServicesBackupItemDeletion cmdlet rehydrates a soft-deleted item.</span></span>
<span data-ttu-id="f6c58-107">使用 Set-AzRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6c58-107">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="f6c58-108">示例</span><span class="sxs-lookup"><span data-stu-id="f6c58-108">EXAMPLES</span></span>

### <span data-ttu-id="f6c58-109">範例1</span><span class="sxs-lookup"><span data-stu-id="f6c58-109">Example 1</span></span>
```powershell
PS C:\> $Cont = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzRecoveryServicesBackupProtection -Item $PI[0] -RemoveRecoveryPoints
PS C:\> $PI = Get-AzRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Undo-AzRecoveryServicesBackupItemDeletion -Item $PI[0]
```

<span data-ttu-id="f6c58-110">第一個命令會取得備份容器陣列，然後將其儲存在 $Cont 陣列中。</span><span class="sxs-lookup"><span data-stu-id="f6c58-110">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>
<span data-ttu-id="f6c58-111">第二個命令會取得對應至第一個容器專案的備份專案，然後將它儲存在 $PI 變數中。</span><span class="sxs-lookup"><span data-stu-id="f6c58-111">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>
<span data-ttu-id="f6c58-112">第三個命令會針對 $PI 0 中的專案停用備份保護 \[ \] ，並將專案置於 softdeleted 狀態。</span><span class="sxs-lookup"><span data-stu-id="f6c58-112">The third command disables Backup protection for the item in $PI\[0\] and puts the item in a softdeleted state.</span></span>
<span data-ttu-id="f6c58-113">第四個命令是 softdeleted 狀態的新專案。</span><span class="sxs-lookup"><span data-stu-id="f6c58-113">The fourth command the new item which is in a softdeleted state.</span></span>
<span data-ttu-id="f6c58-114">Softdeleted VM 的最後一個命令 rehydrates。</span><span class="sxs-lookup"><span data-stu-id="f6c58-114">The last command rehydrates the softdeleted VM.</span></span>

## <span data-ttu-id="f6c58-115">參數</span><span class="sxs-lookup"><span data-stu-id="f6c58-115">PARAMETERS</span></span>

### <span data-ttu-id="f6c58-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6c58-116">-DefaultProfile</span></span>
<span data-ttu-id="f6c58-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6c58-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6c58-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f6c58-118">-Force</span></span>
<span data-ttu-id="f6c58-119">強制停用備份保護 (會防止確認對話方塊) 。</span><span class="sxs-lookup"><span data-stu-id="f6c58-119">Force disables backup protection (prevents confirmation dialog).</span></span>
<span data-ttu-id="f6c58-120">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="f6c58-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="f6c58-121">-專案</span><span class="sxs-lookup"><span data-stu-id="f6c58-121">-Item</span></span>
<span data-ttu-id="f6c58-122">指定此 Cmdlet 停用保護的備份專案。</span><span class="sxs-lookup"><span data-stu-id="f6c58-122">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="f6c58-123">若要取得 AzureRmRecoveryServicesBackupItem，請使用 Get-AzRecoveryServicesBackupItem Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6c58-123">To obtain an AzureRmRecoveryServicesBackupItem , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="f6c58-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="f6c58-124">-VaultId</span></span>
<span data-ttu-id="f6c58-125">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="f6c58-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f6c58-126">-確認</span><span class="sxs-lookup"><span data-stu-id="f6c58-126">-Confirm</span></span>
<span data-ttu-id="f6c58-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f6c58-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6c58-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6c58-128">-WhatIf</span></span>
<span data-ttu-id="f6c58-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f6c58-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6c58-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6c58-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6c58-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6c58-131">CommonParameters</span></span>
<span data-ttu-id="f6c58-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6c58-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6c58-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f6c58-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6c58-134">輸入</span><span class="sxs-lookup"><span data-stu-id="f6c58-134">INPUTS</span></span>

### <span data-ttu-id="f6c58-135">ItemBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="f6c58-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="f6c58-136">System.object</span><span class="sxs-lookup"><span data-stu-id="f6c58-136">System.String</span></span>

## <span data-ttu-id="f6c58-137">輸出</span><span class="sxs-lookup"><span data-stu-id="f6c58-137">OUTPUTS</span></span>

### <span data-ttu-id="f6c58-138">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="f6c58-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="f6c58-139">筆記</span><span class="sxs-lookup"><span data-stu-id="f6c58-139">NOTES</span></span>

## <span data-ttu-id="f6c58-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6c58-140">RELATED LINKS</span></span>

[<span data-ttu-id="f6c58-141">AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f6c58-141">Get-AzRecoveryServicesBackupContainer</span></span>]()

[<span data-ttu-id="f6c58-142">AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="f6c58-142">Get-AzRecoveryServicesBackupItem</span></span>]()
