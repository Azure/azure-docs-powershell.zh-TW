---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/add-Azstorageaccountmanagementpolicyaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountManagementPolicyAction.md
ms.openlocfilehash: ed876765e3b5eb9d306847958772d9205758f5d6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127346"
---
# <span data-ttu-id="72369-101">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="72369-101">Add-AzStorageAccountManagementPolicyAction</span></span>

## <span data-ttu-id="72369-102">摘要</span><span class="sxs-lookup"><span data-stu-id="72369-102">SYNOPSIS</span></span>
<span data-ttu-id="72369-103">在 [輸入 ManagementPolicy] 動作群組物件中新增動作，或使用動作建立 ManagementPolicy 動作群組物件。</span><span class="sxs-lookup"><span data-stu-id="72369-103">Adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span> <span data-ttu-id="72369-104">該物件可以在新的-AzStorageAccountManagementPolicyRule 中使用。</span><span class="sxs-lookup"><span data-stu-id="72369-104">The object can be used in New-AzStorageAccountManagementPolicyRule.</span></span>

## <span data-ttu-id="72369-105">句法</span><span class="sxs-lookup"><span data-stu-id="72369-105">SYNTAX</span></span>

### <span data-ttu-id="72369-106">BaseBlob (預設) </span><span class="sxs-lookup"><span data-stu-id="72369-106">BaseBlob (Default)</span></span>
```
Add-AzStorageAccountManagementPolicyAction -BaseBlobAction <String> -DaysAfterModificationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72369-107">拍攝</span><span class="sxs-lookup"><span data-stu-id="72369-107">Snapshot</span></span>
```
Add-AzStorageAccountManagementPolicyAction -SnapshotAction <String> -DaysAfterCreationGreaterThan <Int32>
 [-InputObject <PSManagementPolicyActionGroup>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72369-108">說明</span><span class="sxs-lookup"><span data-stu-id="72369-108">DESCRIPTION</span></span>
<span data-ttu-id="72369-109">**AzStorageAccountManagementPolicyAction** Cmdlet 會將動作新增至輸入 ManagementPolicy 動作群組物件，或使用動作建立 ManagementPolicy 動作群組物件。</span><span class="sxs-lookup"><span data-stu-id="72369-109">The **Add-AzStorageAccountManagementPolicyAction** cmdlet adds an action to the input ManagementPolicy Action Group object, or creates a ManagementPolicy Action Group object with the action.</span></span>

## <span data-ttu-id="72369-110">示例</span><span class="sxs-lookup"><span data-stu-id="72369-110">EXAMPLES</span></span>

### <span data-ttu-id="72369-111">範例1：建立包含4個動作的 ManagementPolicy 動作群組物件，然後將它新增到管理原則規則並設定為儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="72369-111">Example 1: Creates a ManagementPolicy Action Group object with 4 actions, then add it to a management policy rule and set to a Storage account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action
PS C:\>$action 

BaseBlob.TierToCool.DaysAfterModificationGreaterThan    : 30
BaseBlob.TierToArchive.DaysAfterModificationGreaterThan : 50
BaseBlob.Delete.DaysAfterModificationGreaterThan        : 100
Snapshot.Delete.DaysAfterCreationGreaterThan            : 100

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="72369-112">第一個命令會建立 ManagementPolicy 動作群組物件，下列3個命令會在物件中新增3個動作。</span><span class="sxs-lookup"><span data-stu-id="72369-112">The first command create a ManagementPolicy Action Group object, the following 3 commands add 3 actions to the object.</span></span> <span data-ttu-id="72369-113">然後將它新增到管理原則規則，並設定為儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="72369-113">Then add it to a management policy rule and set to a Storage account.</span></span>

## <span data-ttu-id="72369-114">參數</span><span class="sxs-lookup"><span data-stu-id="72369-114">PARAMETERS</span></span>

### <span data-ttu-id="72369-115">-BaseBlobAction</span><span class="sxs-lookup"><span data-stu-id="72369-115">-BaseBlobAction</span></span>
<span data-ttu-id="72369-116">Baseblob 的管理原則動作。</span><span class="sxs-lookup"><span data-stu-id="72369-116">The management policy action for baseblob.</span></span>

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

### <span data-ttu-id="72369-117">-DaysAfterCreationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="72369-117">-DaysAfterCreationGreaterThan</span></span>
<span data-ttu-id="72369-118">整數值，指出在建立之後的天數。</span><span class="sxs-lookup"><span data-stu-id="72369-118">Integer value indicating the age in days after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Snapshot
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72369-119">-DaysAfterModificationGreaterThan</span><span class="sxs-lookup"><span data-stu-id="72369-119">-DaysAfterModificationGreaterThan</span></span>
<span data-ttu-id="72369-120">整數值，指出上次修改之後的天數。</span><span class="sxs-lookup"><span data-stu-id="72369-120">Integer value indicating the age in days after last modification.</span></span>

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

### <span data-ttu-id="72369-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72369-121">-DefaultProfile</span></span>
<span data-ttu-id="72369-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="72369-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72369-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72369-123">-InputObject</span></span>
<span data-ttu-id="72369-124">如果輸入 ManagementPolicy 動作物件，會將動作設定為輸入動作物件。</span><span class="sxs-lookup"><span data-stu-id="72369-124">If input the ManagementPolicy Action object, will set the action to the input action object.</span></span>
<span data-ttu-id="72369-125">如果沒有輸入，將會建立新的 action 物件。</span><span class="sxs-lookup"><span data-stu-id="72369-125">If not input, will create a new action object.</span></span>

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

### <span data-ttu-id="72369-126">-SnapshotAction</span><span class="sxs-lookup"><span data-stu-id="72369-126">-SnapshotAction</span></span>
<span data-ttu-id="72369-127">[快照] 的管理原則動作。</span><span class="sxs-lookup"><span data-stu-id="72369-127">The management policy action for snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: Snapshot
Aliases:
Accepted values: Delete

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72369-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72369-128">CommonParameters</span></span>
<span data-ttu-id="72369-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="72369-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72369-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="72369-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72369-131">輸入</span><span class="sxs-lookup"><span data-stu-id="72369-131">INPUTS</span></span>

### <span data-ttu-id="72369-132">PSManagementPolicyActionGroup 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="72369-132">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="72369-133">輸出</span><span class="sxs-lookup"><span data-stu-id="72369-133">OUTPUTS</span></span>

### <span data-ttu-id="72369-134">PSManagementPolicyActionGroup 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="72369-134">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup</span></span>

## <span data-ttu-id="72369-135">筆記</span><span class="sxs-lookup"><span data-stu-id="72369-135">NOTES</span></span>

## <span data-ttu-id="72369-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="72369-136">RELATED LINKS</span></span>
