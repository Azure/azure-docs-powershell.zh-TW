---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/get-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: b27d6e8bec4dda2ba87a0b38a9b37a8d4739ae00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128028"
---
# <span data-ttu-id="f1121-101">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f1121-101">Get-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="f1121-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1121-102">SYNOPSIS</span></span>
<span data-ttu-id="f1121-103">取得 Azure 儲存空間帳戶的管理原則。</span><span class="sxs-lookup"><span data-stu-id="f1121-103">Gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="f1121-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1121-104">SYNTAX</span></span>

### <span data-ttu-id="f1121-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="f1121-105">AccountName (Default)</span></span>
```
Get-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1121-106">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="f1121-106">AccountResourceId</span></span>
```
Get-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1121-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f1121-107">AccountObject</span></span>
```
Get-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1121-108">說明</span><span class="sxs-lookup"><span data-stu-id="f1121-108">DESCRIPTION</span></span>
<span data-ttu-id="f1121-109">**AzStorageAccountManagementPolicy** Cmdlet 會取得 Azure 儲存空間帳戶的管理原則。</span><span class="sxs-lookup"><span data-stu-id="f1121-109">The **Get-AzStorageAccountManagementPolicy** cmdlet gets the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="f1121-110">示例</span><span class="sxs-lookup"><span data-stu-id="f1121-110">EXAMPLES</span></span>

### <span data-ttu-id="f1121-111">範例1：取得儲存空間帳戶的管理原則。</span><span class="sxs-lookup"><span data-stu-id="f1121-111">Example 1: Get the management policy of a Storage account.</span></span>
```
PS C:\>Get-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 7:04:05 AM
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

<span data-ttu-id="f1121-112">這個命令會取得儲存空間帳戶的管理原則。</span><span class="sxs-lookup"><span data-stu-id="f1121-112">This command gets the management policy of a Storage account.</span></span>

## <span data-ttu-id="f1121-113">參數</span><span class="sxs-lookup"><span data-stu-id="f1121-113">PARAMETERS</span></span>

### <span data-ttu-id="f1121-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1121-114">-DefaultProfile</span></span>
<span data-ttu-id="f1121-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1121-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1121-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1121-116">-ResourceGroupName</span></span>
<span data-ttu-id="f1121-117">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f1121-117">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1121-118">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f1121-118">-StorageAccount</span></span>
<span data-ttu-id="f1121-119">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="f1121-119">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1121-120">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f1121-120">-StorageAccountName</span></span>
<span data-ttu-id="f1121-121">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f1121-121">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1121-122">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="f1121-122">-StorageAccountResourceId</span></span>
<span data-ttu-id="f1121-123">儲存空間帳戶資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f1121-123">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1121-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1121-124">CommonParameters</span></span>
<span data-ttu-id="f1121-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1121-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1121-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f1121-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1121-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f1121-127">INPUTS</span></span>

### <span data-ttu-id="f1121-128">System.object</span><span class="sxs-lookup"><span data-stu-id="f1121-128">System.String</span></span>

## <span data-ttu-id="f1121-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f1121-129">OUTPUTS</span></span>

### <span data-ttu-id="f1121-130">StorageAccountKey （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="f1121-130">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="f1121-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f1121-131">NOTES</span></span>

## <span data-ttu-id="f1121-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1121-132">RELATED LINKS</span></span>
