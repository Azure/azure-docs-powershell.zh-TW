---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
ms.openlocfilehash: 195ef931b942f3dc8a88ede7e3feb31a3b8aa77f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793061"
---
# <span data-ttu-id="eb513-101">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="eb513-101">New-AzStorageAccountManagementPolicyRule</span></span>

## <span data-ttu-id="eb513-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb513-102">SYNOPSIS</span></span>
<span data-ttu-id="eb513-103">建立 ManagementPolicy 規則物件，可在 AzStorageAccountManagementPolicy 中使用。</span><span class="sxs-lookup"><span data-stu-id="eb513-103">Creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="eb513-104">句法</span><span class="sxs-lookup"><span data-stu-id="eb513-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyRule [-Name] <String> [-Disabled] -Action <PSManagementPolicyActionGroup>
 [-Filter <PSManagementPolicyRuleFilter>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb513-105">說明</span><span class="sxs-lookup"><span data-stu-id="eb513-105">DESCRIPTION</span></span>
<span data-ttu-id="eb513-106">**AzStorageAccountManagementPolicyRule** Cmdlet 會建立 ManagementPolicy 規則物件，可在 Set-AzStorageAccountManagementPolicy 中使用。</span><span class="sxs-lookup"><span data-stu-id="eb513-106">The **New-AzStorageAccountManagementPolicyRule** cmdlet creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="eb513-107">示例</span><span class="sxs-lookup"><span data-stu-id="eb513-107">EXAMPLES</span></span>

### <span data-ttu-id="eb513-108">範例1：建立 ManagementPolicy 規則物件，然後設定為儲存空間帳戶</span><span class="sxs-lookup"><span data-stu-id="eb513-108">Example 1: Creates a ManagementPolicy rule object, then set to a Storage Account</span></span>
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

<span data-ttu-id="eb513-109">這個命令會建立 ManagementPolicy 規則物件，其中 [ManagementPolicy] 動作群組物件包含4個動作、ManagementPolicy 規則篩選物件，然後將規則設定為儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="eb513-109">This command create a ManagementPolicy rule object, with a ManagementPolicy action group object contains 4 actions, a ManagementPolicy rule filter object, then set the rule to a Storage Account.</span></span>

## <span data-ttu-id="eb513-110">參數</span><span class="sxs-lookup"><span data-stu-id="eb513-110">PARAMETERS</span></span>

### <span data-ttu-id="eb513-111">-動作</span><span class="sxs-lookup"><span data-stu-id="eb513-111">-Action</span></span>
<span data-ttu-id="eb513-112">定義動作集的物件。</span><span class="sxs-lookup"><span data-stu-id="eb513-112">An object that defines the action set.</span></span>
<span data-ttu-id="eb513-113">使用 Cmdlet 取得物件 Add-AzureStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="eb513-113">Get the Object with cmdlet Add-AzureStorageAccountManagementPolicyAction</span></span>

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

### <span data-ttu-id="eb513-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb513-114">-DefaultProfile</span></span>
<span data-ttu-id="eb513-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb513-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb513-116">-已停用</span><span class="sxs-lookup"><span data-stu-id="eb513-116">-Disabled</span></span>
<span data-ttu-id="eb513-117">如果設定規則，則會停用。</span><span class="sxs-lookup"><span data-stu-id="eb513-117">The rule is disabled if set it.</span></span>

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

### <span data-ttu-id="eb513-118">-篩選</span><span class="sxs-lookup"><span data-stu-id="eb513-118">-Filter</span></span>
<span data-ttu-id="eb513-119">定義篩選集的物件。</span><span class="sxs-lookup"><span data-stu-id="eb513-119">An object that defines the filter set.</span></span>
<span data-ttu-id="eb513-120">使用 Cmdlet 取得物件 New-AzureStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="eb513-120">Get the Object with cmdlet New-AzureStorageAccountManagementPolicyFilter</span></span>

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

### <span data-ttu-id="eb513-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="eb513-121">-Name</span></span>
<span data-ttu-id="eb513-122">規則名稱可以包含字母數位字元的任何組合。</span><span class="sxs-lookup"><span data-stu-id="eb513-122">A rule name can contain any combination of alpha numeric characters.</span></span>
<span data-ttu-id="eb513-123">規則名稱是區分大小寫的。</span><span class="sxs-lookup"><span data-stu-id="eb513-123">Rule name is case-sensitive.</span></span>
<span data-ttu-id="eb513-124">它在原則中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="eb513-124">It must be unique within a policy.</span></span>

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

### <span data-ttu-id="eb513-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb513-125">CommonParameters</span></span>
<span data-ttu-id="eb513-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb513-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb513-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eb513-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb513-128">輸入</span><span class="sxs-lookup"><span data-stu-id="eb513-128">INPUTS</span></span>

### <span data-ttu-id="eb513-129">所有</span><span class="sxs-lookup"><span data-stu-id="eb513-129">None</span></span>

## <span data-ttu-id="eb513-130">輸出</span><span class="sxs-lookup"><span data-stu-id="eb513-130">OUTPUTS</span></span>

### <span data-ttu-id="eb513-131">PSManagementPolicyRule 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="eb513-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span></span>

## <span data-ttu-id="eb513-132">筆記</span><span class="sxs-lookup"><span data-stu-id="eb513-132">NOTES</span></span>

## <span data-ttu-id="eb513-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb513-133">RELATED LINKS</span></span>
