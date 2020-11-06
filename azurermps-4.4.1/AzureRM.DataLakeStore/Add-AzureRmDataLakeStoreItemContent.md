---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 4ce79044793bbecc76d72fab015166ccc3d8fba6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446829"
---
# <span data-ttu-id="347a9-101">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="347a9-101">Add-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="347a9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="347a9-102">SYNOPSIS</span></span>
<span data-ttu-id="347a9-103">將內容新增至 Data Lake Store 中的專案。</span><span class="sxs-lookup"><span data-stu-id="347a9-103">Adds content to an item in a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="347a9-104">句法</span><span class="sxs-lookup"><span data-stu-id="347a9-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="347a9-105">說明</span><span class="sxs-lookup"><span data-stu-id="347a9-105">DESCRIPTION</span></span>
<span data-ttu-id="347a9-106">**載入 AzureRmDataLakeStoreItemContent** Cmdlet 會將內容新增至 Azure Data Lake store 中的專案。</span><span class="sxs-lookup"><span data-stu-id="347a9-106">The **Add-AzureRmDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="347a9-107">示例</span><span class="sxs-lookup"><span data-stu-id="347a9-107">EXAMPLES</span></span>

### <span data-ttu-id="347a9-108">範例1：新增內容至檔案</span><span class="sxs-lookup"><span data-stu-id="347a9-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzureRmDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="347a9-109">這個命令會將內容新增至檔案 myFile.txt。</span><span class="sxs-lookup"><span data-stu-id="347a9-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="347a9-110">參數</span><span class="sxs-lookup"><span data-stu-id="347a9-110">PARAMETERS</span></span>

### <span data-ttu-id="347a9-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="347a9-111">-Account</span></span>
<span data-ttu-id="347a9-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="347a9-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="347a9-113">編碼</span><span class="sxs-lookup"><span data-stu-id="347a9-113">-Encoding</span></span>
<span data-ttu-id="347a9-114">指定要建立之專案的編碼。</span><span class="sxs-lookup"><span data-stu-id="347a9-114">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="347a9-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="347a9-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="347a9-116">清楚</span><span class="sxs-lookup"><span data-stu-id="347a9-116">Unknown</span></span>
- <span data-ttu-id="347a9-117">字串</span><span class="sxs-lookup"><span data-stu-id="347a9-117">String</span></span>
- <span data-ttu-id="347a9-118">消除</span><span class="sxs-lookup"><span data-stu-id="347a9-118">Unicode</span></span>
- <span data-ttu-id="347a9-119">位元組</span><span class="sxs-lookup"><span data-stu-id="347a9-119">Byte</span></span>
- <span data-ttu-id="347a9-120">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="347a9-120">BigEndianUnicode</span></span>
- <span data-ttu-id="347a9-121">UTF8</span><span class="sxs-lookup"><span data-stu-id="347a9-121">UTF8</span></span>
- <span data-ttu-id="347a9-122">UTF7</span><span class="sxs-lookup"><span data-stu-id="347a9-122">UTF7</span></span>
- <span data-ttu-id="347a9-123">Ascii</span><span class="sxs-lookup"><span data-stu-id="347a9-123">Ascii</span></span>
- <span data-ttu-id="347a9-124">設置</span><span class="sxs-lookup"><span data-stu-id="347a9-124">Default</span></span>
- <span data-ttu-id="347a9-125">Oem</span><span class="sxs-lookup"><span data-stu-id="347a9-125">Oem</span></span>
- <span data-ttu-id="347a9-126">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="347a9-126">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.PowerShell.Commands.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="347a9-127">-Path</span><span class="sxs-lookup"><span data-stu-id="347a9-127">-Path</span></span>
<span data-ttu-id="347a9-128">指定要修改之專案的 Data Lake Store 路徑（從根目錄 (/) 開始）。</span><span class="sxs-lookup"><span data-stu-id="347a9-128">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="347a9-129">-值</span><span class="sxs-lookup"><span data-stu-id="347a9-129">-Value</span></span>
<span data-ttu-id="347a9-130">指定要新增到專案中的內容。</span><span class="sxs-lookup"><span data-stu-id="347a9-130">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="347a9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="347a9-131">-DefaultProfile</span></span>
<span data-ttu-id="347a9-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="347a9-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="347a9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="347a9-133">CommonParameters</span></span>
<span data-ttu-id="347a9-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="347a9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="347a9-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="347a9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="347a9-136">輸入</span><span class="sxs-lookup"><span data-stu-id="347a9-136">INPUTS</span></span>

### <span data-ttu-id="347a9-137">面向</span><span class="sxs-lookup"><span data-stu-id="347a9-137">Object</span></span>
<span data-ttu-id="347a9-138">形參 "Value" 接受管線中 "Object" 類型的值</span><span class="sxs-lookup"><span data-stu-id="347a9-138">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="347a9-139">輸出</span><span class="sxs-lookup"><span data-stu-id="347a9-139">OUTPUTS</span></span>

### <span data-ttu-id="347a9-140">bool</span><span class="sxs-lookup"><span data-stu-id="347a9-140">bool</span></span>
<span data-ttu-id="347a9-141">成功時，傳回 true。</span><span class="sxs-lookup"><span data-stu-id="347a9-141">Returns true on success.</span></span>

## <span data-ttu-id="347a9-142">筆記</span><span class="sxs-lookup"><span data-stu-id="347a9-142">NOTES</span></span>

## <span data-ttu-id="347a9-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="347a9-143">RELATED LINKS</span></span>

[<span data-ttu-id="347a9-144">AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="347a9-144">Get-AzureRmDataLakeStoreItemContent</span></span>](./Get-AzureRmDataLakeStoreItemContent.md)


