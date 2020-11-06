---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageAccountKey.md
ms.openlocfilehash: 651fdef0599a9a62de5d4bdfac8fc5e9105bb4dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452012"
---
# <span data-ttu-id="563b8-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="563b8-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="563b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="563b8-102">SYNOPSIS</span></span>
<span data-ttu-id="563b8-103">重新產生 Azure 儲存空間帳戶的儲存金鑰。</span><span class="sxs-lookup"><span data-stu-id="563b8-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="563b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="563b8-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="563b8-105">說明</span><span class="sxs-lookup"><span data-stu-id="563b8-105">DESCRIPTION</span></span>
<span data-ttu-id="563b8-106">**新的-AzureRmStorageAccountKey** Cmdlet 會為 Azure 儲存空間帳戶重新產生儲存空間金鑰。</span><span class="sxs-lookup"><span data-stu-id="563b8-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="563b8-107">示例</span><span class="sxs-lookup"><span data-stu-id="563b8-107">EXAMPLES</span></span>

### <span data-ttu-id="563b8-108">範例1：重新產生儲存金鑰</span><span class="sxs-lookup"><span data-stu-id="563b8-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageAccountKey -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -KeyName "key1"
```

<span data-ttu-id="563b8-109">這個命令會為指定的儲存空間帳戶重新生成儲存空間。</span><span class="sxs-lookup"><span data-stu-id="563b8-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="563b8-110">參數</span><span class="sxs-lookup"><span data-stu-id="563b8-110">PARAMETERS</span></span>

### <span data-ttu-id="563b8-111">-KeyName</span><span class="sxs-lookup"><span data-stu-id="563b8-111">-KeyName</span></span>
<span data-ttu-id="563b8-112">指定要重新產生的金鑰。</span><span class="sxs-lookup"><span data-stu-id="563b8-112">Specifies which key to regenerate.</span></span>
<span data-ttu-id="563b8-113">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="563b8-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="563b8-114">key1</span><span class="sxs-lookup"><span data-stu-id="563b8-114">key1</span></span>
- <span data-ttu-id="563b8-115">key2</span><span class="sxs-lookup"><span data-stu-id="563b8-115">key2</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="563b8-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="563b8-116">-Name</span></span>
<span data-ttu-id="563b8-117">指定要重新產生儲存金鑰的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="563b8-117">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="563b8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="563b8-118">-ResourceGroupName</span></span>
<span data-ttu-id="563b8-119">指定包含儲存空間帳戶之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="563b8-119">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="563b8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="563b8-120">CommonParameters</span></span>
<span data-ttu-id="563b8-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="563b8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="563b8-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="563b8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="563b8-123">輸入</span><span class="sxs-lookup"><span data-stu-id="563b8-123">INPUTS</span></span>

### <span data-ttu-id="563b8-124">所有</span><span class="sxs-lookup"><span data-stu-id="563b8-124">None</span></span>
<span data-ttu-id="563b8-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="563b8-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="563b8-126">輸出</span><span class="sxs-lookup"><span data-stu-id="563b8-126">OUTPUTS</span></span>

## <span data-ttu-id="563b8-127">筆記</span><span class="sxs-lookup"><span data-stu-id="563b8-127">NOTES</span></span>

## <span data-ttu-id="563b8-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="563b8-128">RELATED LINKS</span></span>

[<span data-ttu-id="563b8-129">AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="563b8-129">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)
