---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 3cf411e75e2a3ec430f13354015d5b6e271c840c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278415"
---
# <span data-ttu-id="f057c-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="f057c-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="f057c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f057c-102">SYNOPSIS</span></span>
<span data-ttu-id="f057c-103">將內容新增至 Data Lake Store 中的專案。</span><span class="sxs-lookup"><span data-stu-id="f057c-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="f057c-104">句法</span><span class="sxs-lookup"><span data-stu-id="f057c-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f057c-105">說明</span><span class="sxs-lookup"><span data-stu-id="f057c-105">DESCRIPTION</span></span>
<span data-ttu-id="f057c-106">**載入 AzDataLakeStoreItemContent** Cmdlet 會將內容新增至 Azure Data Lake store 中的專案。</span><span class="sxs-lookup"><span data-stu-id="f057c-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="f057c-107">示例</span><span class="sxs-lookup"><span data-stu-id="f057c-107">EXAMPLES</span></span>

### <span data-ttu-id="f057c-108">範例1：新增內容至檔案</span><span class="sxs-lookup"><span data-stu-id="f057c-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="f057c-109">這個命令會將內容新增至檔案 myFile.txt。</span><span class="sxs-lookup"><span data-stu-id="f057c-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="f057c-110">參數</span><span class="sxs-lookup"><span data-stu-id="f057c-110">PARAMETERS</span></span>

### <span data-ttu-id="f057c-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="f057c-111">-Account</span></span>
<span data-ttu-id="f057c-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="f057c-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f057c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f057c-113">-DefaultProfile</span></span>
<span data-ttu-id="f057c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f057c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f057c-115">編碼</span><span class="sxs-lookup"><span data-stu-id="f057c-115">-Encoding</span></span>
<span data-ttu-id="f057c-116">指定要建立之專案的編碼。</span><span class="sxs-lookup"><span data-stu-id="f057c-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="f057c-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f057c-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f057c-118">清楚</span><span class="sxs-lookup"><span data-stu-id="f057c-118">Unknown</span></span>
- <span data-ttu-id="f057c-119">字串</span><span class="sxs-lookup"><span data-stu-id="f057c-119">String</span></span>
- <span data-ttu-id="f057c-120">消除</span><span class="sxs-lookup"><span data-stu-id="f057c-120">Unicode</span></span>
- <span data-ttu-id="f057c-121">位元組</span><span class="sxs-lookup"><span data-stu-id="f057c-121">Byte</span></span>
- <span data-ttu-id="f057c-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="f057c-122">BigEndianUnicode</span></span>
- <span data-ttu-id="f057c-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="f057c-123">UTF8</span></span>
- <span data-ttu-id="f057c-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="f057c-124">UTF7</span></span>
- <span data-ttu-id="f057c-125">Ascii</span><span class="sxs-lookup"><span data-stu-id="f057c-125">Ascii</span></span>
- <span data-ttu-id="f057c-126">設置</span><span class="sxs-lookup"><span data-stu-id="f057c-126">Default</span></span>
- <span data-ttu-id="f057c-127">Oem</span><span class="sxs-lookup"><span data-stu-id="f057c-127">Oem</span></span>
- <span data-ttu-id="f057c-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="f057c-128">BigEndianUTF32</span></span>

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

### <span data-ttu-id="f057c-129">-Path</span><span class="sxs-lookup"><span data-stu-id="f057c-129">-Path</span></span>
<span data-ttu-id="f057c-130">指定要修改之專案的 Data Lake Store 路徑（從根目錄 (/) 開始）。</span><span class="sxs-lookup"><span data-stu-id="f057c-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f057c-131">-值</span><span class="sxs-lookup"><span data-stu-id="f057c-131">-Value</span></span>
<span data-ttu-id="f057c-132">指定要新增到專案中的內容。</span><span class="sxs-lookup"><span data-stu-id="f057c-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="f057c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f057c-133">CommonParameters</span></span>
<span data-ttu-id="f057c-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f057c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f057c-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f057c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f057c-136">輸入</span><span class="sxs-lookup"><span data-stu-id="f057c-136">INPUTS</span></span>

### <span data-ttu-id="f057c-137">System.object</span><span class="sxs-lookup"><span data-stu-id="f057c-137">System.String</span></span>

### <span data-ttu-id="f057c-138">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="f057c-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="f057c-139">System.object</span><span class="sxs-lookup"><span data-stu-id="f057c-139">System.Object</span></span>

### <span data-ttu-id="f057c-140">文字編碼</span><span class="sxs-lookup"><span data-stu-id="f057c-140">System.Text.Encoding</span></span>

## <span data-ttu-id="f057c-141">輸出</span><span class="sxs-lookup"><span data-stu-id="f057c-141">OUTPUTS</span></span>

### <span data-ttu-id="f057c-142">System.object</span><span class="sxs-lookup"><span data-stu-id="f057c-142">System.Boolean</span></span>

## <span data-ttu-id="f057c-143">筆記</span><span class="sxs-lookup"><span data-stu-id="f057c-143">NOTES</span></span>

## <span data-ttu-id="f057c-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="f057c-144">RELATED LINKS</span></span>

[<span data-ttu-id="f057c-145">AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="f057c-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


