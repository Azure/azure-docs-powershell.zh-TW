---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3ba13fb1ee18f5dcc35b81ff70ebd7c5a61d1e4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445275"
---
# <span data-ttu-id="cb7ae-101">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="cb7ae-101">Get-AzureStorageTable</span></span>

## <span data-ttu-id="cb7ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb7ae-102">SYNOPSIS</span></span>
<span data-ttu-id="cb7ae-103">列出儲存資料表。</span><span class="sxs-lookup"><span data-stu-id="cb7ae-103">Lists the storage tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb7ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb7ae-104">SYNTAX</span></span>

### <span data-ttu-id="cb7ae-105">TableName (預設) </span><span class="sxs-lookup"><span data-stu-id="cb7ae-105">TableName (Default)</span></span>
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="cb7ae-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="cb7ae-106">TablePrefix</span></span>
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="cb7ae-107">說明</span><span class="sxs-lookup"><span data-stu-id="cb7ae-107">DESCRIPTION</span></span>
<span data-ttu-id="cb7ae-108">**AzureStorageTable** Cmdlet 會列出與 Azure 中的儲存空間帳戶相關聯的儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="cb7ae-108">The **Get-AzureStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="cb7ae-109">示例</span><span class="sxs-lookup"><span data-stu-id="cb7ae-109">EXAMPLES</span></span>

### <span data-ttu-id="cb7ae-110">範例1：列出所有 Azure 儲存空間資料表</span><span class="sxs-lookup"><span data-stu-id="cb7ae-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzureStorageTable
```

<span data-ttu-id="cb7ae-111">這個命令會取得儲存空間帳戶的所有儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="cb7ae-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="cb7ae-112">範例2：使用萬用字元列出 Azure 儲存空間資料表</span><span class="sxs-lookup"><span data-stu-id="cb7ae-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageTable -Name table*
```

<span data-ttu-id="cb7ae-113">這個命令使用萬用字元來取得名稱以 table 開頭的儲存資料表。</span><span class="sxs-lookup"><span data-stu-id="cb7ae-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="cb7ae-114">範例3：使用表格名稱首碼列出 Azure 儲存空間資料表</span><span class="sxs-lookup"><span data-stu-id="cb7ae-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

<span data-ttu-id="cb7ae-115">這個命令會使用 *Prefix* 參數來取得名稱以 table 開頭的儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="cb7ae-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="cb7ae-116">參數</span><span class="sxs-lookup"><span data-stu-id="cb7ae-116">PARAMETERS</span></span>

### <span data-ttu-id="cb7ae-117">-內容</span><span class="sxs-lookup"><span data-stu-id="cb7ae-117">-Context</span></span>
<span data-ttu-id="cb7ae-118">指定儲存內容。</span><span class="sxs-lookup"><span data-stu-id="cb7ae-118">Specifies the storage context.</span></span>
<span data-ttu-id="cb7ae-119">若要建立它，您可以使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb7ae-119">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="cb7ae-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb7ae-120">-Name</span></span>
<span data-ttu-id="cb7ae-121">指定資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="cb7ae-121">Specifies the table name.</span></span>
<span data-ttu-id="cb7ae-122">如果資料表名稱是空值，該 Cmdlet 會列出所有的資料表。</span><span class="sxs-lookup"><span data-stu-id="cb7ae-122">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="cb7ae-123">否則，它會列出符合指定名稱或一般名稱模式的所有資料表。</span><span class="sxs-lookup"><span data-stu-id="cb7ae-123">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="cb7ae-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="cb7ae-124">-Prefix</span></span>
<span data-ttu-id="cb7ae-125">指定要取得的資料表名稱中所用的首碼。</span><span class="sxs-lookup"><span data-stu-id="cb7ae-125">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="cb7ae-126">您可以使用此程式來找出所有以相同字串（例如 table）開頭的資料表。</span><span class="sxs-lookup"><span data-stu-id="cb7ae-126">You can use this to find all tables that start with the same string, such as table.</span></span>

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

### <span data-ttu-id="cb7ae-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb7ae-127">CommonParameters</span></span>
<span data-ttu-id="cb7ae-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb7ae-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb7ae-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cb7ae-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb7ae-130">輸入</span><span class="sxs-lookup"><span data-stu-id="cb7ae-130">INPUTS</span></span>

### <span data-ttu-id="cb7ae-131">IStorageCoNtext</span><span class="sxs-lookup"><span data-stu-id="cb7ae-131">IStorageContext</span></span>

<span data-ttu-id="cb7ae-132">參數「CoNtext」接受來自管線的 "IStorageCoNtext" 類型的值</span><span class="sxs-lookup"><span data-stu-id="cb7ae-132">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="cb7ae-133">字串</span><span class="sxs-lookup"><span data-stu-id="cb7ae-133">String</span></span>

<span data-ttu-id="cb7ae-134">形參 "Name" 接受管線中類型 "String" 的值</span><span class="sxs-lookup"><span data-stu-id="cb7ae-134">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="cb7ae-135">輸出</span><span class="sxs-lookup"><span data-stu-id="cb7ae-135">OUTPUTS</span></span>

### <span data-ttu-id="cb7ae-136">AzureStorageTable WindowsAzure. ResourceModel。</span><span class="sxs-lookup"><span data-stu-id="cb7ae-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="cb7ae-137">筆記</span><span class="sxs-lookup"><span data-stu-id="cb7ae-137">NOTES</span></span>

## <span data-ttu-id="cb7ae-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb7ae-138">RELATED LINKS</span></span>

[<span data-ttu-id="cb7ae-139">新-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="cb7ae-139">New-AzureStorageTable</span></span>](./New-AzureStorageTable.md)

[<span data-ttu-id="cb7ae-140">移除-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="cb7ae-140">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


