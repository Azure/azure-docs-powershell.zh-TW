---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: b1a570d2821606944d4afde21919dad8832ed380
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623712"
---
# <span data-ttu-id="ef918-101">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ef918-101">Get-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="ef918-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef918-102">SYNOPSIS</span></span>
<span data-ttu-id="ef918-103">取得 Data Lake Store 中檔案或資料夾的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ef918-103">Gets the details of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef918-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef918-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef918-105">說明</span><span class="sxs-lookup"><span data-stu-id="ef918-105">DESCRIPTION</span></span>
<span data-ttu-id="ef918-106">**AzureRmDataLakeStoreItem** Cmdlet 會取得 Data Lake store 中檔案或資料夾的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ef918-106">The **Get-AzureRmDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="ef918-107">示例</span><span class="sxs-lookup"><span data-stu-id="ef918-107">EXAMPLES</span></span>

### <span data-ttu-id="ef918-108">範例1：從 Data Lake Store 取得檔案的詳細資料</span><span class="sxs-lookup"><span data-stu-id="ef918-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="ef918-109">這個命令會從 Data Lake Store 取得檔案 Test.csv 的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ef918-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="ef918-110">參數</span><span class="sxs-lookup"><span data-stu-id="ef918-110">PARAMETERS</span></span>

### <span data-ttu-id="ef918-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="ef918-111">-Account</span></span>
<span data-ttu-id="ef918-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef918-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef918-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef918-113">-DefaultProfile</span></span>
<span data-ttu-id="ef918-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ef918-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef918-115">-Path</span><span class="sxs-lookup"><span data-stu-id="ef918-115">-Path</span></span>
<span data-ttu-id="ef918-116">指定資料 Lake Store 路徑，從根目錄 (/) 開始，可從該目錄取得專案的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ef918-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef918-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef918-117">CommonParameters</span></span>
<span data-ttu-id="ef918-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef918-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef918-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ef918-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef918-120">輸入</span><span class="sxs-lookup"><span data-stu-id="ef918-120">INPUTS</span></span>

### <span data-ttu-id="ef918-121">所有</span><span class="sxs-lookup"><span data-stu-id="ef918-121">None</span></span>
<span data-ttu-id="ef918-122">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="ef918-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ef918-123">輸出</span><span class="sxs-lookup"><span data-stu-id="ef918-123">OUTPUTS</span></span>

### <span data-ttu-id="ef918-124">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ef918-124">DataLakeStoreItem</span></span>
<span data-ttu-id="ef918-125">指定路徑中的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="ef918-125">The file or folder at the path specified.</span></span>

## <span data-ttu-id="ef918-126">筆記</span><span class="sxs-lookup"><span data-stu-id="ef918-126">NOTES</span></span>

## <span data-ttu-id="ef918-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef918-127">RELATED LINKS</span></span>

[<span data-ttu-id="ef918-128">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ef918-128">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ef918-129">AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="ef918-129">Get-AzureRmDataLakeStoreChildItem</span></span>](./Get-AzureRmDataLakeStoreChildItem.md)

[<span data-ttu-id="ef918-130">匯入-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ef918-130">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ef918-131">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ef918-131">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ef918-132">移動流覽 AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ef918-132">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ef918-133">新-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ef918-133">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ef918-134">移除-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ef918-134">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="ef918-135">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="ef918-135">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


