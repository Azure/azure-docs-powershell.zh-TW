---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/set-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: 82faf45a348eb1e84fdc0c577c27a4d68fda3894
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958998"
---
# <span data-ttu-id="2dd08-101">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="2dd08-101">Set-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="2dd08-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2dd08-102">SYNOPSIS</span></span>
<span data-ttu-id="2dd08-103">建立或修改 Azure 儲存空間帳戶的管理原則。</span><span class="sxs-lookup"><span data-stu-id="2dd08-103">Creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="2dd08-104">句法</span><span class="sxs-lookup"><span data-stu-id="2dd08-104">SYNTAX</span></span>

### <span data-ttu-id="2dd08-105">AccountNamePolicyRule (預設) </span><span class="sxs-lookup"><span data-stu-id="2dd08-105">AccountNamePolicyRule (Default)</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Rule <PSManagementPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2dd08-106">AccountNamePolicyObject</span><span class="sxs-lookup"><span data-stu-id="2dd08-106">AccountNamePolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Policy <PSManagementPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2dd08-107">AccountObjectPolicyRule</span><span class="sxs-lookup"><span data-stu-id="2dd08-107">AccountObjectPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dd08-108">AccountObjectPolicyObject</span><span class="sxs-lookup"><span data-stu-id="2dd08-108">AccountObjectPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dd08-109">AccountResourceIdPolicyRule</span><span class="sxs-lookup"><span data-stu-id="2dd08-109">AccountResourceIdPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dd08-110">AccountResourceIdPolicyObject</span><span class="sxs-lookup"><span data-stu-id="2dd08-110">AccountResourceIdPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dd08-111">說明</span><span class="sxs-lookup"><span data-stu-id="2dd08-111">DESCRIPTION</span></span>
<span data-ttu-id="2dd08-112">**AzStorageAccountManagementPolicy** Cmdlet 會建立或修改 Azure 儲存空間帳戶的管理原則。</span><span class="sxs-lookup"><span data-stu-id="2dd08-112">The **Set-AzStorageAccountManagementPolicy** cmdlet creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="2dd08-113">示例</span><span class="sxs-lookup"><span data-stu-id="2dd08-113">EXAMPLES</span></span>

### <span data-ttu-id="2dd08-114">範例1：使用 ManagementPolicy 規則物件建立或更新儲存空間帳戶的管理原則。</span><span class="sxs-lookup"><span data-stu-id="2dd08-114">Example 1: Create or update the management policy of a Storage account with ManagementPolicy rule objects.</span></span>
```
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -SnapshotAction Delete -daysAfterCreationGreaterThan 100
PS C:\>$filter1 = New-AzStorageAccountManagementPolicyFilter -PrefixMatch ab,cd 
PS C:\>$rule1 = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action1 -Filter $filter1

PS C:\>$action2 = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$filter2 = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule2 = New-AzStorageAccountManagementPolicyRule -Name Test2 -Action $action2 -Filter $filter2

PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule1,$rule2


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 10:29:29 AM
Rules              : [
                         {
                             "Enabled":  true,
                             "Name":  "Test",
                             "Definition":  {
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
                                                                                    "prefix1",
                                                                                    "prefix2"
                                                                                ],
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         },
                         {
                             "Enabled":  true,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  null,
                                                                                 "TierToArchive":  null,
                                                                                 "Delete":  {
                                                                                                "DaysAfterModificationGreaterThan":  100
                                                                                            }
                                                                             },
                                                                "Snapshot":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="2dd08-115">這個命令會先建立2個 ManagementPolicy 規則物件，然後建立或更新具有2個 ManagementPolicy 規則物件之儲存空間帳戶的管理原則。</span><span class="sxs-lookup"><span data-stu-id="2dd08-115">This command first create 2 ManagementPolicy rule objects, then creates or updates the management policy of a Storage account with the 2 ManagementPolicy rule objects.</span></span>

### <span data-ttu-id="2dd08-116">範例2：使用 Json 格式原則建立或更新儲存帳戶的管理原則。</span><span class="sxs-lookup"><span data-stu-id="2dd08-116">Example 2: Create or update the management policy of a Storage account with a Json format policy.</span></span>
```
PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Policy (@{
    Rules=(@{
        Enabled="true";
        Name="Test";
        Definition=(@{
            Actions=(@{
                BaseBlob=(@{
                    TierToCool=30;
                    TierToArchive=50;
                    Delete=100;
                });
                Snapshot=(@{
                    Delete=100
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob");
                PrefixMatch=@("prefix1","prefix2");
            })
        })
    },
    @{
        Enabled="false";
        Name="Test2";
        Definition=(@{
            Actions=(@{
                BaseBlob=(@{
                    TierToCool=80;
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob");
            })
        })
    })
})


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 10:24:55 AM
Rules              : [
                         {
                             "Enabled":  true,
                             "Name":  "Test",
                             "Definition":  {
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
                                                                                    "prefix1",
                                                                                    "prefix2"
                                                                                ],
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         },
                         {
                             "Enabled":  true,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  {
                                                                                                    "DaysAfterModificationGreaterThan":  80
                                                                                                },
                                                                                 "TierToArchive":  null,
                                                                                 "Delete":  null
                                                                             },
                                                                "Snapshot":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="2dd08-117">這個命令會建立或更新具有 json 格式原則之儲存帳戶的管理原則。</span><span class="sxs-lookup"><span data-stu-id="2dd08-117">This command creates or updates the management policy of a Storage account with a json format policy.</span></span>

### <span data-ttu-id="2dd08-118">範例3：從存儲帳戶取得管理原則，然後將它設定為其他儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="2dd08-118">Example 3: Get the management policy from a Storage account, then set it to another Storage account.</span></span>
```
PS C:\>$outputPolicy = Get-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" | Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup2" -AccountName "mystorageaccount2"
```

<span data-ttu-id="2dd08-119">這個命令首先從儲存帳戶取得管理原則，然後將它設定為其他儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="2dd08-119">This command first gets the management policy from a Storage account, then set it to another Storage account.</span></span>

## <span data-ttu-id="2dd08-120">參數</span><span class="sxs-lookup"><span data-stu-id="2dd08-120">PARAMETERS</span></span>

### <span data-ttu-id="2dd08-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dd08-121">-DefaultProfile</span></span>
<span data-ttu-id="2dd08-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2dd08-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dd08-123">-原則</span><span class="sxs-lookup"><span data-stu-id="2dd08-123">-Policy</span></span>
<span data-ttu-id="2dd08-124">要設定的管理原則物件</span><span class="sxs-lookup"><span data-stu-id="2dd08-124">Management Policy Object to Set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy
Parameter Sets: AccountNamePolicyObject, AccountObjectPolicyObject, AccountResourceIdPolicyObject
Aliases: ManagementPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dd08-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dd08-125">-ResourceGroupName</span></span>
<span data-ttu-id="2dd08-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="2dd08-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNamePolicyRule, AccountNamePolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd08-127">-規則</span><span class="sxs-lookup"><span data-stu-id="2dd08-127">-Rule</span></span>
<span data-ttu-id="2dd08-128">管理原則規則。</span><span class="sxs-lookup"><span data-stu-id="2dd08-128">The Management Policy rules.</span></span> <span data-ttu-id="2dd08-129">使用 New-AzStorageAccountManagementPolicyRule Cmdlet 取得物件。</span><span class="sxs-lookup"><span data-stu-id="2dd08-129">Get the object with New-AzStorageAccountManagementPolicyRule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule[]
Parameter Sets: AccountNamePolicyRule, AccountObjectPolicyRule, AccountResourceIdPolicyRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dd08-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2dd08-130">-StorageAccount</span></span>
<span data-ttu-id="2dd08-131">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="2dd08-131">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObjectPolicyRule, AccountObjectPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dd08-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2dd08-132">-StorageAccountName</span></span>
<span data-ttu-id="2dd08-133">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2dd08-133">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNamePolicyRule, AccountNamePolicyObject
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd08-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="2dd08-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="2dd08-135">儲存空間帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2dd08-135">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceIdPolicyRule, AccountResourceIdPolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dd08-136">-確認</span><span class="sxs-lookup"><span data-stu-id="2dd08-136">-Confirm</span></span>
<span data-ttu-id="2dd08-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2dd08-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd08-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dd08-138">-WhatIf</span></span>
<span data-ttu-id="2dd08-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2dd08-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dd08-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2dd08-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd08-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dd08-141">CommonParameters</span></span>
<span data-ttu-id="2dd08-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2dd08-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dd08-143">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2dd08-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dd08-144">輸入</span><span class="sxs-lookup"><span data-stu-id="2dd08-144">INPUTS</span></span>

### <span data-ttu-id="2dd08-145">System.object</span><span class="sxs-lookup"><span data-stu-id="2dd08-145">System.String</span></span>

## <span data-ttu-id="2dd08-146">輸出</span><span class="sxs-lookup"><span data-stu-id="2dd08-146">OUTPUTS</span></span>

### <span data-ttu-id="2dd08-147">PSManagementPolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="2dd08-147">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy</span></span>

## <span data-ttu-id="2dd08-148">筆記</span><span class="sxs-lookup"><span data-stu-id="2dd08-148">NOTES</span></span>

## <span data-ttu-id="2dd08-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="2dd08-149">RELATED LINKS</span></span>
