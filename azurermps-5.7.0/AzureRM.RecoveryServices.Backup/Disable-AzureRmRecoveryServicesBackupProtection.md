---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: ECD3F05A-9350-407E-8B48-67443547652F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/disable-azurermrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupProtection.md
ms.openlocfilehash: 7235c70eae1ab7b93340e68bbb705c17b74c3408
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446155"
---
# <span data-ttu-id="9a213-101">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="9a213-101">Disable-AzureRmRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="9a213-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9a213-102">SYNOPSIS</span></span>
<span data-ttu-id="9a213-103">針對受備份保護的專案停用保護。</span><span class="sxs-lookup"><span data-stu-id="9a213-103">Disables protection for a Backup-protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a213-104">句法</span><span class="sxs-lookup"><span data-stu-id="9a213-104">SYNTAX</span></span>

```
Disable-AzureRmRecoveryServicesBackupProtection [-Item] <ItemBase> [-RemoveRecoveryPoints] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a213-105">說明</span><span class="sxs-lookup"><span data-stu-id="9a213-105">DESCRIPTION</span></span>
<span data-ttu-id="9a213-106">**Disable AzureRmRecoveryServicesBackupProtection** Cmdlet 會針對 Azure 備份保護的專案停用保護。</span><span class="sxs-lookup"><span data-stu-id="9a213-106">The **Disable-AzureRmRecoveryServicesBackupProtection** cmdlet disables protection for an Azure Backup-protected item.</span></span>
<span data-ttu-id="9a213-107">這個 Cmdlet 會停止定期排程的專案備份。</span><span class="sxs-lookup"><span data-stu-id="9a213-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="9a213-108">這個 Cmdlet 也可以刪除備份專案的現有復原點。</span><span class="sxs-lookup"><span data-stu-id="9a213-108">This cmdlet can also delete existing recovery points for the backup item.</span></span>

<span data-ttu-id="9a213-109">使用 Set-AzureRmRecoveryServicesVaultContext Cmdlet 來設定 vault 內容，然後再使用目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a213-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="9a213-110">示例</span><span class="sxs-lookup"><span data-stu-id="9a213-110">EXAMPLES</span></span>

### <span data-ttu-id="9a213-111">範例1：停用備份保護</span><span class="sxs-lookup"><span data-stu-id="9a213-111">Example 1: Disable Backup protection</span></span>
```
PS C:\> $Cont = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered 
PS C:\> $PI = Get-AzureRmRecoveryServicesBackupItem -Container $Cont[0] -WorkloadType AzureVM 
PS C:\> Disable-AzureRmRecoveryServicesBackupProtection -Item $PI[0]
```

<span data-ttu-id="9a213-112">第一個命令會取得備份容器陣列，然後將其儲存在 $Cont 陣列中。</span><span class="sxs-lookup"><span data-stu-id="9a213-112">The first command gets an array of backup containers, and then stores it in the $Cont array.</span></span>

<span data-ttu-id="9a213-113">第二個命令會取得對應至第一個容器專案的備份專案，然後將它儲存在 $PI 變數中。</span><span class="sxs-lookup"><span data-stu-id="9a213-113">The second command gets the Backup item corresponding to the first container item, and then stores it in the $PI variable.</span></span>

<span data-ttu-id="9a213-114">上一個命令會針對 $PI 0 中的專案停用備份保護 \[ \] ，但會保留資料。</span><span class="sxs-lookup"><span data-stu-id="9a213-114">The last command disables Backup protection for the item in $PI\[0\], but retains the data.</span></span>

## <span data-ttu-id="9a213-115">參數</span><span class="sxs-lookup"><span data-stu-id="9a213-115">PARAMETERS</span></span>

### <span data-ttu-id="9a213-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a213-116">-DefaultProfile</span></span>
<span data-ttu-id="9a213-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9a213-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a213-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9a213-118">-Force</span></span>
<span data-ttu-id="9a213-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="9a213-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a213-120">-專案</span><span class="sxs-lookup"><span data-stu-id="9a213-120">-Item</span></span>
<span data-ttu-id="9a213-121">指定此 Cmdlet 停用保護的備份專案。</span><span class="sxs-lookup"><span data-stu-id="9a213-121">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="9a213-122">若要取得 **AzureRmRecoveryServicesBackupItem** ，請使用 Get-AzureRmRecoveryServicesBackupItem Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a213-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzureRmRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: ItemBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a213-123">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="9a213-123">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="9a213-124">表示此 Cmdlet 會刪除現有的復原點。</span><span class="sxs-lookup"><span data-stu-id="9a213-124">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="9a213-125">若要稍後刪除儲存的復原點，請再次執行此 Cmdlet，並指定此參數。</span><span class="sxs-lookup"><span data-stu-id="9a213-125">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a213-126">-確認</span><span class="sxs-lookup"><span data-stu-id="9a213-126">-Confirm</span></span>
<span data-ttu-id="9a213-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9a213-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a213-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a213-128">-WhatIf</span></span>
<span data-ttu-id="9a213-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9a213-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a213-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9a213-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a213-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a213-131">CommonParameters</span></span>
<span data-ttu-id="9a213-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9a213-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a213-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9a213-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a213-134">輸入</span><span class="sxs-lookup"><span data-stu-id="9a213-134">INPUTS</span></span>

### <span data-ttu-id="9a213-135">ItemBase</span><span class="sxs-lookup"><span data-stu-id="9a213-135">ItemBase</span></span>
<span data-ttu-id="9a213-136">形參 "Item" 接受管線中 "ItemBase" 類型的值</span><span class="sxs-lookup"><span data-stu-id="9a213-136">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="9a213-137">輸出</span><span class="sxs-lookup"><span data-stu-id="9a213-137">OUTPUTS</span></span>

### <span data-ttu-id="9a213-138">JobBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="9a213-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="9a213-139">筆記</span><span class="sxs-lookup"><span data-stu-id="9a213-139">NOTES</span></span>

## <span data-ttu-id="9a213-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="9a213-140">RELATED LINKS</span></span>

[<span data-ttu-id="9a213-141">Enable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="9a213-141">Enable-AzureRmRecoveryServicesBackupProtection</span></span>](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="9a213-142">AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="9a213-142">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="9a213-143">AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="9a213-143">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)


