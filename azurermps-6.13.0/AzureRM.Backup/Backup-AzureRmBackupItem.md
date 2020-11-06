---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9FF4F649-F50C-4C27-842F-1CD6C5BC7A2B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/backup-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Backup-AzureRmBackupItem.md
ms.openlocfilehash: e87ab3ec04378dc97e144d2b444ee5398ff4f4f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453900"
---
# <span data-ttu-id="385a5-101">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="385a5-101">Backup-AzureRmBackupItem</span></span>

## <span data-ttu-id="385a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="385a5-102">SYNOPSIS</span></span>
<span data-ttu-id="385a5-103">啟動備份專案的備份。</span><span class="sxs-lookup"><span data-stu-id="385a5-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="385a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="385a5-104">SYNTAX</span></span>

```
Backup-AzureRmBackupItem [-Item] <AzureRMBackupItem> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="385a5-105">說明</span><span class="sxs-lookup"><span data-stu-id="385a5-105">DESCRIPTION</span></span>
<span data-ttu-id="385a5-106">**AzureRmBackupItem** Cmdlet 會針對受保護的 Azure 備份專案（未與備份排程關聯）啟動備份。</span><span class="sxs-lookup"><span data-stu-id="385a5-106">The **Backup-AzureRmBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="385a5-107">您可以在啟用保護後立即執行初始備份，或在排程備份失敗後啟動備份。</span><span class="sxs-lookup"><span data-stu-id="385a5-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="385a5-108">如果現有的備份作業正在執行，此 Cmdlet 會失敗。</span><span class="sxs-lookup"><span data-stu-id="385a5-108">If an existing backup job is running, this cmdlet fails.</span></span>

## <span data-ttu-id="385a5-109">示例</span><span class="sxs-lookup"><span data-stu-id="385a5-109">EXAMPLES</span></span>

### <span data-ttu-id="385a5-110">範例1：開始備份虛擬機器</span><span class="sxs-lookup"><span data-stu-id="385a5-110">Example 1: Start to back up a virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container | Backup-AzureRmBackupItem
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
```

<span data-ttu-id="385a5-111">第一個命令會使用 Get-AzureRmBackupVault Cmdlet 來取得名為 Vault03 的保存庫。</span><span class="sxs-lookup"><span data-stu-id="385a5-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="385a5-112">該命令會將該物件儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="385a5-112">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="385a5-113">第二個命令會在 $Vault 中使用 Get-AzureRmBackupContainer Cmdlet，透過電子倉庫中的指定名稱來取得容器。</span><span class="sxs-lookup"><span data-stu-id="385a5-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="385a5-114">該命令會將該物件儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="385a5-114">The command stores that object in the $Container variable.</span></span>
<span data-ttu-id="385a5-115">最後一個命令會使用 Get-AzureRmBackupItem Cmdlet，在 $Container 中取得備份專案。</span><span class="sxs-lookup"><span data-stu-id="385a5-115">The last command gets the backup items in $Container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="385a5-116">命令會使用管線運算子將專案傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="385a5-116">The command passes the items to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="385a5-117">目前的 Cmdlet 會開始備份容器中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="385a5-117">The current cmdlet starts backing up the virtual machine in the container.</span></span>

## <span data-ttu-id="385a5-118">參數</span><span class="sxs-lookup"><span data-stu-id="385a5-118">PARAMETERS</span></span>

### <span data-ttu-id="385a5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="385a5-119">-DefaultProfile</span></span>
<span data-ttu-id="385a5-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="385a5-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="385a5-121">-專案</span><span class="sxs-lookup"><span data-stu-id="385a5-121">-Item</span></span>
<span data-ttu-id="385a5-122">指定此 Cmdlet 啟動備份操作的備份專案。</span><span class="sxs-lookup"><span data-stu-id="385a5-122">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="385a5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="385a5-123">CommonParameters</span></span>
<span data-ttu-id="385a5-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="385a5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="385a5-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="385a5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="385a5-126">輸入</span><span class="sxs-lookup"><span data-stu-id="385a5-126">INPUTS</span></span>

### <span data-ttu-id="385a5-127">AzureRMBackupItem 中的 AzureBackup。</span><span class="sxs-lookup"><span data-stu-id="385a5-127">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem</span></span>
<span data-ttu-id="385a5-128">參數： (ByValue 的專案) </span><span class="sxs-lookup"><span data-stu-id="385a5-128">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="385a5-129">輸出</span><span class="sxs-lookup"><span data-stu-id="385a5-129">OUTPUTS</span></span>

### <span data-ttu-id="385a5-130">AzureRMBackupJob 中的 AzureBackup。</span><span class="sxs-lookup"><span data-stu-id="385a5-130">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="385a5-131">筆記</span><span class="sxs-lookup"><span data-stu-id="385a5-131">NOTES</span></span>

## <span data-ttu-id="385a5-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="385a5-132">RELATED LINKS</span></span>

[<span data-ttu-id="385a5-133">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="385a5-133">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="385a5-134">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="385a5-134">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="385a5-135">Restore-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="385a5-135">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)


