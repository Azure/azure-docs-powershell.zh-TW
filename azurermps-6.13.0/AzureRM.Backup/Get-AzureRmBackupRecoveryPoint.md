---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6778E018-B6CC-468A-823E-3DA047EA6B52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackuprecoverypoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
ms.openlocfilehash: f82abc45a9b78093c13764ab0eb28f2593c7fabb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450317"
---
# <span data-ttu-id="f2b5a-101">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="f2b5a-101">Get-AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="f2b5a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b5a-103">取得已備份專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="f2b5a-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2b5a-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2b5a-104">SYNTAX</span></span>

```
Get-AzureRmBackupRecoveryPoint [[-RecoveryPointId] <String>] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2b5a-105">說明</span><span class="sxs-lookup"><span data-stu-id="f2b5a-105">DESCRIPTION</span></span>
<span data-ttu-id="f2b5a-106">**AzureRmBackupRecoveryPoint** Cmdlet 會取得已備份之 Azure 備份專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="f2b5a-106">The **Get-AzureRmBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="f2b5a-107">備份專案之後，備份會儲存一或多個復原點。</span><span class="sxs-lookup"><span data-stu-id="f2b5a-107">After an item has been backed up, Backup stores one or more recovery points.</span></span>

## <span data-ttu-id="f2b5a-108">示例</span><span class="sxs-lookup"><span data-stu-id="f2b5a-108">EXAMPLES</span></span>

### <span data-ttu-id="f2b5a-109">範例1：取得專案的復原點</span><span class="sxs-lookup"><span data-stu-id="f2b5a-109">Example 1: Get recovery points for an item</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> Get-AzureRmBackupRecoveryPoint -Item $BackupItem
RecoveryPointId    RecoveryPointType  RecoveryPointTime      ContainerName
---------------    -----------------  -----------------      -------------
15273496567119     AppConsistent      26-Aug-15 12:27:38 PM  iaasvmcontainer;conto02-vm;conto0...
```

<span data-ttu-id="f2b5a-110">第一個命令會使用 Get-AzureRmBackupVault Cmdlet 來取得名為 Vault03 的保存庫。</span><span class="sxs-lookup"><span data-stu-id="f2b5a-110">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="f2b5a-111">該命令會將該物件儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="f2b5a-111">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="f2b5a-112">第二個命令會在 $Vault 中使用 **AzureRmBackupContainer** Cmdlet，透過電子倉庫中的指定名稱取得容器。</span><span class="sxs-lookup"><span data-stu-id="f2b5a-112">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="f2b5a-113">該命令會將該物件儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="f2b5a-113">The command stores that object in the $Container variable.</span></span>
<span data-ttu-id="f2b5a-114">第三個命令會使用 **AzureRmBackupItem** Cmdlet，在 $Container 中取得容器中的備份專案。</span><span class="sxs-lookup"><span data-stu-id="f2b5a-114">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="f2b5a-115">該命令會將該物件儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="f2b5a-115">The command stores that object in the $BackupItem variable.</span></span>
<span data-ttu-id="f2b5a-116">最終命令會在 $BackupItem 中取得專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="f2b5a-116">The final command gets recovery points for the item in $BackupItem.</span></span>

## <span data-ttu-id="f2b5a-117">參數</span><span class="sxs-lookup"><span data-stu-id="f2b5a-117">PARAMETERS</span></span>

### <span data-ttu-id="f2b5a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2b5a-118">-DefaultProfile</span></span>
<span data-ttu-id="f2b5a-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f2b5a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2b5a-120">-專案</span><span class="sxs-lookup"><span data-stu-id="f2b5a-120">-Item</span></span>
<span data-ttu-id="f2b5a-121">指定此 Cmdlet 取得復原點的專案。</span><span class="sxs-lookup"><span data-stu-id="f2b5a-121">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="f2b5a-122">若要取得 **AzureRmBackupItem** ，請使用 Get-AzureRmBackupItem Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f2b5a-122">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="f2b5a-123">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="f2b5a-123">-RecoveryPointId</span></span>
<span data-ttu-id="f2b5a-124">指定此 Cmdlet 取得的復原點識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2b5a-124">Specifies the ID of a recovery point that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b5a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b5a-125">CommonParameters</span></span>
<span data-ttu-id="f2b5a-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2b5a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b5a-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f2b5a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b5a-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f2b5a-128">INPUTS</span></span>

### <span data-ttu-id="f2b5a-129">AzureRMBackupItem 中的 AzureBackup。</span><span class="sxs-lookup"><span data-stu-id="f2b5a-129">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem</span></span>
<span data-ttu-id="f2b5a-130">參數： (ByValue 的專案) </span><span class="sxs-lookup"><span data-stu-id="f2b5a-130">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="f2b5a-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f2b5a-131">OUTPUTS</span></span>

### <span data-ttu-id="f2b5a-132">AzureRMBackupRecoveryPoint 中的 AzureBackup。</span><span class="sxs-lookup"><span data-stu-id="f2b5a-132">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRecoveryPoint</span></span>

## <span data-ttu-id="f2b5a-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f2b5a-133">NOTES</span></span>

## <span data-ttu-id="f2b5a-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2b5a-134">RELATED LINKS</span></span>

[<span data-ttu-id="f2b5a-135">AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f2b5a-135">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="f2b5a-136">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="f2b5a-136">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="f2b5a-137">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="f2b5a-137">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


