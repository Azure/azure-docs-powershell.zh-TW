---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6778E018-B6CC-468A-823E-3DA047EA6B52
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupRecoveryPoint.md
ms.openlocfilehash: 0a5c5f42f7a6f4755335a5b8827fd2d23e096679
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447166"
---
# <span data-ttu-id="236a1-101">Get-AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="236a1-101">Get-AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="236a1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="236a1-102">SYNOPSIS</span></span>
<span data-ttu-id="236a1-103">取得已備份專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="236a1-103">Gets the recovery points for a backed up item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="236a1-104">句法</span><span class="sxs-lookup"><span data-stu-id="236a1-104">SYNTAX</span></span>

```
Get-AzureRmBackupRecoveryPoint [[-RecoveryPointId] <String>] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="236a1-105">說明</span><span class="sxs-lookup"><span data-stu-id="236a1-105">DESCRIPTION</span></span>
<span data-ttu-id="236a1-106">**AzureRmBackupRecoveryPoint** Cmdlet 會取得已備份之 Azure 備份專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="236a1-106">The **Get-AzureRmBackupRecoveryPoint** cmdlet gets the recovery points for a backed up Azure Backup item.</span></span>
<span data-ttu-id="236a1-107">備份專案之後，備份會儲存一或多個復原點。</span><span class="sxs-lookup"><span data-stu-id="236a1-107">After an item has been backed up, Backup stores one or more recovery points.</span></span>

## <span data-ttu-id="236a1-108">示例</span><span class="sxs-lookup"><span data-stu-id="236a1-108">EXAMPLES</span></span>

### <span data-ttu-id="236a1-109">範例1：取得專案的復原點</span><span class="sxs-lookup"><span data-stu-id="236a1-109">Example 1: Get recovery points for an item</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> $BackupItem = Get-AzureRmBackupItem -Container $Container
PS C:\> Get-AzureRmBackupRecoveryPoint -Item $BackupItem
RecoveryPointId    RecoveryPointType  RecoveryPointTime      ContainerName
---------------    -----------------  -----------------      -------------
15273496567119     AppConsistent      26-Aug-15 12:27:38 PM  iaasvmcontainer;conto02-vm;conto0...
```

<span data-ttu-id="236a1-110">第一個命令會使用 Get-AzureRmBackupVault Cmdlet 來取得名為 Vault03 的保存庫。</span><span class="sxs-lookup"><span data-stu-id="236a1-110">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="236a1-111">該命令會將該物件儲存在 $Vault 變數中。</span><span class="sxs-lookup"><span data-stu-id="236a1-111">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="236a1-112">第二個命令會在 $Vault 中使用 **AzureRmBackupContainer** Cmdlet，透過電子倉庫中的指定名稱取得容器。</span><span class="sxs-lookup"><span data-stu-id="236a1-112">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="236a1-113">該命令會將該物件儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="236a1-113">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="236a1-114">第三個命令會使用 **AzureRmBackupItem** Cmdlet，在 $Container 中取得容器中的備份專案。</span><span class="sxs-lookup"><span data-stu-id="236a1-114">The third command gets the backup item in the container in $Container by using the **Get-AzureRmBackupItem** cmdlet.</span></span>
<span data-ttu-id="236a1-115">該命令會將該物件儲存在 $BackupItem 變數中。</span><span class="sxs-lookup"><span data-stu-id="236a1-115">The command stores that object in the $BackupItem variable.</span></span>

<span data-ttu-id="236a1-116">最終命令會在 $BackupItem 中取得專案的復原點。</span><span class="sxs-lookup"><span data-stu-id="236a1-116">The final command gets recovery points for the item in $BackupItem.</span></span>

## <span data-ttu-id="236a1-117">參數</span><span class="sxs-lookup"><span data-stu-id="236a1-117">PARAMETERS</span></span>

### <span data-ttu-id="236a1-118">-專案</span><span class="sxs-lookup"><span data-stu-id="236a1-118">-Item</span></span>
<span data-ttu-id="236a1-119">指定此 Cmdlet 取得復原點的專案。</span><span class="sxs-lookup"><span data-stu-id="236a1-119">Specifies the item for which this cmdlet gets recovery points.</span></span>
<span data-ttu-id="236a1-120">若要取得 **AzureRmBackupItem** ，請使用 Get-AzureRmBackupItem Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="236a1-120">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="236a1-121">-RecoveryPointId</span><span class="sxs-lookup"><span data-stu-id="236a1-121">-RecoveryPointId</span></span>
<span data-ttu-id="236a1-122">指定此 Cmdlet 取得的復原點識別碼。</span><span class="sxs-lookup"><span data-stu-id="236a1-122">Specifies the ID of a recovery point that this cmdlet gets.</span></span>

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

### <span data-ttu-id="236a1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="236a1-123">-DefaultProfile</span></span>
<span data-ttu-id="236a1-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="236a1-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="236a1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="236a1-125">CommonParameters</span></span>
<span data-ttu-id="236a1-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="236a1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="236a1-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="236a1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="236a1-128">輸入</span><span class="sxs-lookup"><span data-stu-id="236a1-128">INPUTS</span></span>

### <span data-ttu-id="236a1-129">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="236a1-129">AzureRmBackupItem</span></span>

## <span data-ttu-id="236a1-130">輸出</span><span class="sxs-lookup"><span data-stu-id="236a1-130">OUTPUTS</span></span>

### <span data-ttu-id="236a1-131">AzureRmBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="236a1-131">AzureRmBackupRecoveryPoint</span></span>

## <span data-ttu-id="236a1-132">筆記</span><span class="sxs-lookup"><span data-stu-id="236a1-132">NOTES</span></span>

## <span data-ttu-id="236a1-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="236a1-133">RELATED LINKS</span></span>

[<span data-ttu-id="236a1-134">AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="236a1-134">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="236a1-135">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="236a1-135">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="236a1-136">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="236a1-136">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


