---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 2dc2d18fc0bc09fd7e9477115f4212aeb2452bbb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446264"
---
# <span data-ttu-id="cedb1-101">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cedb1-101">New-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="cedb1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cedb1-102">SYNOPSIS</span></span>
<span data-ttu-id="cedb1-103">在 Data Lake Store 中建立新的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="cedb1-103">Creates a new file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cedb1-104">句法</span><span class="sxs-lookup"><span data-stu-id="cedb1-104">SYNTAX</span></span>

```
New-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cedb1-105">說明</span><span class="sxs-lookup"><span data-stu-id="cedb1-105">DESCRIPTION</span></span>
<span data-ttu-id="cedb1-106">**新的-AzureRmDataLakeStoreItem** Cmdlet 會在 Data Lake store 中建立新的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="cedb1-106">The **New-AzureRmDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="cedb1-107">示例</span><span class="sxs-lookup"><span data-stu-id="cedb1-107">EXAMPLES</span></span>

### <span data-ttu-id="cedb1-108">範例1：建立新的檔案和新資料夾</span><span class="sxs-lookup"><span data-stu-id="cedb1-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="cedb1-109">第一個命令會針對指定的帳號建立檔案 NewFile.txt。</span><span class="sxs-lookup"><span data-stu-id="cedb1-109">The first command creates the file NewFile.txt for the specified account.</span></span>

<span data-ttu-id="cedb1-110">第二個命令會在根資料夾中建立資料夾 NewFolder。</span><span class="sxs-lookup"><span data-stu-id="cedb1-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="cedb1-111">參數</span><span class="sxs-lookup"><span data-stu-id="cedb1-111">PARAMETERS</span></span>

### <span data-ttu-id="cedb1-112">-帳戶</span><span class="sxs-lookup"><span data-stu-id="cedb1-112">-Account</span></span>
<span data-ttu-id="cedb1-113">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="cedb1-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="cedb1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cedb1-114">-DefaultProfile</span></span>
<span data-ttu-id="cedb1-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cedb1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cedb1-116">編碼</span><span class="sxs-lookup"><span data-stu-id="cedb1-116">-Encoding</span></span>
<span data-ttu-id="cedb1-117">指定要建立之專案的編碼。</span><span class="sxs-lookup"><span data-stu-id="cedb1-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="cedb1-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="cedb1-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cedb1-119">清楚</span><span class="sxs-lookup"><span data-stu-id="cedb1-119">Unknown</span></span>
- <span data-ttu-id="cedb1-120">字串</span><span class="sxs-lookup"><span data-stu-id="cedb1-120">String</span></span>
- <span data-ttu-id="cedb1-121">消除</span><span class="sxs-lookup"><span data-stu-id="cedb1-121">Unicode</span></span>
- <span data-ttu-id="cedb1-122">位元組</span><span class="sxs-lookup"><span data-stu-id="cedb1-122">Byte</span></span>
- <span data-ttu-id="cedb1-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="cedb1-123">BigEndianUnicode</span></span>
- <span data-ttu-id="cedb1-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="cedb1-124">UTF8</span></span>
- <span data-ttu-id="cedb1-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="cedb1-125">UTF7</span></span>
- <span data-ttu-id="cedb1-126">Ascii</span><span class="sxs-lookup"><span data-stu-id="cedb1-126">Ascii</span></span>
- <span data-ttu-id="cedb1-127">設置</span><span class="sxs-lookup"><span data-stu-id="cedb1-127">Default</span></span>
- <span data-ttu-id="cedb1-128">Oem</span><span class="sxs-lookup"><span data-stu-id="cedb1-128">Oem</span></span>
- <span data-ttu-id="cedb1-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="cedb1-129">BigEndianUTF32</span></span>

```yaml
Type: FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cedb1-130">-資料夾</span><span class="sxs-lookup"><span data-stu-id="cedb1-130">-Folder</span></span>
<span data-ttu-id="cedb1-131">指示這個作業會建立一個資料夾。</span><span class="sxs-lookup"><span data-stu-id="cedb1-131">Indicates that this operation creates a folder.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cedb1-132">-Force</span><span class="sxs-lookup"><span data-stu-id="cedb1-132">-Force</span></span>
<span data-ttu-id="cedb1-133">表示此操作可以覆寫目標專案（如果它已經存在的話）。</span><span class="sxs-lookup"><span data-stu-id="cedb1-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cedb1-134">-Path</span><span class="sxs-lookup"><span data-stu-id="cedb1-134">-Path</span></span>
<span data-ttu-id="cedb1-135">指定要建立之專案的資料 Lake Store 路徑，從根目錄 (/) 開始。</span><span class="sxs-lookup"><span data-stu-id="cedb1-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="cedb1-136">-值</span><span class="sxs-lookup"><span data-stu-id="cedb1-136">-Value</span></span>
<span data-ttu-id="cedb1-137">指定要新增到您所建立之專案的內容。</span><span class="sxs-lookup"><span data-stu-id="cedb1-137">Specifies the content to add to the item you create.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cedb1-138">-確認</span><span class="sxs-lookup"><span data-stu-id="cedb1-138">-Confirm</span></span>
<span data-ttu-id="cedb1-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cedb1-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cedb1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cedb1-140">-WhatIf</span></span>
<span data-ttu-id="cedb1-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cedb1-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cedb1-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cedb1-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cedb1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cedb1-143">CommonParameters</span></span>
<span data-ttu-id="cedb1-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cedb1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cedb1-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cedb1-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cedb1-146">輸入</span><span class="sxs-lookup"><span data-stu-id="cedb1-146">INPUTS</span></span>

### <span data-ttu-id="cedb1-147">面向</span><span class="sxs-lookup"><span data-stu-id="cedb1-147">Object</span></span>
<span data-ttu-id="cedb1-148">形參 "Value" 接受管線中 "Object" 類型的值</span><span class="sxs-lookup"><span data-stu-id="cedb1-148">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="cedb1-149">輸出</span><span class="sxs-lookup"><span data-stu-id="cedb1-149">OUTPUTS</span></span>

### <span data-ttu-id="cedb1-150">字串</span><span class="sxs-lookup"><span data-stu-id="cedb1-150">string</span></span>
<span data-ttu-id="cedb1-151">已建立的檔案或資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="cedb1-151">The full path to the created file or folder.</span></span>

## <span data-ttu-id="cedb1-152">筆記</span><span class="sxs-lookup"><span data-stu-id="cedb1-152">NOTES</span></span>

## <span data-ttu-id="cedb1-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="cedb1-153">RELATED LINKS</span></span>

[<span data-ttu-id="cedb1-154">AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cedb1-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="cedb1-155">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cedb1-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="cedb1-156">匯入-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cedb1-156">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="cedb1-157">新-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cedb1-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="cedb1-158">移除-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cedb1-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="cedb1-159">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cedb1-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


