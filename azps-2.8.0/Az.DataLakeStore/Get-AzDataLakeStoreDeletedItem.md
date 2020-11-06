---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 750203e954ef96619e32b63ffd6eae333bb852f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612797"
---
# <span data-ttu-id="79bea-101">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="79bea-101">Get-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="79bea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="79bea-102">SYNOPSIS</span></span>
<span data-ttu-id="79bea-103">搜尋 [垃圾桶] 中與篩選相符的已刪除專案。</span><span class="sxs-lookup"><span data-stu-id="79bea-103">Searches for deleted entries in trash which match the filter.</span></span>

## <span data-ttu-id="79bea-104">句法</span><span class="sxs-lookup"><span data-stu-id="79bea-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79bea-105">說明</span><span class="sxs-lookup"><span data-stu-id="79bea-105">DESCRIPTION</span></span>
<span data-ttu-id="79bea-106">**AzDataLakeStoreDeletedItem** Cmdlet 會搜尋 Data Lake store 中已刪除的檔案或資料夾，這些檔案會與指定的篩選器相符。</span><span class="sxs-lookup"><span data-stu-id="79bea-106">The **Get-AzDataLakeStoreDeletedItem** cmdlet searches the deleted files or folders in Data Lake Store which match the given filter.</span></span>
<span data-ttu-id="79bea-107">它會顯示已刪除專案的下列屬性： OriginalPath、TrashDirPath、Type、CreationTime。</span><span class="sxs-lookup"><span data-stu-id="79bea-107">It displays the following attributes of the deleted items - OriginalPath, TrashDirPath, Type, CreationTime.</span></span>
<span data-ttu-id="79bea-108">這可能是長時間執行的作業，因為可能需要在垃圾桶中搜尋數百萬個檔案，而且可以作為工作執行。</span><span class="sxs-lookup"><span data-stu-id="79bea-108">This could be a long running operation as it may have to search through millions of files in trash and could be run as a job.</span></span>

## <span data-ttu-id="79bea-109">示例</span><span class="sxs-lookup"><span data-stu-id="79bea-109">EXAMPLES</span></span>

### <span data-ttu-id="79bea-110">範例：從 Data Lake Store 取得檔案的詳細資料</span><span class="sxs-lookup"><span data-stu-id="79bea-110">Example: Get details of a file from the Data Lake Store</span></span>
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## <span data-ttu-id="79bea-111">參數</span><span class="sxs-lookup"><span data-stu-id="79bea-111">PARAMETERS</span></span>

### <span data-ttu-id="79bea-112">-帳戶</span><span class="sxs-lookup"><span data-stu-id="79bea-112">-Account</span></span>
<span data-ttu-id="79bea-113">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="79bea-113">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79bea-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79bea-114">-AsJob</span></span>
<span data-ttu-id="79bea-115">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="79bea-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="79bea-116">-Count</span><span class="sxs-lookup"><span data-stu-id="79bea-116">-Count</span></span>
<span data-ttu-id="79bea-117">指定使用者想要尋找的結果數目。</span><span class="sxs-lookup"><span data-stu-id="79bea-117">Specifies the number of results the user wants to find.</span></span> <span data-ttu-id="79bea-118">查詢會執行，直到找到 Count 結果，或它搜尋整個垃圾桶為止（視哪一開始）。</span><span class="sxs-lookup"><span data-stu-id="79bea-118">The query runs until it finds Count results or it searches through entire trash, whichever happens first.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79bea-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79bea-119">-DefaultProfile</span></span>
<span data-ttu-id="79bea-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="79bea-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79bea-121">-篩選</span><span class="sxs-lookup"><span data-stu-id="79bea-121">-Filter</span></span>
<span data-ttu-id="79bea-122">指定搜尋查詢。</span><span class="sxs-lookup"><span data-stu-id="79bea-122">Specifies the search query.</span></span> <span data-ttu-id="79bea-123">更明確的值會提供更相關的結果。</span><span class="sxs-lookup"><span data-stu-id="79bea-123">A more specific value gives more relevant results.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79bea-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79bea-124">CommonParameters</span></span>
<span data-ttu-id="79bea-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="79bea-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79bea-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="79bea-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79bea-127">輸入</span><span class="sxs-lookup"><span data-stu-id="79bea-127">INPUTS</span></span>

### <span data-ttu-id="79bea-128">System.object</span><span class="sxs-lookup"><span data-stu-id="79bea-128">System.String</span></span>

## <span data-ttu-id="79bea-129">輸出</span><span class="sxs-lookup"><span data-stu-id="79bea-129">OUTPUTS</span></span>

### <span data-ttu-id="79bea-130">DataLakeStore DataLakeStoreDeletedItem<.> 中的 [系統集合]。</span><span class="sxs-lookup"><span data-stu-id="79bea-130">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span></span>

## <span data-ttu-id="79bea-131">筆記</span><span class="sxs-lookup"><span data-stu-id="79bea-131">NOTES</span></span>

## <span data-ttu-id="79bea-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="79bea-132">RELATED LINKS</span></span>

[<span data-ttu-id="79bea-133">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="79bea-133">Restore-AzDataLakeStoreDeletedItem</span></span>](./Restore-AzDataLakeStoreDeletedItem.md)