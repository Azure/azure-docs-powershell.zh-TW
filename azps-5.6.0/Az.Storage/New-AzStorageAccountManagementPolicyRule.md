---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
ms.openlocfilehash: 73606a2af9ff0c5e948d407dd5da1f21df5d14b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915109"
---
# <span data-ttu-id="33b12-101">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="33b12-101">New-AzStorageAccountManagementPolicyRule</span></span>

## <span data-ttu-id="33b12-102">簡介</span><span class="sxs-lookup"><span data-stu-id="33b12-102">SYNOPSIS</span></span>
<span data-ttu-id="33b12-103">建立 ManagementPolicy 規則物件，可用於 Set-AzStorageAccountManagementPolicy。</span><span class="sxs-lookup"><span data-stu-id="33b12-103">Creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="33b12-104">語法</span><span class="sxs-lookup"><span data-stu-id="33b12-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyRule [-Name] <String> [-Disabled] -Action <PSManagementPolicyActionGroup>
 [-Filter <PSManagementPolicyRuleFilter>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33b12-105">描述</span><span class="sxs-lookup"><span data-stu-id="33b12-105">DESCRIPTION</span></span>
<span data-ttu-id="33b12-106">**New-AzStorageAccountManagementPolicyRule** Cmdlet 會建立 ManagementPolicy 規則物件，可用於 Set-AzStorageAccountManagementPolicy。</span><span class="sxs-lookup"><span data-stu-id="33b12-106">The **New-AzStorageAccountManagementPolicyRule** cmdlet creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="33b12-107">例子</span><span class="sxs-lookup"><span data-stu-id="33b12-107">EXAMPLES</span></span>

### <span data-ttu-id="33b12-108">範例 1：建立 ManagementPolicy 規則物件，然後設定為儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="33b12-108">Example 1: Creates a ManagementPolicy rule object, then set to a Storage Account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2

PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name rule1 -Action $action -Filter $filter
PS C:\>$rule

Enabled    : True
Name       : rule1
Definition : {
                 "Actions":  {
                                 "BaseBlob":  {
                                                  "TierToCool":  {
                                                                     "DaysAfterModificationGreaterThan":  30
                                                                 },
                                                  "TierToArchive":  {
                                                                        "DaysAfterModificationGreaterThan":  50
                                                                    },
                                                  "Delete":  {
                                                                 "DaysAfterModificationGreaterThan":  100
                                                             }
                                              },
                                 "Snapshot":  {
                                                  "Delete":  {
                                                                 "DaysAfterCreationGreaterThan":  100
                                                             }
                                              }
                             },
                 "Filters":  {
                                 "PrefixMatch":  [
                                                     "blobprefix1",
                                                     "blobprefix2"
                                                 ],
                                 "BlobTypes":  [
                                                   "blockBlob"
                                               ]
                             }
             }

PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="33b12-109">此命令會建立 ManagementPolicy 規則物件，其中 ManagementPolicy 動作群組物件包含 4 個動作 ，即 ManagementPolicy 規則篩選物件，然後將規則設定為儲存帳戶。</span><span class="sxs-lookup"><span data-stu-id="33b12-109">This command create a ManagementPolicy rule object, with a ManagementPolicy action group object contains 4 actions, a ManagementPolicy rule filter object, then set the rule to a Storage Account.</span></span>

## <span data-ttu-id="33b12-110">參數</span><span class="sxs-lookup"><span data-stu-id="33b12-110">PARAMETERS</span></span>

### <span data-ttu-id="33b12-111">-動作</span><span class="sxs-lookup"><span data-stu-id="33b12-111">-Action</span></span>
<span data-ttu-id="33b12-112">定義動作集的物件。</span><span class="sxs-lookup"><span data-stu-id="33b12-112">An object that defines the action set.</span></span>
<span data-ttu-id="33b12-113">使用 Cmdlet 取得物件Add-AzureStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="33b12-113">Get the Object with cmdlet Add-AzureStorageAccountManagementPolicyAction</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33b12-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33b12-114">-DefaultProfile</span></span>
<span data-ttu-id="33b12-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="33b12-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33b12-116">-已停用</span><span class="sxs-lookup"><span data-stu-id="33b12-116">-Disabled</span></span>
<span data-ttu-id="33b12-117">如果設定規則，則規則會停用。</span><span class="sxs-lookup"><span data-stu-id="33b12-117">The rule is disabled if set it.</span></span>

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

### <span data-ttu-id="33b12-118">-篩選</span><span class="sxs-lookup"><span data-stu-id="33b12-118">-Filter</span></span>
<span data-ttu-id="33b12-119">定義篩選集的物件。</span><span class="sxs-lookup"><span data-stu-id="33b12-119">An object that defines the filter set.</span></span>
<span data-ttu-id="33b12-120">使用 Cmdlet 取得物件New-AzureStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="33b12-120">Get the Object with cmdlet New-AzureStorageAccountManagementPolicyFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33b12-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="33b12-121">-Name</span></span>
<span data-ttu-id="33b12-122">規則名稱可以包含任何 Alpha 數位字元組合。</span><span class="sxs-lookup"><span data-stu-id="33b12-122">A rule name can contain any combination of alpha numeric characters.</span></span>
<span data-ttu-id="33b12-123">規則名稱會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="33b12-123">Rule name is case-sensitive.</span></span>
<span data-ttu-id="33b12-124">它必須在策略中是唯一的。</span><span class="sxs-lookup"><span data-stu-id="33b12-124">It must be unique within a policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33b12-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33b12-125">CommonParameters</span></span>
<span data-ttu-id="33b12-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="33b12-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33b12-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="33b12-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33b12-128">輸入</span><span class="sxs-lookup"><span data-stu-id="33b12-128">INPUTS</span></span>

### <span data-ttu-id="33b12-129">沒有</span><span class="sxs-lookup"><span data-stu-id="33b12-129">None</span></span>

## <span data-ttu-id="33b12-130">輸出</span><span class="sxs-lookup"><span data-stu-id="33b12-130">OUTPUTS</span></span>

### <span data-ttu-id="33b12-131">Microsoft.Azure.Commands.management.storage.models.PSManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="33b12-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span></span>

## <span data-ttu-id="33b12-132">筆記</span><span class="sxs-lookup"><span data-stu-id="33b12-132">NOTES</span></span>

## <span data-ttu-id="33b12-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="33b12-133">RELATED LINKS</span></span>
