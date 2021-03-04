---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 1d14a1559d62f00b4a513c6a25dad28b7816e2d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911870"
---
# <span data-ttu-id="5e86a-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="5e86a-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="5e86a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5e86a-102">SYNOPSIS</span></span>
<span data-ttu-id="5e86a-103">此命令會在特定容器內或跨所有已登錄的容器，來取回所有可保護的專案。</span><span class="sxs-lookup"><span data-stu-id="5e86a-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="5e86a-104">它會包含應用程式階層的所有元素。</span><span class="sxs-lookup"><span data-stu-id="5e86a-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="5e86a-105">會返回 DB 及其上層實體，例如 Instance、AvailabilityGroup 等。</span><span class="sxs-lookup"><span data-stu-id="5e86a-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="5e86a-106">語法</span><span class="sxs-lookup"><span data-stu-id="5e86a-106">SYNTAX</span></span>

### <span data-ttu-id="5e86a-107">NoFilterParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5e86a-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e86a-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="5e86a-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e86a-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="5e86a-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e86a-110">描述</span><span class="sxs-lookup"><span data-stu-id="5e86a-110">DESCRIPTION</span></span>
<span data-ttu-id="5e86a-111">**Get-AzRecoveryServicesBackupProtectableItem** Cmdlet 會取得容器中可保護專案的清單，以及專案的保護狀態。</span><span class="sxs-lookup"><span data-stu-id="5e86a-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the list of protectable items in a container and the protection status of the items.</span></span>
<span data-ttu-id="5e86a-112">已註冊至 Azure 修復服務儲存庫的容器可以有一或多個可受到保護的專案。</span><span class="sxs-lookup"><span data-stu-id="5e86a-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="5e86a-113">例子</span><span class="sxs-lookup"><span data-stu-id="5e86a-113">EXAMPLES</span></span>

### <span data-ttu-id="5e86a-114">範例 1</span><span class="sxs-lookup"><span data-stu-id="5e86a-114">Example 1</span></span>
```
PS C:\> $Vault = Get-AzRecoveryServicesVault -Name "MyRecoveryVault"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVMAppContainer -Status Registered -VaultId $Vault.Id
PS C:\> $Item = Get-AzRecoveryServicesBackupProtectableItem -Container $Container -ItemType "SQLInstance" -WorkloadType "MSSQL" -VaultId $Vault.ID
```

<span data-ttu-id="5e86a-115">第一個命令會獲得 MSSQL 類型的容器，然後將它儲存在$Container變數中。</span><span class="sxs-lookup"><span data-stu-id="5e86a-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="5e86a-116">第二個命令會獲得 $Container 備份可保護的專案，然後將它儲存在$Item變數中。</span><span class="sxs-lookup"><span data-stu-id="5e86a-116">The second command gets the Backup protectable item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="5e86a-117">參數</span><span class="sxs-lookup"><span data-stu-id="5e86a-117">PARAMETERS</span></span>

### <span data-ttu-id="5e86a-118">-Container</span><span class="sxs-lookup"><span data-stu-id="5e86a-118">-Container</span></span>
<span data-ttu-id="5e86a-119">專案所在的容器</span><span class="sxs-lookup"><span data-stu-id="5e86a-119">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e86a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e86a-120">-DefaultProfile</span></span>
<span data-ttu-id="5e86a-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5e86a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e86a-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="5e86a-122">-ItemType</span></span>
<span data-ttu-id="5e86a-123">指定可保護專案的類型。</span><span class="sxs-lookup"><span data-stu-id="5e86a-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="5e86a-124">適用值： (SQLDataBase、SQLInstance、SQLAvailabilityGroup) 。</span><span class="sxs-lookup"><span data-stu-id="5e86a-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemType
Parameter Sets: FilterParamSet, IdParamSet
Aliases:
Accepted values: SQLDataBase, SQLInstance, SQLAvailabilityGroup

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e86a-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="5e86a-125">-Name</span></span>
<span data-ttu-id="5e86a-126">指定資料庫、實例或可用性組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5e86a-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e86a-127">-ParentID</span><span class="sxs-lookup"><span data-stu-id="5e86a-127">-ParentID</span></span>
<span data-ttu-id="5e86a-128">指定實例或 AG 的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e86a-128">Specified the ARM ID of an Instance or AG.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e86a-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5e86a-129">-ServerName</span></span>
<span data-ttu-id="5e86a-130">指定專案所屬的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="5e86a-130">Specifies the name of the server to which the item belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: FilterParamSet, IdParamSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e86a-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="5e86a-131">-VaultId</span></span>
<span data-ttu-id="5e86a-132">復原服務庫的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="5e86a-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5e86a-133">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="5e86a-133">-WorkloadType</span></span>
<span data-ttu-id="5e86a-134">資源的工作量類型。</span><span class="sxs-lookup"><span data-stu-id="5e86a-134">Workload type of the resource.</span></span> <span data-ttu-id="5e86a-135">目前支援的值為 Azure 屬性值、WindowsServer 值、AzureFiles 值、MSSQL 值</span><span class="sxs-lookup"><span data-stu-id="5e86a-135">The current supported values are  AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: NoFilterParamSet, FilterParamSet
Aliases:
Accepted values: AzureVM, WindowsServer, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e86a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e86a-136">CommonParameters</span></span>
<span data-ttu-id="5e86a-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5e86a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e86a-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e86a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e86a-139">輸入</span><span class="sxs-lookup"><span data-stu-id="5e86a-139">INPUTS</span></span>

### <span data-ttu-id="5e86a-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="5e86a-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="5e86a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="5e86a-141">System.String</span></span>

## <span data-ttu-id="5e86a-142">輸出</span><span class="sxs-lookup"><span data-stu-id="5e86a-142">OUTPUTS</span></span>

### <span data-ttu-id="5e86a-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.models.ProtectableItemBase</span><span class="sxs-lookup"><span data-stu-id="5e86a-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="5e86a-144">筆記</span><span class="sxs-lookup"><span data-stu-id="5e86a-144">NOTES</span></span>

## <span data-ttu-id="5e86a-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="5e86a-145">RELATED LINKS</span></span>
