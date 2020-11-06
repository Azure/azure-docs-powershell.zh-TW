---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a087c2f7cfd4358e137550aa2e916fa2200d2a2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453544"
---
# <span data-ttu-id="008ae-101">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="008ae-101">New-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="008ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="008ae-102">SYNOPSIS</span></span>
<span data-ttu-id="008ae-103">在 Data Lake Store 中建立新的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="008ae-103">Creates a new file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="008ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="008ae-104">SYNTAX</span></span>

```
New-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="008ae-105">說明</span><span class="sxs-lookup"><span data-stu-id="008ae-105">DESCRIPTION</span></span>
<span data-ttu-id="008ae-106">**新的-AzureRmDataLakeStoreItem** Cmdlet 會在 Data Lake store 中建立新的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="008ae-106">The **New-AzureRmDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="008ae-107">示例</span><span class="sxs-lookup"><span data-stu-id="008ae-107">EXAMPLES</span></span>

### <span data-ttu-id="008ae-108">範例1：建立新的檔案和新資料夾</span><span class="sxs-lookup"><span data-stu-id="008ae-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="008ae-109">第一個命令會針對指定的帳號建立檔案 NewFile.txt。</span><span class="sxs-lookup"><span data-stu-id="008ae-109">The first command creates the file NewFile.txt for the specified account.</span></span>

<span data-ttu-id="008ae-110">第二個命令會在根資料夾中建立資料夾 NewFolder。</span><span class="sxs-lookup"><span data-stu-id="008ae-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="008ae-111">參數</span><span class="sxs-lookup"><span data-stu-id="008ae-111">PARAMETERS</span></span>

### <span data-ttu-id="008ae-112">-帳戶</span><span class="sxs-lookup"><span data-stu-id="008ae-112">-Account</span></span>
<span data-ttu-id="008ae-113">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="008ae-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="008ae-114">編碼</span><span class="sxs-lookup"><span data-stu-id="008ae-114">-Encoding</span></span>
<span data-ttu-id="008ae-115">指定要建立之專案的編碼。</span><span class="sxs-lookup"><span data-stu-id="008ae-115">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="008ae-116">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="008ae-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="008ae-117">清楚</span><span class="sxs-lookup"><span data-stu-id="008ae-117">Unknown</span></span>
- <span data-ttu-id="008ae-118">字串</span><span class="sxs-lookup"><span data-stu-id="008ae-118">String</span></span>
- <span data-ttu-id="008ae-119">消除</span><span class="sxs-lookup"><span data-stu-id="008ae-119">Unicode</span></span>
- <span data-ttu-id="008ae-120">位元組</span><span class="sxs-lookup"><span data-stu-id="008ae-120">Byte</span></span>
- <span data-ttu-id="008ae-121">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="008ae-121">BigEndianUnicode</span></span>
- <span data-ttu-id="008ae-122">UTF8</span><span class="sxs-lookup"><span data-stu-id="008ae-122">UTF8</span></span>
- <span data-ttu-id="008ae-123">UTF7</span><span class="sxs-lookup"><span data-stu-id="008ae-123">UTF7</span></span>
- <span data-ttu-id="008ae-124">Ascii</span><span class="sxs-lookup"><span data-stu-id="008ae-124">Ascii</span></span>
- <span data-ttu-id="008ae-125">設置</span><span class="sxs-lookup"><span data-stu-id="008ae-125">Default</span></span>
- <span data-ttu-id="008ae-126">Oem</span><span class="sxs-lookup"><span data-stu-id="008ae-126">Oem</span></span>
- <span data-ttu-id="008ae-127">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="008ae-127">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.PowerShell.Commands.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="008ae-128">-資料夾</span><span class="sxs-lookup"><span data-stu-id="008ae-128">-Folder</span></span>
<span data-ttu-id="008ae-129">指示這個作業會建立一個資料夾。</span><span class="sxs-lookup"><span data-stu-id="008ae-129">Indicates that this operation creates a folder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="008ae-130">-Force</span><span class="sxs-lookup"><span data-stu-id="008ae-130">-Force</span></span>
<span data-ttu-id="008ae-131">表示此操作可以覆寫目標專案（如果它已經存在的話）。</span><span class="sxs-lookup"><span data-stu-id="008ae-131">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="008ae-132">-Path</span><span class="sxs-lookup"><span data-stu-id="008ae-132">-Path</span></span>
<span data-ttu-id="008ae-133">指定要建立之專案的資料 Lake Store 路徑，從根目錄 (/) 開始。</span><span class="sxs-lookup"><span data-stu-id="008ae-133">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="008ae-134">-值</span><span class="sxs-lookup"><span data-stu-id="008ae-134">-Value</span></span>
<span data-ttu-id="008ae-135">指定要新增到您所建立之專案的內容。</span><span class="sxs-lookup"><span data-stu-id="008ae-135">Specifies the content to add to the item you create.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="008ae-136">-確認</span><span class="sxs-lookup"><span data-stu-id="008ae-136">-Confirm</span></span>
<span data-ttu-id="008ae-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="008ae-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="008ae-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="008ae-138">-WhatIf</span></span>
<span data-ttu-id="008ae-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="008ae-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="008ae-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="008ae-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="008ae-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="008ae-141">-DefaultProfile</span></span>
<span data-ttu-id="008ae-142">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="008ae-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="008ae-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="008ae-143">CommonParameters</span></span>
<span data-ttu-id="008ae-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="008ae-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="008ae-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="008ae-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="008ae-146">輸入</span><span class="sxs-lookup"><span data-stu-id="008ae-146">INPUTS</span></span>

### <span data-ttu-id="008ae-147">面向</span><span class="sxs-lookup"><span data-stu-id="008ae-147">Object</span></span>
<span data-ttu-id="008ae-148">形參 "Value" 接受管線中 "Object" 類型的值</span><span class="sxs-lookup"><span data-stu-id="008ae-148">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="008ae-149">輸出</span><span class="sxs-lookup"><span data-stu-id="008ae-149">OUTPUTS</span></span>

### <span data-ttu-id="008ae-150">字串</span><span class="sxs-lookup"><span data-stu-id="008ae-150">string</span></span>
<span data-ttu-id="008ae-151">已建立的檔案或資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="008ae-151">The full path to the created file or folder.</span></span>

## <span data-ttu-id="008ae-152">筆記</span><span class="sxs-lookup"><span data-stu-id="008ae-152">NOTES</span></span>

## <span data-ttu-id="008ae-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="008ae-153">RELATED LINKS</span></span>

[<span data-ttu-id="008ae-154">AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="008ae-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="008ae-155">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="008ae-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="008ae-156">匯入-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="008ae-156">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="008ae-157">新-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="008ae-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="008ae-158">移除-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="008ae-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="008ae-159">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="008ae-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


