---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
ms.openlocfilehash: c79e8c225fbbc901d9c39eed85d795cf27d6d1d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612729"
---
# <span data-ttu-id="1a673-101">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1a673-101">Test-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="1a673-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1a673-102">SYNOPSIS</span></span>
<span data-ttu-id="1a673-103">測試 Data Lake Store 中的檔案或資料夾是否存在。</span><span class="sxs-lookup"><span data-stu-id="1a673-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1a673-104">句法</span><span class="sxs-lookup"><span data-stu-id="1a673-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a673-105">說明</span><span class="sxs-lookup"><span data-stu-id="1a673-105">DESCRIPTION</span></span>
<span data-ttu-id="1a673-106">**Test AzDataLakeStoreItem** Cmdlet 會測試 Data Lake store 中的檔案或資料夾是否存在。</span><span class="sxs-lookup"><span data-stu-id="1a673-106">The **Test-AzDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1a673-107">示例</span><span class="sxs-lookup"><span data-stu-id="1a673-107">EXAMPLES</span></span>

### <span data-ttu-id="1a673-108">範例1：測試檔案</span><span class="sxs-lookup"><span data-stu-id="1a673-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="1a673-109">這個命令會測試檔案 Test.csv 是否存在於 ContosoADL 帳戶中。</span><span class="sxs-lookup"><span data-stu-id="1a673-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="1a673-110">參數</span><span class="sxs-lookup"><span data-stu-id="1a673-110">PARAMETERS</span></span>

### <span data-ttu-id="1a673-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="1a673-111">-Account</span></span>
<span data-ttu-id="1a673-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a673-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1a673-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a673-113">-DefaultProfile</span></span>
<span data-ttu-id="1a673-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1a673-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a673-115">-Path</span><span class="sxs-lookup"><span data-stu-id="1a673-115">-Path</span></span>
<span data-ttu-id="1a673-116">指定要測試之專案的資料 Lake Store 路徑，從根目錄 (/) 開始。</span><span class="sxs-lookup"><span data-stu-id="1a673-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="1a673-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="1a673-117">-PathType</span></span>
<span data-ttu-id="1a673-118">指定要測試的專案類型。</span><span class="sxs-lookup"><span data-stu-id="1a673-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="1a673-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1a673-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1a673-120">每</span><span class="sxs-lookup"><span data-stu-id="1a673-120">Any</span></span> 
- <span data-ttu-id="1a673-121">檔案</span><span class="sxs-lookup"><span data-stu-id="1a673-121">File</span></span> 
- <span data-ttu-id="1a673-122">資料夾</span><span class="sxs-lookup"><span data-stu-id="1a673-122">Folder</span></span>

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

### <span data-ttu-id="1a673-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a673-123">CommonParameters</span></span>
<span data-ttu-id="1a673-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1a673-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a673-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1a673-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a673-126">輸入</span><span class="sxs-lookup"><span data-stu-id="1a673-126">INPUTS</span></span>

### <span data-ttu-id="1a673-127">System.object</span><span class="sxs-lookup"><span data-stu-id="1a673-127">System.String</span></span>

### <span data-ttu-id="1a673-128">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="1a673-128">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="1a673-129">DataLakeStoreEnums + PathType （DataLakeStore）。</span><span class="sxs-lookup"><span data-stu-id="1a673-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="1a673-130">輸出</span><span class="sxs-lookup"><span data-stu-id="1a673-130">OUTPUTS</span></span>

### <span data-ttu-id="1a673-131">System.object</span><span class="sxs-lookup"><span data-stu-id="1a673-131">System.Boolean</span></span>

## <span data-ttu-id="1a673-132">筆記</span><span class="sxs-lookup"><span data-stu-id="1a673-132">NOTES</span></span>

## <span data-ttu-id="1a673-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="1a673-133">RELATED LINKS</span></span>

[<span data-ttu-id="1a673-134">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1a673-134">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="1a673-135">AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1a673-135">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="1a673-136">匯入-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1a673-136">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="1a673-137">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1a673-137">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="1a673-138">移動流覽 AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1a673-138">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="1a673-139">移除-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1a673-139">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)


