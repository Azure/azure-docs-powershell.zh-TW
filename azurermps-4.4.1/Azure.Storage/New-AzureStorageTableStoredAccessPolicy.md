---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: b87dd24c78b835e16ab1c4e8e9c0c3bb265d4feb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457355"
---
# <span data-ttu-id="a278d-101">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a278d-101">New-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="a278d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a278d-102">SYNOPSIS</span></span>
<span data-ttu-id="a278d-103">建立 Azure 儲存空間資料表的儲存存取原則。</span><span class="sxs-lookup"><span data-stu-id="a278d-103">Creates a stored access policy for an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a278d-104">句法</span><span class="sxs-lookup"><span data-stu-id="a278d-104">SYNTAX</span></span>

```
New-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="a278d-105">說明</span><span class="sxs-lookup"><span data-stu-id="a278d-105">DESCRIPTION</span></span>
<span data-ttu-id="a278d-106">**新的-AzureStorageTableStoredAccessPolicy** Cmdlet 會為 Azure 儲存空間資料表建立儲存的存取原則。</span><span class="sxs-lookup"><span data-stu-id="a278d-106">The **New-AzureStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="a278d-107">示例</span><span class="sxs-lookup"><span data-stu-id="a278d-107">EXAMPLES</span></span>

### <span data-ttu-id="a278d-108">範例1：在資料表中建立儲存的存取原則</span><span class="sxs-lookup"><span data-stu-id="a278d-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="a278d-109">這個命令會在名為 MyTable 的存儲資料表中，建立名為 Policy02 的訪問原則。</span><span class="sxs-lookup"><span data-stu-id="a278d-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="a278d-110">參數</span><span class="sxs-lookup"><span data-stu-id="a278d-110">PARAMETERS</span></span>

### <span data-ttu-id="a278d-111">-內容</span><span class="sxs-lookup"><span data-stu-id="a278d-111">-Context</span></span>
<span data-ttu-id="a278d-112">指定 Azure 儲存區內容。</span><span class="sxs-lookup"><span data-stu-id="a278d-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a278d-113">若要取得儲存內容，請使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a278d-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a278d-114">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a278d-114">-ExpiryTime</span></span>
<span data-ttu-id="a278d-115">指定儲存的存取原則失效的時間。</span><span class="sxs-lookup"><span data-stu-id="a278d-115">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="a278d-116">-許可權</span><span class="sxs-lookup"><span data-stu-id="a278d-116">-Permission</span></span>
<span data-ttu-id="a278d-117">指定儲存的存取原則中的許可權來存取儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="a278d-117">Specifies permissions in the stored access policy to access the storage table.</span></span>

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

### <span data-ttu-id="a278d-118">-原則</span><span class="sxs-lookup"><span data-stu-id="a278d-118">-Policy</span></span>
<span data-ttu-id="a278d-119">指定儲存的存取原則的名稱。</span><span class="sxs-lookup"><span data-stu-id="a278d-119">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="a278d-120">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a278d-120">-StartTime</span></span>
<span data-ttu-id="a278d-121">指定儲存的存取原則生效的時間。</span><span class="sxs-lookup"><span data-stu-id="a278d-121">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="a278d-122">-資料表</span><span class="sxs-lookup"><span data-stu-id="a278d-122">-Table</span></span>
<span data-ttu-id="a278d-123">指定 Azure 儲存空間資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="a278d-123">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="a278d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a278d-124">CommonParameters</span></span>
<span data-ttu-id="a278d-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a278d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a278d-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a278d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a278d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="a278d-127">INPUTS</span></span>

### <span data-ttu-id="a278d-128">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="a278d-128">IStorageContext</span></span>

<span data-ttu-id="a278d-129">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a278d-129">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="a278d-130">字串</span><span class="sxs-lookup"><span data-stu-id="a278d-130">String</span></span>

<span data-ttu-id="a278d-131">形參 "Table" 接受來自管線的 "String" 類型的值</span><span class="sxs-lookup"><span data-stu-id="a278d-131">Parameter 'Table' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="a278d-132">輸出</span><span class="sxs-lookup"><span data-stu-id="a278d-132">OUTPUTS</span></span>

### <span data-ttu-id="a278d-133">System.object</span><span class="sxs-lookup"><span data-stu-id="a278d-133">System.String</span></span>

## <span data-ttu-id="a278d-134">筆記</span><span class="sxs-lookup"><span data-stu-id="a278d-134">NOTES</span></span>

## <span data-ttu-id="a278d-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="a278d-135">RELATED LINKS</span></span>

[<span data-ttu-id="a278d-136">AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a278d-136">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="a278d-137">新-AzureStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="a278d-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="a278d-138">移除-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a278d-138">Remove-AzureStorageTableStoredAccessPolicy</span></span>](./Remove-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="a278d-139">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a278d-139">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)


