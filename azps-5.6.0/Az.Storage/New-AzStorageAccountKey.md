---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountKey.md
ms.openlocfilehash: 254d9a012bd3539242e560511e23975acb68b4bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915118"
---
# <span data-ttu-id="4f142-101">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4f142-101">New-AzStorageAccountKey</span></span>

## <span data-ttu-id="4f142-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4f142-102">SYNOPSIS</span></span>
<span data-ttu-id="4f142-103">重新產生 Azure 儲存體帳戶的儲存金鑰。</span><span class="sxs-lookup"><span data-stu-id="4f142-103">Regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="4f142-104">語法</span><span class="sxs-lookup"><span data-stu-id="4f142-104">SYNTAX</span></span>

```
New-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f142-105">描述</span><span class="sxs-lookup"><span data-stu-id="4f142-105">DESCRIPTION</span></span>
<span data-ttu-id="4f142-106">**New-AzStorageAccountKey** Cmdlet 會重新產生 Azure 儲存體帳戶的儲存金鑰。</span><span class="sxs-lookup"><span data-stu-id="4f142-106">The **New-AzStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="4f142-107">例子</span><span class="sxs-lookup"><span data-stu-id="4f142-107">EXAMPLES</span></span>

### <span data-ttu-id="4f142-108">範例 1：重新產生儲存金鑰</span><span class="sxs-lookup"><span data-stu-id="4f142-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzStorageAccountKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="4f142-109">此命令會為指定的儲存空間帳戶重新產生儲存金鑰。</span><span class="sxs-lookup"><span data-stu-id="4f142-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="4f142-110">參數</span><span class="sxs-lookup"><span data-stu-id="4f142-110">PARAMETERS</span></span>

### <span data-ttu-id="4f142-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f142-111">-DefaultProfile</span></span>
<span data-ttu-id="4f142-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f142-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f142-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="4f142-113">-KeyName</span></span>
<span data-ttu-id="4f142-114">指定要重新產生哪個金鑰。</span><span class="sxs-lookup"><span data-stu-id="4f142-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="4f142-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="4f142-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4f142-116">鍵1</span><span class="sxs-lookup"><span data-stu-id="4f142-116">key1</span></span>
- <span data-ttu-id="4f142-117">key2</span><span class="sxs-lookup"><span data-stu-id="4f142-117">key2</span></span>
- <span data-ttu-id="4f142-118">kerb1</span><span class="sxs-lookup"><span data-stu-id="4f142-118">kerb1</span></span>
- <span data-ttu-id="4f142-119">kerb2</span><span class="sxs-lookup"><span data-stu-id="4f142-119">kerb2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2, kerb1, kerb2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f142-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="4f142-120">-Name</span></span>
<span data-ttu-id="4f142-121">指定要重新產生儲存金鑰的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="4f142-121">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f142-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f142-122">-ResourceGroupName</span></span>
<span data-ttu-id="4f142-123">指定包含儲存空間帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="4f142-123">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f142-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f142-124">CommonParameters</span></span>
<span data-ttu-id="4f142-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4f142-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f142-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="4f142-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f142-127">輸入</span><span class="sxs-lookup"><span data-stu-id="4f142-127">INPUTS</span></span>

### <span data-ttu-id="4f142-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4f142-128">System.String</span></span>

## <span data-ttu-id="4f142-129">輸出</span><span class="sxs-lookup"><span data-stu-id="4f142-129">OUTPUTS</span></span>

### <span data-ttu-id="4f142-130">Microsoft.Azure.management.storage.models.StorageAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="4f142-130">Microsoft.Azure.Management.Storage.Models.StorageAccountListKeysResult</span></span>

## <span data-ttu-id="4f142-131">筆記</span><span class="sxs-lookup"><span data-stu-id="4f142-131">NOTES</span></span>

## <span data-ttu-id="4f142-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f142-132">RELATED LINKS</span></span>

[<span data-ttu-id="4f142-133">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4f142-133">Get-AzStorageAccountKey</span></span>](./Get-AzStorageAccountKey.md)
