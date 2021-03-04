---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: 3a39e2f341404ac3f6dbb75c27408dd9d9ee2d47
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916570"
---
# <span data-ttu-id="dc311-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dc311-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="dc311-102">簡介</span><span class="sxs-lookup"><span data-stu-id="dc311-102">SYNOPSIS</span></span>
<span data-ttu-id="dc311-103">在 Data Lake Store 中，獲得檔案或資料夾的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="dc311-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="dc311-104">語法</span><span class="sxs-lookup"><span data-stu-id="dc311-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc311-105">描述</span><span class="sxs-lookup"><span data-stu-id="dc311-105">DESCRIPTION</span></span>
<span data-ttu-id="dc311-106">**Get-AzDataLakeStoreItem** Cmdlet 會取得 Data Lake Store 中檔案或資料夾的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="dc311-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="dc311-107">例子</span><span class="sxs-lookup"><span data-stu-id="dc311-107">EXAMPLES</span></span>

### <span data-ttu-id="dc311-108">範例 1：從 Data Lake Store 取得檔案詳細資料</span><span class="sxs-lookup"><span data-stu-id="dc311-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="dc311-109">此命令會從 Data Lake Store Test.csv檔案的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="dc311-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="dc311-110">參數</span><span class="sxs-lookup"><span data-stu-id="dc311-110">PARAMETERS</span></span>

### <span data-ttu-id="dc311-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="dc311-111">-Account</span></span>
<span data-ttu-id="dc311-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="dc311-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="dc311-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc311-113">-DefaultProfile</span></span>
<span data-ttu-id="dc311-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="dc311-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc311-115">-路徑</span><span class="sxs-lookup"><span data-stu-id="dc311-115">-Path</span></span>
<span data-ttu-id="dc311-116">指定從根目錄開始取得專案詳細資料的 Data Lake Store 路徑 (/) 。</span><span class="sxs-lookup"><span data-stu-id="dc311-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc311-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc311-117">CommonParameters</span></span>
<span data-ttu-id="dc311-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="dc311-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc311-119">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="dc311-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc311-120">輸入</span><span class="sxs-lookup"><span data-stu-id="dc311-120">INPUTS</span></span>

### <span data-ttu-id="dc311-121">System.String</span><span class="sxs-lookup"><span data-stu-id="dc311-121">System.String</span></span>

### <span data-ttu-id="dc311-122">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="dc311-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="dc311-123">輸出</span><span class="sxs-lookup"><span data-stu-id="dc311-123">OUTPUTS</span></span>

### <span data-ttu-id="dc311-124">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dc311-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="dc311-125">筆記</span><span class="sxs-lookup"><span data-stu-id="dc311-125">NOTES</span></span>

## <span data-ttu-id="dc311-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="dc311-126">RELATED LINKS</span></span>

[<span data-ttu-id="dc311-127">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dc311-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="dc311-128">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="dc311-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="dc311-129">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dc311-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="dc311-130">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dc311-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="dc311-131">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dc311-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="dc311-132">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dc311-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="dc311-133">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dc311-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="dc311-134">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="dc311-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


