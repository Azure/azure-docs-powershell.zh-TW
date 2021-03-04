---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 92ad3143a52f0d9a81505375ff5abd221784fb2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910517"
---
# <span data-ttu-id="d393d-101">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="d393d-101">Get-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="d393d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d393d-102">SYNOPSIS</span></span>
<span data-ttu-id="d393d-103">在垃圾桶中搜尋符合篩選的已刪除專案。</span><span class="sxs-lookup"><span data-stu-id="d393d-103">Searches for deleted entries in trash which match the filter.</span></span>

## <span data-ttu-id="d393d-104">語法</span><span class="sxs-lookup"><span data-stu-id="d393d-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d393d-105">描述</span><span class="sxs-lookup"><span data-stu-id="d393d-105">DESCRIPTION</span></span>
<span data-ttu-id="d393d-106">**Get-AzDataLakeStoreDeletedItem** Cmdlet 會搜尋 Data Lake Store 中符合指定篩選的已刪除檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="d393d-106">The **Get-AzDataLakeStoreDeletedItem** cmdlet searches the deleted files or folders in Data Lake Store which match the given filter.</span></span>
<span data-ttu-id="d393d-107">它會顯示已刪除專案的下列屬性 ：OriginalPath、TrashDirPath、Type、CreationTime。</span><span class="sxs-lookup"><span data-stu-id="d393d-107">It displays the following attributes of the deleted items - OriginalPath, TrashDirPath, Type, CreationTime.</span></span>
<span data-ttu-id="d393d-108">這可能是一項長時間執行的工作，因為它可能必須搜尋垃圾桶中的數百萬個檔案，而且可能會以工作方式執行。</span><span class="sxs-lookup"><span data-stu-id="d393d-108">This could be a long running operation as it may have to search through millions of files in trash and could be run as a job.</span></span>
<span data-ttu-id="d393d-109">注意：取消下載檔案是最佳方法。</span><span class="sxs-lookup"><span data-stu-id="d393d-109">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="d393d-110">不保證檔案一旦刪除後即可以還原。</span><span class="sxs-lookup"><span data-stu-id="d393d-110">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="d393d-111">此 API 的使用會透過白名單啟用。</span><span class="sxs-lookup"><span data-stu-id="d393d-111">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="d393d-112">如果您的 ADL 帳戶未列入白名單，則使用此 api 會放棄未執行例外。</span><span class="sxs-lookup"><span data-stu-id="d393d-112">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="d393d-113">如需詳細資訊和協助，請聯絡 Microsoft 支援服務。</span><span class="sxs-lookup"><span data-stu-id="d393d-113">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="d393d-114">例子</span><span class="sxs-lookup"><span data-stu-id="d393d-114">EXAMPLES</span></span>

### <span data-ttu-id="d393d-115">範例：從 Data Lake Store 取得檔案詳細資料</span><span class="sxs-lookup"><span data-stu-id="d393d-115">Example: Get details of a file from the Data Lake Store</span></span>
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## <span data-ttu-id="d393d-116">參數</span><span class="sxs-lookup"><span data-stu-id="d393d-116">PARAMETERS</span></span>

### <span data-ttu-id="d393d-117">-帳戶</span><span class="sxs-lookup"><span data-stu-id="d393d-117">-Account</span></span>
<span data-ttu-id="d393d-118">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="d393d-118">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d393d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d393d-119">-AsJob</span></span>
<span data-ttu-id="d393d-120">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d393d-120">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="d393d-121">-Count</span><span class="sxs-lookup"><span data-stu-id="d393d-121">-Count</span></span>
<span data-ttu-id="d393d-122">指定使用者想要尋找的結果數目。</span><span class="sxs-lookup"><span data-stu-id="d393d-122">Specifies the number of results the user wants to find.</span></span> <span data-ttu-id="d393d-123">查詢會執行直到找到 Count 結果或搜尋整個垃圾桶 ，以先發生者為准。</span><span class="sxs-lookup"><span data-stu-id="d393d-123">The query runs until it finds Count results or it searches through entire trash, whichever happens first.</span></span>

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

### <span data-ttu-id="d393d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d393d-124">-DefaultProfile</span></span>
<span data-ttu-id="d393d-125">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d393d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d393d-126">-篩選</span><span class="sxs-lookup"><span data-stu-id="d393d-126">-Filter</span></span>
<span data-ttu-id="d393d-127">指定搜尋查詢。</span><span class="sxs-lookup"><span data-stu-id="d393d-127">Specifies the search query.</span></span> <span data-ttu-id="d393d-128">更特定的值會提供更相關的結果。</span><span class="sxs-lookup"><span data-stu-id="d393d-128">A more specific value gives more relevant results.</span></span>

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

### <span data-ttu-id="d393d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d393d-129">CommonParameters</span></span>
<span data-ttu-id="d393d-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d393d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d393d-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="d393d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d393d-132">輸入</span><span class="sxs-lookup"><span data-stu-id="d393d-132">INPUTS</span></span>

### <span data-ttu-id="d393d-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d393d-133">System.String</span></span>

## <span data-ttu-id="d393d-134">輸出</span><span class="sxs-lookup"><span data-stu-id="d393d-134">OUTPUTS</span></span>

### <span data-ttu-id="d393d-135">System.Collections.generic.List<Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStoreDeletedItem></span><span class="sxs-lookup"><span data-stu-id="d393d-135">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span></span>

## <span data-ttu-id="d393d-136">筆記</span><span class="sxs-lookup"><span data-stu-id="d393d-136">NOTES</span></span>

## <span data-ttu-id="d393d-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="d393d-137">RELATED LINKS</span></span>

[<span data-ttu-id="d393d-138">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="d393d-138">Restore-AzDataLakeStoreDeletedItem</span></span>](./Restore-AzDataLakeStoreDeletedItem.md)