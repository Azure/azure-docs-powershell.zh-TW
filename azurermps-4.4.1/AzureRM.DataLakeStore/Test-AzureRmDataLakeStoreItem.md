---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a5087c3c2d2354eb33ab9777687d43f56f3eb42c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93451712"
---
# <span data-ttu-id="2751b-101">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2751b-101">Test-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="2751b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2751b-102">SYNOPSIS</span></span>
<span data-ttu-id="2751b-103">測試 Data Lake Store 中的檔案或資料夾是否存在。</span><span class="sxs-lookup"><span data-stu-id="2751b-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2751b-104">句法</span><span class="sxs-lookup"><span data-stu-id="2751b-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2751b-105">說明</span><span class="sxs-lookup"><span data-stu-id="2751b-105">DESCRIPTION</span></span>
<span data-ttu-id="2751b-106">**Test AzureRmDataLakeStoreItem** Cmdlet 會測試 Data Lake store 中的檔案或資料夾是否存在。</span><span class="sxs-lookup"><span data-stu-id="2751b-106">The **Test-AzureRmDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2751b-107">示例</span><span class="sxs-lookup"><span data-stu-id="2751b-107">EXAMPLES</span></span>

### <span data-ttu-id="2751b-108">範例1：測試檔案</span><span class="sxs-lookup"><span data-stu-id="2751b-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="2751b-109">這個命令會測試檔案 Test.csv 是否存在於 ContosoADL 帳戶中。</span><span class="sxs-lookup"><span data-stu-id="2751b-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="2751b-110">參數</span><span class="sxs-lookup"><span data-stu-id="2751b-110">PARAMETERS</span></span>

### <span data-ttu-id="2751b-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="2751b-111">-Account</span></span>
<span data-ttu-id="2751b-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="2751b-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="2751b-113">-Path</span><span class="sxs-lookup"><span data-stu-id="2751b-113">-Path</span></span>
<span data-ttu-id="2751b-114">指定要測試之專案的資料 Lake Store 路徑，從根目錄 (/) 開始。</span><span class="sxs-lookup"><span data-stu-id="2751b-114">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="2751b-115">-PathType</span><span class="sxs-lookup"><span data-stu-id="2751b-115">-PathType</span></span>
<span data-ttu-id="2751b-116">指定要測試的專案類型。</span><span class="sxs-lookup"><span data-stu-id="2751b-116">Specifies the type of item to test.</span></span>
<span data-ttu-id="2751b-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2751b-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2751b-118">每</span><span class="sxs-lookup"><span data-stu-id="2751b-118">Any</span></span> 
- <span data-ttu-id="2751b-119">檔案</span><span class="sxs-lookup"><span data-stu-id="2751b-119">File</span></span> 
- <span data-ttu-id="2751b-120">資料夾</span><span class="sxs-lookup"><span data-stu-id="2751b-120">Folder</span></span>

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

### <span data-ttu-id="2751b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2751b-121">-DefaultProfile</span></span>
<span data-ttu-id="2751b-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2751b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2751b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2751b-123">CommonParameters</span></span>
<span data-ttu-id="2751b-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2751b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2751b-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2751b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2751b-126">輸入</span><span class="sxs-lookup"><span data-stu-id="2751b-126">INPUTS</span></span>

## <span data-ttu-id="2751b-127">輸出</span><span class="sxs-lookup"><span data-stu-id="2751b-127">OUTPUTS</span></span>

### <span data-ttu-id="2751b-128">bool</span><span class="sxs-lookup"><span data-stu-id="2751b-128">bool</span></span>
<span data-ttu-id="2751b-129">True 或 false，表示存在指定檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="2751b-129">True or false indicating the existence of the specified file or folder.</span></span>

## <span data-ttu-id="2751b-130">筆記</span><span class="sxs-lookup"><span data-stu-id="2751b-130">NOTES</span></span>

## <span data-ttu-id="2751b-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="2751b-131">RELATED LINKS</span></span>

[<span data-ttu-id="2751b-132">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2751b-132">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2751b-133">AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2751b-133">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2751b-134">匯入-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2751b-134">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2751b-135">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2751b-135">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2751b-136">移動流覽 AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2751b-136">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="2751b-137">移除-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="2751b-137">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)


