---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 1727c0960d90a8566d2247e8d8e091f6ce66f9b5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622526"
---
# <span data-ttu-id="a6b02-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="a6b02-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="a6b02-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6b02-102">SYNOPSIS</span></span>
<span data-ttu-id="a6b02-103">將內容新增至 Data Lake Store 中的專案。</span><span class="sxs-lookup"><span data-stu-id="a6b02-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="a6b02-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6b02-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6b02-105">說明</span><span class="sxs-lookup"><span data-stu-id="a6b02-105">DESCRIPTION</span></span>
<span data-ttu-id="a6b02-106">**載入 AzDataLakeStoreItemContent** Cmdlet 會將內容新增至 Azure Data Lake store 中的專案。</span><span class="sxs-lookup"><span data-stu-id="a6b02-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="a6b02-107">示例</span><span class="sxs-lookup"><span data-stu-id="a6b02-107">EXAMPLES</span></span>

### <span data-ttu-id="a6b02-108">範例1：新增內容至檔案</span><span class="sxs-lookup"><span data-stu-id="a6b02-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="a6b02-109">這個命令會將內容新增至檔案 myFile.txt。</span><span class="sxs-lookup"><span data-stu-id="a6b02-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="a6b02-110">參數</span><span class="sxs-lookup"><span data-stu-id="a6b02-110">PARAMETERS</span></span>

### <span data-ttu-id="a6b02-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="a6b02-111">-Account</span></span>
<span data-ttu-id="a6b02-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6b02-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a6b02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6b02-113">-DefaultProfile</span></span>
<span data-ttu-id="a6b02-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a6b02-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6b02-115">編碼</span><span class="sxs-lookup"><span data-stu-id="a6b02-115">-Encoding</span></span>
<span data-ttu-id="a6b02-116">指定要建立之專案的編碼。</span><span class="sxs-lookup"><span data-stu-id="a6b02-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="a6b02-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a6b02-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a6b02-118">清楚</span><span class="sxs-lookup"><span data-stu-id="a6b02-118">Unknown</span></span>
- <span data-ttu-id="a6b02-119">字串</span><span class="sxs-lookup"><span data-stu-id="a6b02-119">String</span></span>
- <span data-ttu-id="a6b02-120">消除</span><span class="sxs-lookup"><span data-stu-id="a6b02-120">Unicode</span></span>
- <span data-ttu-id="a6b02-121">位元組</span><span class="sxs-lookup"><span data-stu-id="a6b02-121">Byte</span></span>
- <span data-ttu-id="a6b02-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="a6b02-122">BigEndianUnicode</span></span>
- <span data-ttu-id="a6b02-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="a6b02-123">UTF8</span></span>
- <span data-ttu-id="a6b02-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="a6b02-124">UTF7</span></span>
- <span data-ttu-id="a6b02-125">Ascii</span><span class="sxs-lookup"><span data-stu-id="a6b02-125">Ascii</span></span>
- <span data-ttu-id="a6b02-126">設置</span><span class="sxs-lookup"><span data-stu-id="a6b02-126">Default</span></span>
- <span data-ttu-id="a6b02-127">Oem</span><span class="sxs-lookup"><span data-stu-id="a6b02-127">Oem</span></span>
- <span data-ttu-id="a6b02-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="a6b02-128">BigEndianUTF32</span></span>

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6b02-129">-Path</span><span class="sxs-lookup"><span data-stu-id="a6b02-129">-Path</span></span>
<span data-ttu-id="a6b02-130">指定要修改之專案的 Data Lake Store 路徑（從根目錄 (/) 開始）。</span><span class="sxs-lookup"><span data-stu-id="a6b02-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="a6b02-131">-值</span><span class="sxs-lookup"><span data-stu-id="a6b02-131">-Value</span></span>
<span data-ttu-id="a6b02-132">指定要新增到專案中的內容。</span><span class="sxs-lookup"><span data-stu-id="a6b02-132">Specifies the content to add to the item.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a6b02-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6b02-133">CommonParameters</span></span>
<span data-ttu-id="a6b02-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6b02-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6b02-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a6b02-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6b02-136">輸入</span><span class="sxs-lookup"><span data-stu-id="a6b02-136">INPUTS</span></span>

### <span data-ttu-id="a6b02-137">System.object</span><span class="sxs-lookup"><span data-stu-id="a6b02-137">System.String</span></span>

### <span data-ttu-id="a6b02-138">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="a6b02-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="a6b02-139">System.object</span><span class="sxs-lookup"><span data-stu-id="a6b02-139">System.Object</span></span>

### <span data-ttu-id="a6b02-140">文字編碼</span><span class="sxs-lookup"><span data-stu-id="a6b02-140">System.Text.Encoding</span></span>

## <span data-ttu-id="a6b02-141">輸出</span><span class="sxs-lookup"><span data-stu-id="a6b02-141">OUTPUTS</span></span>

### <span data-ttu-id="a6b02-142">System.object</span><span class="sxs-lookup"><span data-stu-id="a6b02-142">System.Boolean</span></span>

## <span data-ttu-id="a6b02-143">筆記</span><span class="sxs-lookup"><span data-stu-id="a6b02-143">NOTES</span></span>

## <span data-ttu-id="a6b02-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6b02-144">RELATED LINKS</span></span>

[<span data-ttu-id="a6b02-145">AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="a6b02-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


