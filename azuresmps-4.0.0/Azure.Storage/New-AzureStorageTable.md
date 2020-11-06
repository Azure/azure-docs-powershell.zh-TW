---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a58f869d5308b176a68614cbb2fa2fec401fa14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443264"
---
# <span data-ttu-id="fed6c-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="fed6c-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="fed6c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fed6c-102">SYNOPSIS</span></span>
<span data-ttu-id="fed6c-103">建立儲存空間表。</span><span class="sxs-lookup"><span data-stu-id="fed6c-103">Creates a storage table.</span></span>

## <span data-ttu-id="fed6c-104">句法</span><span class="sxs-lookup"><span data-stu-id="fed6c-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="fed6c-105">說明</span><span class="sxs-lookup"><span data-stu-id="fed6c-105">DESCRIPTION</span></span>
<span data-ttu-id="fed6c-106">**新的-AzureStorageTable** Cmdlet 會建立與 Azure 中的儲存空間帳戶相關聯的儲存空間表。</span><span class="sxs-lookup"><span data-stu-id="fed6c-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="fed6c-107">示例</span><span class="sxs-lookup"><span data-stu-id="fed6c-107">EXAMPLES</span></span>

### <span data-ttu-id="fed6c-108">範例1：建立 azure 儲存空間資料表</span><span class="sxs-lookup"><span data-stu-id="fed6c-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="fed6c-109">這個命令會建立名稱為 tableabc 的儲存空間資料表。</span><span class="sxs-lookup"><span data-stu-id="fed6c-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="fed6c-110">範例2：建立多個 azure 儲存空間資料表</span><span class="sxs-lookup"><span data-stu-id="fed6c-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="fed6c-111">這個命令會建立多個資料表。</span><span class="sxs-lookup"><span data-stu-id="fed6c-111">This command creates multiple tables.</span></span>
<span data-ttu-id="fed6c-112">它會使用 .NET **字串** 類別的 **Split** 方法，然後傳送管線上的名稱。</span><span class="sxs-lookup"><span data-stu-id="fed6c-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="fed6c-113">參數</span><span class="sxs-lookup"><span data-stu-id="fed6c-113">PARAMETERS</span></span>

### <span data-ttu-id="fed6c-114">-內容</span><span class="sxs-lookup"><span data-stu-id="fed6c-114">-Context</span></span>
<span data-ttu-id="fed6c-115">指定儲存內容。</span><span class="sxs-lookup"><span data-stu-id="fed6c-115">Specifies the storage context.</span></span>
<span data-ttu-id="fed6c-116">若要建立它，您可以使用 New-AzureStorageContext Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fed6c-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fed6c-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="fed6c-117">-Name</span></span>
<span data-ttu-id="fed6c-118">指定新資料表的名稱。</span><span class="sxs-lookup"><span data-stu-id="fed6c-118">Specifies a name for the new table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fed6c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fed6c-119">CommonParameters</span></span>
<span data-ttu-id="fed6c-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fed6c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fed6c-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fed6c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fed6c-122">輸入</span><span class="sxs-lookup"><span data-stu-id="fed6c-122">INPUTS</span></span>

## <span data-ttu-id="fed6c-123">輸出</span><span class="sxs-lookup"><span data-stu-id="fed6c-123">OUTPUTS</span></span>

## <span data-ttu-id="fed6c-124">筆記</span><span class="sxs-lookup"><span data-stu-id="fed6c-124">NOTES</span></span>

## <span data-ttu-id="fed6c-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="fed6c-125">RELATED LINKS</span></span>

[<span data-ttu-id="fed6c-126">AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="fed6c-126">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="fed6c-127">移除-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="fed6c-127">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


