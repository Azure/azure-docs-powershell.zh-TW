---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54b28caaf39bd3d4750e341da4f4564d60b59138
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93442443"
---
# <span data-ttu-id="f30fb-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f30fb-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="f30fb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f30fb-102">SYNOPSIS</span></span>
<span data-ttu-id="f30fb-103">建立 Azure 儲存空間資料表的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="f30fb-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="f30fb-104">句法</span><span class="sxs-lookup"><span data-stu-id="f30fb-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="f30fb-105">說明</span><span class="sxs-lookup"><span data-stu-id="f30fb-105">DESCRIPTION</span></span>
<span data-ttu-id="f30fb-106">**新的-AzureStorageTableStoredAccessPolicy** Cmdlet 會為 Azure 儲存空間資料表建立儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="f30fb-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="f30fb-107">示例</span><span class="sxs-lookup"><span data-stu-id="f30fb-107">EXAMPLES</span></span>

### <span data-ttu-id="f30fb-108">範例1：在資料表中建立儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="f30fb-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="f30fb-109">這個命令會在名為 MyTable 的存儲資料表中，建立名為 Policy02 的訪問原則。</span><span class="sxs-lookup"><span data-stu-id="f30fb-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="f30fb-110">參數</span><span class="sxs-lookup"><span data-stu-id="f30fb-110">PARAMETERS</span></span>

### <span data-ttu-id="f30fb-111">-內容</span><span class="sxs-lookup"><span data-stu-id="f30fb-111">-Context</span></span>
<span data-ttu-id="f30fb-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="f30fb-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f30fb-113">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f30fb-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f30fb-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="f30fb-114">-ExpiryTime</span></span>
<span data-ttu-id="f30fb-115">指定儲存的存取原則失效的時間。</span><span class="sxs-lookup"><span data-stu-id="f30fb-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30fb-116">-許可權</span><span class="sxs-lookup"><span data-stu-id="f30fb-116">-Permission</span></span>
<span data-ttu-id="f30fb-117">指定此儲存空間表格的公開存取層級。</span><span class="sxs-lookup"><span data-stu-id="f30fb-117">Specifies the level of public access to this storage table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30fb-118">-原則</span><span class="sxs-lookup"><span data-stu-id="f30fb-118">-Policy</span></span>
<span data-ttu-id="f30fb-119">指定儲存的存取原則，包括此共用存取簽名 (SAS) 權杖的許可權。</span><span class="sxs-lookup"><span data-stu-id="f30fb-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30fb-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="f30fb-120">-StartTime</span></span>
<span data-ttu-id="f30fb-121">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="f30fb-121">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f30fb-122">-資料表</span><span class="sxs-lookup"><span data-stu-id="f30fb-122">-Table</span></span>
<span data-ttu-id="f30fb-123">指定 Azure 儲存空間資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="f30fb-123">Specifies the Azure storage table name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f30fb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f30fb-124">CommonParameters</span></span>
<span data-ttu-id="f30fb-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f30fb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f30fb-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f30fb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f30fb-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f30fb-127">INPUTS</span></span>

## <span data-ttu-id="f30fb-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f30fb-128">OUTPUTS</span></span>

## <span data-ttu-id="f30fb-129">筆記</span><span class="sxs-lookup"><span data-stu-id="f30fb-129">NOTES</span></span>

## <span data-ttu-id="f30fb-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="f30fb-130">RELATED LINKS</span></span>

[<span data-ttu-id="f30fb-131">AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f30fb-131">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="f30fb-132">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="f30fb-132">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="f30fb-133">移除-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f30fb-133">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="f30fb-134">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f30fb-134">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


