---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: 65bce04c3df14a6b9dc4397d47577d0642746c45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907969"
---
# <span data-ttu-id="cd071-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="cd071-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="cd071-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cd071-102">SYNOPSIS</span></span>
<span data-ttu-id="cd071-103">新增動作至輸入 ManagementPolicy 動作群組物件，或建立包含該動作的 ManagementPolicy 動作群組物件。</span><span class="sxs-lookup"><span data-stu-id="cd071-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="cd071-104">該物件可用於 New-AzStorageAccountManagementPolicyRule。</span><span class="sxs-lookup"><span data-stu-id="cd071-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="cd071-105">語法</span><span class="sxs-lookup"><span data-stu-id="cd071-105">SYNTAX</span></span>

### <span data-ttu-id="cd071-106">BaseBlob (預設) </span><span class="sxs-lookup"><span data-stu-id="cd071-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd071-107">快照</span><span class="sxs-lookup"><span data-stu-id="cd071-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd071-108">BlobVersion</span><span class="sxs-lookup"><span data-stu-id="cd071-108">BlobVersion</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BlobVersionAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd071-109">描述</span><span class="sxs-lookup"><span data-stu-id="cd071-109">DESCRIPTION</span></span>
<span data-ttu-id="cd071-110">**Add-AzStorageAccountManagementPolicyAction** Cmdlet 會新增動作至輸入 ManagementPolicy 動作群組物件，或建立具有該動作的 ManagementPolicy 動作群組物件。</span><span class="sxs-lookup"><span data-stu-id="cd071-110">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="cd071-111">例子</span><span class="sxs-lookup"><span data-stu-id="cd071-111">EXAMPLES</span></span>

### <span data-ttu-id="cd071-112">範例 1：使用 4 個動作建立 ManagementPolicy 動作群組物件，然後將它新增到管理原則規則，並設定為儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="cd071-112">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action
PS C:\>$action 

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 30
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 50
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 100
Snapshot.TierToCool.DaysAfterCreationGreaterThan        : 
Snapshot.TierToArchive.DaysAfterCreationGreaterThan     : 
Snapshot.Delete.DaysAfterCreationGreaterThan            : 100
Version.TierToCool.DaysAfterCreationGreaterThan         : 
Version.TierToArchive.DaysAfterCreationGreaterThan      : 
Version.Delete.DaysAfterCreationGreaterThan             : 

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="cd071-113">第一個命令會建立 ManagementPolicy 動作群組物件，下列 3 個命令會新增 3 個動作至該物件。</span><span class="sxs-lookup"><span data-stu-id="cd071-113">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="cd071-114">然後將它新增到管理原則規則，並設定為儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="cd071-114">Then add it to a management policy rule and set to a Storage account.</span></span>

### <span data-ttu-id="cd071-115">範例 2：在快照和 Blob 版本上建立包含 6 個動作的 ManagementPolicy 動作群組物件，然後將它新增到管理原則規則，並設定為儲存帳戶</span><span class="sxs-lookup"><span data-stu-id="cd071-115">Example 2: Creates a ManagementPolicy Action Group object with 6 actions on snapshot and blob version, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction  -SnapshotAction Delete -daysAfterCreationGreaterThan 40
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -SnapshotAction TierToArchive -daysAfterCreationGreaterThan 50
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -SnapshotAction TierToCool -daysAfterCreationGreaterThan 60
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction Delete -daysAfterCreationGreaterThan 70
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction TierToArchive -daysAfterCreationGreaterThan 80
PS C:\> $action = Add-AzStorageAccountManagementPolicyAction -InputObject $action -BlobVersionAction TierToCool -daysAfterCreationGreaterThan 90
PS C:\> $action

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 
Snapshot.TierToCool.DaysAfterCreationGreaterThan        : 60
Snapshot.TierToArchive.DaysAfterCreationGreaterThan     : 50
Snapshot.Delete.DaysAfterCreationGreaterThan            : 40
Version.TierToCool.DaysAfterCreationGreaterThan         : 90
Version.TierToArchive.DaysAfterCreationGreaterThan      : 80
Version.Delete.DaysAfterCreationGreaterThan             : 70

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="cd071-116">第一個命令會建立 ManagementPolicy 動作群組物件，下列 5 個命令會新增 5 個快照和 Blob 版本的動作至該物件。</span><span class="sxs-lookup"><span data-stu-id="cd071-116">The first command create a ManagementPolicy Action Group object, the following 5 commands add 5 actions on snapshot and blob version to the object.</span></span> <span data-ttu-id="cd071-117">然後將它新增到管理原則規則，並設定為儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="cd071-117">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="cd071-118">參數</span><span class="sxs-lookup"><span data-stu-id="cd071-118">PARAMETERS</span></span>

### <span data-ttu-id="cd071-119">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="cd071-119">-BaseBlobAction</span></span>
<span data-ttu-id="cd071-120">baseblob 的管理原則動作。</span><span class="sxs-lookup"><span data-stu-id="cd071-120">The management policy action for baseblob.</span></span>

```yaml
Type: System.String
Parameter Sets: BaseBlob
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd071-121">-BlobVersionAction</span><span class="sxs-lookup"><span data-stu-id="cd071-121">-BlobVersionAction</span></span>
<span data-ttu-id="cd071-122">Blob 版本的管理政策動作。</span><span class="sxs-lookup"><span data-stu-id="cd071-122">The management policy action for blob version.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobVersion
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd071-123">-DaysAfterCreationGreater方程式</span><span class="sxs-lookup"><span data-stu-id="cd071-123">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="cd071-124">指出建立後天數的整數值。</span><span class="sxs-lookup"><span data-stu-id="cd071-124">Integer value indicating the age in days after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Snapshot, BlobVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd071-125">-DaysAfterModificationGreater方程式</span><span class="sxs-lookup"><span data-stu-id="cd071-125">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="cd071-126">指出上次修改後天數的整數值。</span><span class="sxs-lookup"><span data-stu-id="cd071-126">Integer value indicating the age in days after last modification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: BaseBlob
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd071-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd071-127">-DefaultProfile</span></span>
<span data-ttu-id="cd071-128">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd071-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd071-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd071-129">-InputObject</span></span>
<span data-ttu-id="cd071-130">如果輸入 ManagementPolicy 動作物件，就會將動作設定為輸入動作物件。</span><span class="sxs-lookup"><span data-stu-id="cd071-130">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="cd071-131">如果沒有輸入，將會建立新動作物件。</span><span class="sxs-lookup"><span data-stu-id="cd071-131">If not input, will create a new action object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd071-132">-SnapshotAction</span><span class="sxs-lookup"><span data-stu-id="cd071-132">-SnapshotAction</span></span>
<span data-ttu-id="cd071-133">快照的管理原則動作。</span><span class="sxs-lookup"><span data-stu-id="cd071-133">The management policy action for snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: Snapshot
Aliases:
Accepted values: Delete, TierToArchive, TierToCool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd071-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd071-134">CommonParameters</span></span>
<span data-ttu-id="cd071-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cd071-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd071-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="cd071-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd071-137">輸入</span><span class="sxs-lookup"><span data-stu-id="cd071-137">INPUTS</span></span>

### <span data-ttu-id="cd071-138">Microsoft.Azure.Commands.management.storage.models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="cd071-138">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="cd071-139">輸出</span><span class="sxs-lookup"><span data-stu-id="cd071-139">OUTPUTS</span></span>

### <span data-ttu-id="cd071-140">Microsoft.Azure.Commands.management.storage.models.PSManagementPolicyActionGroup</span><span class="sxs-lookup"><span data-stu-id="cd071-140">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="cd071-141">筆記</span><span class="sxs-lookup"><span data-stu-id="cd071-141">NOTES</span></span>

## <span data-ttu-id="cd071-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd071-142">RELATED LINKS</span></span>
