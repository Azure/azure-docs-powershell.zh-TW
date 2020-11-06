---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 856B76FC-88ED-4A29-9DC6-C482398D702E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/restore-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Restore-AzureRmBackupItem.md
ms.openlocfilehash: a203d125e4ff6d811a581b0713ca4a002e098ade
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453144"
---
# <span data-ttu-id="40c93-101">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="40c93-101">Restore-AzureRmBackupItem</span></span>

## <span data-ttu-id="40c93-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40c93-102">SYNOPSIS</span></span>
<span data-ttu-id="40c93-103">將備份專案的資料和設定還原到復原點。</span><span class="sxs-lookup"><span data-stu-id="40c93-103">Restores the data and configuration for a Backup item to a recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40c93-104">句法</span><span class="sxs-lookup"><span data-stu-id="40c93-104">SYNTAX</span></span>

```
Restore-AzureRmBackupItem [-StorageAccountName] <String> [-RecoveryPoint] <AzureRMBackupRecoveryPoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40c93-105">說明</span><span class="sxs-lookup"><span data-stu-id="40c93-105">DESCRIPTION</span></span>
<span data-ttu-id="40c93-106">**Restore-AzureRmBackupItem** Cmdlet 會將 Azure 備份專案的資料和配置還原至指定的復原點。</span><span class="sxs-lookup"><span data-stu-id="40c93-106">The **Restore-AzureRmBackupItem** cmdlet restores the data and configuration for an Azure Backup item to a specified recovery point.</span></span>
<span data-ttu-id="40c93-107">這個 Cmdlet 會從備份電子倉庫開始還原到您的帳戶。</span><span class="sxs-lookup"><span data-stu-id="40c93-107">This cmdlet starts the restore from the Backup vault to your account.</span></span>

<span data-ttu-id="40c93-108">還原操作不會還原完整的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="40c93-108">The restore operation does not restore the full virtual machine.</span></span>
<span data-ttu-id="40c93-109">它會復原磁碟資料和配置資訊。</span><span class="sxs-lookup"><span data-stu-id="40c93-109">It restores the disk data and configuration information.</span></span>
<span data-ttu-id="40c93-110">還原作業完成後，您必須建立虛擬機器並啟動。</span><span class="sxs-lookup"><span data-stu-id="40c93-110">After the restore operation finished, you must create the virtual machine and start it.</span></span>

## <span data-ttu-id="40c93-111">示例</span><span class="sxs-lookup"><span data-stu-id="40c93-111">EXAMPLES</span></span>

### <span data-ttu-id="40c93-112">範例1：將虛擬機器還原到復原點</span><span class="sxs-lookup"><span data-stu-id="40c93-112">Example 1: Restore a virtual machine to a recovery point</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> $RecoveryPoint = Get-AzureRmBackupRecoveryPoint -Item $BackupItem 
PS C:\> Restore-AzureRmBackupItem -StorageAccountName "DestinationAccount" -RecoveryPoint $RecoveryPoint 
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Restore         InProgress      26-Aug-15 1:14:01 PM   01-Jan-01 12:00:00 AM
```

<span data-ttu-id="40c93-113">第一個命令會使用 Get-AzureRmBackupVault Cmdlet 來取得名為 Vault03 的保存庫。</span><span class="sxs-lookup"><span data-stu-id="40c93-113">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="40c93-114">該命令會將該物件儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="40c93-114">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="40c93-115">第二個命令會在 $Vault 中使用 **AzureRmBackupContainer** Cmdlet，透過電子倉庫中的指定名稱取得容器。</span><span class="sxs-lookup"><span data-stu-id="40c93-115">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="40c93-116">該命令會將該物件儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="40c93-116">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="40c93-117">第三個命令會使用 **AzureRmBackupItem** Cmdlet，在 $Container 中取得容器中的備份專案。</span><span class="sxs-lookup"><span data-stu-id="40c93-117">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="40c93-118">該命令會將該物件儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="40c93-118">The command stores that object in the $BackupItem variable.</span></span>

<span data-ttu-id="40c93-119">第四個命令會針對 $BackupItem 中的專案取得復原點。</span><span class="sxs-lookup"><span data-stu-id="40c93-119">The fourth command gets recovery point for the item in $BackupItem.</span></span>
<span data-ttu-id="40c93-120">該命令會將該物件儲存在 $RecoveryPoint 變數中。</span><span class="sxs-lookup"><span data-stu-id="40c93-120">The command stores that object in the $RecoveryPoint variable.</span></span>

<span data-ttu-id="40c93-121">最後一個命令會針對名為 DestinationAccount 的帳戶還原 $RecoveryPoint 中的復原點。</span><span class="sxs-lookup"><span data-stu-id="40c93-121">The final command restores the recovery point in $RecoveryPoint for the account named DestinationAccount.</span></span>

## <span data-ttu-id="40c93-122">參數</span><span class="sxs-lookup"><span data-stu-id="40c93-122">PARAMETERS</span></span>

### <span data-ttu-id="40c93-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40c93-123">-DefaultProfile</span></span>
<span data-ttu-id="40c93-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="40c93-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40c93-125">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="40c93-125">-RecoveryPoint</span></span>
<span data-ttu-id="40c93-126">指定要還原虛擬機器的復原點。</span><span class="sxs-lookup"><span data-stu-id="40c93-126">Specifies the recovery point to which to restore the virtual machine.</span></span>
<span data-ttu-id="40c93-127">若要取得 **AzureRmBackupRecoveryPoint** ，請使用 Get-AzureRmBackupRecoveryPoint Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40c93-127">To obtain an **AzureRmBackupRecoveryPoint** , use the Get-AzureRmBackupRecoveryPoint cmdlet.</span></span>

```yaml
Type: AzureRMBackupRecoveryPoint
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40c93-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="40c93-128">-StorageAccountName</span></span>
<span data-ttu-id="40c93-129">指定訂閱中目標儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="40c93-129">Specifies the name of the target storage account in your subscription.</span></span>
<span data-ttu-id="40c93-130">在還原程式中，此 Cmdlet 會將磁片與設定資訊儲存在這個儲存空間帳戶中。</span><span class="sxs-lookup"><span data-stu-id="40c93-130">As a part of the restore process, this cmdlet stores the disks and the configuration information in this storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40c93-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40c93-131">CommonParameters</span></span>
<span data-ttu-id="40c93-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40c93-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40c93-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="40c93-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40c93-134">輸入</span><span class="sxs-lookup"><span data-stu-id="40c93-134">INPUTS</span></span>

### <span data-ttu-id="40c93-135">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="40c93-135">AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="40c93-136">輸出</span><span class="sxs-lookup"><span data-stu-id="40c93-136">OUTPUTS</span></span>

### <span data-ttu-id="40c93-137">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="40c93-137">AzureRmBackupJob</span></span>

## <span data-ttu-id="40c93-138">筆記</span><span class="sxs-lookup"><span data-stu-id="40c93-138">NOTES</span></span>

## <span data-ttu-id="40c93-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="40c93-139">RELATED LINKS</span></span>

[<span data-ttu-id="40c93-140">備份-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="40c93-140">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="40c93-141">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="40c93-141">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="40c93-142">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="40c93-142">Get-AzureRmBackupRecoveryPoint</span></span>](./Get-AzureRmBackupRecoveryPoint.md)

