---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f2bccab190fc27b5e97ecf3af502d3488f28998
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443415"
---
# <span data-ttu-id="ce7ee-101">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="ce7ee-101">Get-AzureStorageTable</span></span>

## <span data-ttu-id="ce7ee-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce7ee-102">SYNOPSIS</span></span>
<span data-ttu-id="ce7ee-103">列出儲存資料表。</span><span class="sxs-lookup"><span data-stu-id="ce7ee-103">Lists the storage tables.</span></span>

## <span data-ttu-id="ce7ee-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce7ee-104">SYNTAX</span></span>

### <span data-ttu-id="ce7ee-105">TableName (預設) </span><span class="sxs-lookup"><span data-stu-id="ce7ee-105">TableName (Default)</span></span>
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="ce7ee-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="ce7ee-106">TablePrefix</span></span>
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="ce7ee-107">說明</span><span class="sxs-lookup"><span data-stu-id="ce7ee-107">DESCRIPTION</span></span>
<span data-ttu-id="ce7ee-108">**AzureStorageTable** Cmdlet 會列出與 Azure 中的儲存空間帳戶相關聯的儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="ce7ee-108">The **Get-AzureStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="ce7ee-109">示例</span><span class="sxs-lookup"><span data-stu-id="ce7ee-109">EXAMPLES</span></span>

### <span data-ttu-id="ce7ee-110">範例1：列出所有 Azure 儲存空間資料表</span><span class="sxs-lookup"><span data-stu-id="ce7ee-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzureStorageTable
```

<span data-ttu-id="ce7ee-111">這個命令會取得儲存空間帳戶的所有儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="ce7ee-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="ce7ee-112">範例2：使用萬用字元列出 Azure 儲存空間資料表</span><span class="sxs-lookup"><span data-stu-id="ce7ee-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageTable -Name table*
```

<span data-ttu-id="ce7ee-113">這個命令使用萬用字元來取得名稱以 table 開頭的儲存資料表。</span><span class="sxs-lookup"><span data-stu-id="ce7ee-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="ce7ee-114">範例3：使用表格名稱首碼列出 Azure 儲存空間資料表</span><span class="sxs-lookup"><span data-stu-id="ce7ee-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

<span data-ttu-id="ce7ee-115">這個命令會使用 *Prefix* 參數來取得名稱以 table 開頭的儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="ce7ee-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="ce7ee-116">參數</span><span class="sxs-lookup"><span data-stu-id="ce7ee-116">PARAMETERS</span></span>

### <span data-ttu-id="ce7ee-117">-內容</span><span class="sxs-lookup"><span data-stu-id="ce7ee-117">-Context</span></span>
<span data-ttu-id="ce7ee-118">指定儲存內容。</span><span class="sxs-lookup"><span data-stu-id="ce7ee-118">Specifies the storage context.</span></span>
<span data-ttu-id="ce7ee-119">若要建立它，您可以使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce7ee-119">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ce7ee-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="ce7ee-120">-Name</span></span>
<span data-ttu-id="ce7ee-121">指定資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="ce7ee-121">Specifies the table name.</span></span>
<span data-ttu-id="ce7ee-122">如果資料表名稱是空值，該 Cmdlet 會列出所有的資料表。</span><span class="sxs-lookup"><span data-stu-id="ce7ee-122">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="ce7ee-123">否則，它會列出符合指定名稱或一般名稱模式的所有資料表。</span><span class="sxs-lookup"><span data-stu-id="ce7ee-123">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce7ee-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="ce7ee-124">-Prefix</span></span>
<span data-ttu-id="ce7ee-125">指定要取得的資料表名稱中所用的首碼。</span><span class="sxs-lookup"><span data-stu-id="ce7ee-125">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="ce7ee-126">您可以使用此程式來找出所有以相同字串（例如 table）開頭的資料表。</span><span class="sxs-lookup"><span data-stu-id="ce7ee-126">You can use this to find all tables that start with the same string, such as table.</span></span>

```yaml
Type: String
Parameter Sets: TablePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7ee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce7ee-127">CommonParameters</span></span>
<span data-ttu-id="ce7ee-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce7ee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce7ee-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ce7ee-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce7ee-130">輸入</span><span class="sxs-lookup"><span data-stu-id="ce7ee-130">INPUTS</span></span>

## <span data-ttu-id="ce7ee-131">輸出</span><span class="sxs-lookup"><span data-stu-id="ce7ee-131">OUTPUTS</span></span>

## <span data-ttu-id="ce7ee-132">筆記</span><span class="sxs-lookup"><span data-stu-id="ce7ee-132">NOTES</span></span>

## <span data-ttu-id="ce7ee-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce7ee-133">RELATED LINKS</span></span>

[<span data-ttu-id="ce7ee-134">新-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="ce7ee-134">New-AzureStorageTable</span></span>](./New-AzureStorageTable.md)

[<span data-ttu-id="ce7ee-135">移除-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="ce7ee-135">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


