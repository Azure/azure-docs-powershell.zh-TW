---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: add399ca208cdcd1f1b4395523f8df43875ff451
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128847"
---
# <span data-ttu-id="bee45-101">Get-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="bee45-101">Get-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="bee45-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bee45-102">SYNOPSIS</span></span>
<span data-ttu-id="bee45-103">這個命令會在特定的容器內，或跨所有已註冊的容器，檢索所有可保護的專案。</span><span class="sxs-lookup"><span data-stu-id="bee45-103">This command will retrieve all protectable items within a certain container or across all registered containers.</span></span> <span data-ttu-id="bee45-104">它將由應用程式階層的所有元素所組成。</span><span class="sxs-lookup"><span data-stu-id="bee45-104">It will consist of all the elements of the hierarchy of the application.</span></span> <span data-ttu-id="bee45-105">傳回諸如 Instance、AvailabilityGroup 等的存儲和高層實體。</span><span class="sxs-lookup"><span data-stu-id="bee45-105">Returns DBs and their upper tier entities like Instance, AvailabilityGroup etc.</span></span>

## <span data-ttu-id="bee45-106">句法</span><span class="sxs-lookup"><span data-stu-id="bee45-106">SYNTAX</span></span>

### <span data-ttu-id="bee45-107">NoFilterParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bee45-107">NoFilterParamSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bee45-108">FilterParamSet</span><span class="sxs-lookup"><span data-stu-id="bee45-108">FilterParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [[-Container] <ContainerBase>] [-WorkloadType] <WorkloadType>
 [[-ItemType] <ProtectableItemType>] [-Name <String>] [-ServerName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bee45-109">IdParamSet</span><span class="sxs-lookup"><span data-stu-id="bee45-109">IdParamSet</span></span>
```
Get-AzRecoveryServicesBackupProtectableItem [-ParentID] <String> [[-ItemType] <ProtectableItemType>]
 [-Name <String>] [-ServerName <String>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bee45-110">說明</span><span class="sxs-lookup"><span data-stu-id="bee45-110">DESCRIPTION</span></span>
<span data-ttu-id="bee45-111">**AzRecoveryServicesBackupProtectableItem** Cmdlet 會取得容器中可保護的專案清單，以及專案的保護狀態。</span><span class="sxs-lookup"><span data-stu-id="bee45-111">The **Get-AzRecoveryServicesBackupProtectableItem** cmdlet gets the list of protectable items in a container and the protection status of the items.</span></span>
<span data-ttu-id="bee45-112">已登錄至 Azure 恢復服務保存庫的容器可以有一或多個可受保護的專案。</span><span class="sxs-lookup"><span data-stu-id="bee45-112">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>

## <span data-ttu-id="bee45-113">示例</span><span class="sxs-lookup"><span data-stu-id="bee45-113">EXAMPLES</span></span>

### <span data-ttu-id="bee45-114">範例1</span><span class="sxs-lookup"><span data-stu-id="bee45-114">Example 1</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType MSSQL -Status Registered
PS C:\> $Item = Get-AzRecoveryServicesProtectableItem -Container $Container -ItemType "SQLDatabase" -VaultId $vault.ID
```

<span data-ttu-id="bee45-115">第一個命令會取得 MSSQL 類型的容器，然後將它儲存在 $Container 變數中。</span><span class="sxs-lookup"><span data-stu-id="bee45-115">The first command gets the container of type MSSQL, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="bee45-116">第二個命令會在 $Container 中取得備份可保護的專案，然後將其儲存在 $Item 變數中。</span><span class="sxs-lookup"><span data-stu-id="bee45-116">The second command gets the Backup protectable item in $Container, and then stores it in the $Item variable.</span></span>

## <span data-ttu-id="bee45-117">參數</span><span class="sxs-lookup"><span data-stu-id="bee45-117">PARAMETERS</span></span>

### <span data-ttu-id="bee45-118">-容器</span><span class="sxs-lookup"><span data-stu-id="bee45-118">-Container</span></span>
<span data-ttu-id="bee45-119">專案所在的容器</span><span class="sxs-lookup"><span data-stu-id="bee45-119">Container where the item resides</span></span>

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

### <span data-ttu-id="bee45-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bee45-120">-DefaultProfile</span></span>
<span data-ttu-id="bee45-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bee45-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bee45-122">-ItemType</span><span class="sxs-lookup"><span data-stu-id="bee45-122">-ItemType</span></span>
<span data-ttu-id="bee45-123">指定能保護的專案類型。</span><span class="sxs-lookup"><span data-stu-id="bee45-123">Specifies the type of protectable item.</span></span> <span data-ttu-id="bee45-124">適用的值： (SQLDataBase、SQLInstance、SQLAvailabilityGroup) 。</span><span class="sxs-lookup"><span data-stu-id="bee45-124">Applicable values: (SQLDataBase, SQLInstance, SQLAvailabilityGroup).</span></span>

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

### <span data-ttu-id="bee45-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="bee45-125">-Name</span></span>
<span data-ttu-id="bee45-126">指定資料庫、Instance 或 AvailabilityGroup 的名稱。</span><span class="sxs-lookup"><span data-stu-id="bee45-126">Specifies the name of the Database, Instance or AvailabilityGroup.</span></span>

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

### <span data-ttu-id="bee45-127">-ParentID</span><span class="sxs-lookup"><span data-stu-id="bee45-127">-ParentID</span></span>
<span data-ttu-id="bee45-128">已指定實例或 AG 的 ARM 識別碼。</span><span class="sxs-lookup"><span data-stu-id="bee45-128">Specified the ARM ID of an Instance or AG.</span></span>

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

### <span data-ttu-id="bee45-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bee45-129">-ServerName</span></span>
<span data-ttu-id="bee45-130">指定專案所屬之伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="bee45-130">Specifies the name of the server to which the item belongs.</span></span>

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

### <span data-ttu-id="bee45-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="bee45-131">-VaultId</span></span>
<span data-ttu-id="bee45-132">[恢復服務] 保存庫的 ARM ID。</span><span class="sxs-lookup"><span data-stu-id="bee45-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="bee45-133">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="bee45-133">-WorkloadType</span></span>
<span data-ttu-id="bee45-134">資源的工作負荷類型。</span><span class="sxs-lookup"><span data-stu-id="bee45-134">Workload type of the resource.</span></span> <span data-ttu-id="bee45-135">目前支援的值為 Add-azurevm、WindowsServer、AzureFiles、MSSQL</span><span class="sxs-lookup"><span data-stu-id="bee45-135">The current supported values are  AzureVM, WindowsServer, AzureFiles, MSSQL</span></span>

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

### <span data-ttu-id="bee45-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bee45-136">CommonParameters</span></span>
<span data-ttu-id="bee45-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bee45-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bee45-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bee45-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bee45-139">輸入</span><span class="sxs-lookup"><span data-stu-id="bee45-139">INPUTS</span></span>

### <span data-ttu-id="bee45-140">ContainerBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="bee45-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="bee45-141">System.object</span><span class="sxs-lookup"><span data-stu-id="bee45-141">System.String</span></span>

## <span data-ttu-id="bee45-142">輸出</span><span class="sxs-lookup"><span data-stu-id="bee45-142">OUTPUTS</span></span>

### <span data-ttu-id="bee45-143">ProtectableItemBase 中的 RecoveryServices，然後再</span><span class="sxs-lookup"><span data-stu-id="bee45-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase</span></span>

## <span data-ttu-id="bee45-144">筆記</span><span class="sxs-lookup"><span data-stu-id="bee45-144">NOTES</span></span>

## <span data-ttu-id="bee45-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="bee45-145">RELATED LINKS</span></span>
