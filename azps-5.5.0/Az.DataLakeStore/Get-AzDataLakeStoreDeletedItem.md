---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: cfcdf8accb5de467c5b243df2c973074fe9ae31a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141034"
---
# <span data-ttu-id="e97ca-101">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="e97ca-101">Get-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="e97ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e97ca-102">SYNOPSIS</span></span>
<span data-ttu-id="e97ca-103">搜尋 [垃圾桶] 中與篩選相符的已刪除專案。</span><span class="sxs-lookup"><span data-stu-id="e97ca-103">Searches for deleted entries in trash which match the filter.</span></span>

## <span data-ttu-id="e97ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="e97ca-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e97ca-105">說明</span><span class="sxs-lookup"><span data-stu-id="e97ca-105">DESCRIPTION</span></span>
<span data-ttu-id="e97ca-106">**AzDataLakeStoreDeletedItem** Cmdlet 會搜尋 Data Lake store 中已刪除的檔案或資料夾，這些檔案會與指定的篩選器相符。</span><span class="sxs-lookup"><span data-stu-id="e97ca-106">The **Get-AzDataLakeStoreDeletedItem** cmdlet searches the deleted files or folders in Data Lake Store which match the given filter.</span></span>
<span data-ttu-id="e97ca-107">它會顯示已刪除專案的下列屬性： OriginalPath、TrashDirPath、Type、CreationTime。</span><span class="sxs-lookup"><span data-stu-id="e97ca-107">It displays the following attributes of the deleted items - OriginalPath, TrashDirPath, Type, CreationTime.</span></span>
<span data-ttu-id="e97ca-108">這可能是長時間執行的作業，因為可能需要在垃圾桶中搜尋數百萬個檔案，而且可以作為工作執行。</span><span class="sxs-lookup"><span data-stu-id="e97ca-108">This could be a long running operation as it may have to search through millions of files in trash and could be run as a job.</span></span>
<span data-ttu-id="e97ca-109">注意： [未完成的檔案] 是最佳的操作。</span><span class="sxs-lookup"><span data-stu-id="e97ca-109">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="e97ca-110">在刪除檔案後，就不會保證檔案可以還原。</span><span class="sxs-lookup"><span data-stu-id="e97ca-110">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="e97ca-111">此 API 的使用是透過 whitelisting 啟用。</span><span class="sxs-lookup"><span data-stu-id="e97ca-111">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="e97ca-112">如果您的 ADL 帳戶未列入白名單，則使用這個 api 將會拋出未實現的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="e97ca-112">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="e97ca-113">如需進一步的資訊和協助，請聯絡 Microsoft 支援。</span><span class="sxs-lookup"><span data-stu-id="e97ca-113">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="e97ca-114">示例</span><span class="sxs-lookup"><span data-stu-id="e97ca-114">EXAMPLES</span></span>

### <span data-ttu-id="e97ca-115">範例：從 Data Lake Store 取得檔案的詳細資料</span><span class="sxs-lookup"><span data-stu-id="e97ca-115">Example: Get details of a file from the Data Lake Store</span></span>
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## <span data-ttu-id="e97ca-116">參數</span><span class="sxs-lookup"><span data-stu-id="e97ca-116">PARAMETERS</span></span>

### <span data-ttu-id="e97ca-117">-帳戶</span><span class="sxs-lookup"><span data-stu-id="e97ca-117">-Account</span></span>
<span data-ttu-id="e97ca-118">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e97ca-118">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="e97ca-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e97ca-119">-AsJob</span></span>
<span data-ttu-id="e97ca-120">在背景中執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e97ca-120">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e97ca-121">-Count</span><span class="sxs-lookup"><span data-stu-id="e97ca-121">-Count</span></span>
<span data-ttu-id="e97ca-122">指定使用者想要尋找的結果數目。</span><span class="sxs-lookup"><span data-stu-id="e97ca-122">Specifies the number of results the user wants to find.</span></span> <span data-ttu-id="e97ca-123">查詢會執行，直到找到 Count 結果，或它搜尋整個垃圾桶為止（視哪一開始）。</span><span class="sxs-lookup"><span data-stu-id="e97ca-123">The query runs until it finds Count results or it searches through entire trash, whichever happens first.</span></span>

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

### <span data-ttu-id="e97ca-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e97ca-124">-DefaultProfile</span></span>
<span data-ttu-id="e97ca-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e97ca-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e97ca-126">-篩選</span><span class="sxs-lookup"><span data-stu-id="e97ca-126">-Filter</span></span>
<span data-ttu-id="e97ca-127">指定搜尋查詢。</span><span class="sxs-lookup"><span data-stu-id="e97ca-127">Specifies the search query.</span></span> <span data-ttu-id="e97ca-128">更明確的值會提供更相關的結果。</span><span class="sxs-lookup"><span data-stu-id="e97ca-128">A more specific value gives more relevant results.</span></span>

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

### <span data-ttu-id="e97ca-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e97ca-129">CommonParameters</span></span>
<span data-ttu-id="e97ca-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e97ca-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e97ca-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e97ca-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e97ca-132">輸入</span><span class="sxs-lookup"><span data-stu-id="e97ca-132">INPUTS</span></span>

### <span data-ttu-id="e97ca-133">System.object</span><span class="sxs-lookup"><span data-stu-id="e97ca-133">System.String</span></span>

## <span data-ttu-id="e97ca-134">輸出</span><span class="sxs-lookup"><span data-stu-id="e97ca-134">OUTPUTS</span></span>

### <span data-ttu-id="e97ca-135">DataLakeStore DataLakeStoreDeletedItem<.> 中的 [系統集合]。</span><span class="sxs-lookup"><span data-stu-id="e97ca-135">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span></span>

## <span data-ttu-id="e97ca-136">筆記</span><span class="sxs-lookup"><span data-stu-id="e97ca-136">NOTES</span></span>

## <span data-ttu-id="e97ca-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="e97ca-137">RELATED LINKS</span></span>

[<span data-ttu-id="e97ca-138">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="e97ca-138">Restore-AzDataLakeStoreDeletedItem</span></span>](./Restore-AzDataLakeStoreDeletedItem.md)