---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: e9410c8bd63a123f275f6e644971870b998deea0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453768"
---
# <span data-ttu-id="02a40-101">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="02a40-101">Test-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="02a40-102">摘要</span><span class="sxs-lookup"><span data-stu-id="02a40-102">SYNOPSIS</span></span>
<span data-ttu-id="02a40-103">測試 Data Lake Store 中的檔案或資料夾是否存在。</span><span class="sxs-lookup"><span data-stu-id="02a40-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02a40-104">句法</span><span class="sxs-lookup"><span data-stu-id="02a40-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02a40-105">說明</span><span class="sxs-lookup"><span data-stu-id="02a40-105">DESCRIPTION</span></span>
<span data-ttu-id="02a40-106">**Test AzureRmDataLakeStoreItem** Cmdlet 會測試 Data Lake store 中的檔案或資料夾是否存在。</span><span class="sxs-lookup"><span data-stu-id="02a40-106">The **Test-AzureRmDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="02a40-107">示例</span><span class="sxs-lookup"><span data-stu-id="02a40-107">EXAMPLES</span></span>

### <span data-ttu-id="02a40-108">範例1：測試檔案</span><span class="sxs-lookup"><span data-stu-id="02a40-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="02a40-109">這個命令會測試檔案 Test.csv 是否存在於 ContosoADL 帳戶中。</span><span class="sxs-lookup"><span data-stu-id="02a40-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="02a40-110">參數</span><span class="sxs-lookup"><span data-stu-id="02a40-110">PARAMETERS</span></span>

### <span data-ttu-id="02a40-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="02a40-111">-Account</span></span>
<span data-ttu-id="02a40-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="02a40-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="02a40-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a40-113">-DefaultProfile</span></span>
<span data-ttu-id="02a40-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="02a40-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02a40-115">-Path</span><span class="sxs-lookup"><span data-stu-id="02a40-115">-Path</span></span>
<span data-ttu-id="02a40-116">指定要測試之專案的資料 Lake Store 路徑，從根目錄 (/) 開始。</span><span class="sxs-lookup"><span data-stu-id="02a40-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="02a40-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="02a40-117">-PathType</span></span>
<span data-ttu-id="02a40-118">指定要測試的專案類型。</span><span class="sxs-lookup"><span data-stu-id="02a40-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="02a40-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="02a40-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="02a40-120">每</span><span class="sxs-lookup"><span data-stu-id="02a40-120">Any</span></span> 
- <span data-ttu-id="02a40-121">檔案</span><span class="sxs-lookup"><span data-stu-id="02a40-121">File</span></span> 
- <span data-ttu-id="02a40-122">資料夾</span><span class="sxs-lookup"><span data-stu-id="02a40-122">Folder</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType
Parameter Sets: (All)
Aliases:
Accepted values: Any, File, Folder

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02a40-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a40-123">CommonParameters</span></span>
<span data-ttu-id="02a40-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="02a40-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a40-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="02a40-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a40-126">輸入</span><span class="sxs-lookup"><span data-stu-id="02a40-126">INPUTS</span></span>

### <span data-ttu-id="02a40-127">System.object</span><span class="sxs-lookup"><span data-stu-id="02a40-127">System.String</span></span>

### <span data-ttu-id="02a40-128">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="02a40-128">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="02a40-129">DataLakeStoreEnums + PathType （DataLakeStore）。</span><span class="sxs-lookup"><span data-stu-id="02a40-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="02a40-130">輸出</span><span class="sxs-lookup"><span data-stu-id="02a40-130">OUTPUTS</span></span>

### <span data-ttu-id="02a40-131">System.object</span><span class="sxs-lookup"><span data-stu-id="02a40-131">System.Boolean</span></span>

## <span data-ttu-id="02a40-132">筆記</span><span class="sxs-lookup"><span data-stu-id="02a40-132">NOTES</span></span>

## <span data-ttu-id="02a40-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="02a40-133">RELATED LINKS</span></span>

[<span data-ttu-id="02a40-134">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="02a40-134">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="02a40-135">AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="02a40-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="02a40-136">匯入-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="02a40-136">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="02a40-137">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="02a40-137">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="02a40-138">移動流覽 AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="02a40-138">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="02a40-139">移除-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="02a40-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)


