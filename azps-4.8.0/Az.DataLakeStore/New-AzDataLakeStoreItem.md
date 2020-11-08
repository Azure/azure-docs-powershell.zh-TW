---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: ab752ec2201c9b64a9656153f29a947b7a722819
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127062"
---
# <span data-ttu-id="f7532-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f7532-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="f7532-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7532-102">SYNOPSIS</span></span>
<span data-ttu-id="f7532-103">在 Data Lake Store 中建立新的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="f7532-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f7532-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7532-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7532-105">說明</span><span class="sxs-lookup"><span data-stu-id="f7532-105">DESCRIPTION</span></span>
<span data-ttu-id="f7532-106">**新的-AzDataLakeStoreItem** Cmdlet 會在 Data Lake store 中建立新的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="f7532-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f7532-107">示例</span><span class="sxs-lookup"><span data-stu-id="f7532-107">EXAMPLES</span></span>

### <span data-ttu-id="f7532-108">範例1：建立新的檔案和新資料夾</span><span class="sxs-lookup"><span data-stu-id="f7532-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="f7532-109">第一個命令會針對指定的帳號建立檔案 NewFile.txt。</span><span class="sxs-lookup"><span data-stu-id="f7532-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="f7532-110">第二個命令會在根資料夾中建立資料夾 NewFolder。</span><span class="sxs-lookup"><span data-stu-id="f7532-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="f7532-111">參數</span><span class="sxs-lookup"><span data-stu-id="f7532-111">PARAMETERS</span></span>

### <span data-ttu-id="f7532-112">-帳戶</span><span class="sxs-lookup"><span data-stu-id="f7532-112">-Account</span></span>
<span data-ttu-id="f7532-113">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7532-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f7532-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7532-114">-DefaultProfile</span></span>
<span data-ttu-id="f7532-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7532-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7532-116">編碼</span><span class="sxs-lookup"><span data-stu-id="f7532-116">-Encoding</span></span>
<span data-ttu-id="f7532-117">指定要建立之專案的編碼。</span><span class="sxs-lookup"><span data-stu-id="f7532-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="f7532-118">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="f7532-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f7532-119">清楚</span><span class="sxs-lookup"><span data-stu-id="f7532-119">Unknown</span></span>
- <span data-ttu-id="f7532-120">字串</span><span class="sxs-lookup"><span data-stu-id="f7532-120">String</span></span>
- <span data-ttu-id="f7532-121">消除</span><span class="sxs-lookup"><span data-stu-id="f7532-121">Unicode</span></span>
- <span data-ttu-id="f7532-122">位元組</span><span class="sxs-lookup"><span data-stu-id="f7532-122">Byte</span></span>
- <span data-ttu-id="f7532-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="f7532-123">BigEndianUnicode</span></span>
- <span data-ttu-id="f7532-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="f7532-124">UTF8</span></span>
- <span data-ttu-id="f7532-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="f7532-125">UTF7</span></span>
- <span data-ttu-id="f7532-126">Ascii</span><span class="sxs-lookup"><span data-stu-id="f7532-126">Ascii</span></span>
- <span data-ttu-id="f7532-127">設置</span><span class="sxs-lookup"><span data-stu-id="f7532-127">Default</span></span>
- <span data-ttu-id="f7532-128">Oem</span><span class="sxs-lookup"><span data-stu-id="f7532-128">Oem</span></span>
- <span data-ttu-id="f7532-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="f7532-129">BigEndianUTF32</span></span>

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

### <span data-ttu-id="f7532-130">-資料夾</span><span class="sxs-lookup"><span data-stu-id="f7532-130">-Folder</span></span>
<span data-ttu-id="f7532-131">指示這個作業會建立一個資料夾。</span><span class="sxs-lookup"><span data-stu-id="f7532-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="f7532-132">-Force</span><span class="sxs-lookup"><span data-stu-id="f7532-132">-Force</span></span>
<span data-ttu-id="f7532-133">表示此操作可以覆寫目標專案（如果它已經存在的話）。</span><span class="sxs-lookup"><span data-stu-id="f7532-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="f7532-134">-Path</span><span class="sxs-lookup"><span data-stu-id="f7532-134">-Path</span></span>
<span data-ttu-id="f7532-135">指定要建立之專案的資料 Lake Store 路徑，從根目錄 (/) 開始。</span><span class="sxs-lookup"><span data-stu-id="f7532-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f7532-136">-值</span><span class="sxs-lookup"><span data-stu-id="f7532-136">-Value</span></span>
<span data-ttu-id="f7532-137">指定要新增到您所建立之專案的內容。</span><span class="sxs-lookup"><span data-stu-id="f7532-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="f7532-138">-確認</span><span class="sxs-lookup"><span data-stu-id="f7532-138">-Confirm</span></span>
<span data-ttu-id="f7532-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f7532-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7532-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7532-140">-WhatIf</span></span>
<span data-ttu-id="f7532-141">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f7532-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7532-142">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7532-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7532-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7532-143">CommonParameters</span></span>
<span data-ttu-id="f7532-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7532-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7532-145">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f7532-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7532-146">輸入</span><span class="sxs-lookup"><span data-stu-id="f7532-146">INPUTS</span></span>

### <span data-ttu-id="f7532-147">System.object</span><span class="sxs-lookup"><span data-stu-id="f7532-147">System.String</span></span>

### <span data-ttu-id="f7532-148">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="f7532-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="f7532-149">System.object</span><span class="sxs-lookup"><span data-stu-id="f7532-149">System.Object</span></span>

### <span data-ttu-id="f7532-150">文字編碼</span><span class="sxs-lookup"><span data-stu-id="f7532-150">System.Text.Encoding</span></span>

### <span data-ttu-id="f7532-151">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="f7532-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f7532-152">輸出</span><span class="sxs-lookup"><span data-stu-id="f7532-152">OUTPUTS</span></span>

### <span data-ttu-id="f7532-153">System.object</span><span class="sxs-lookup"><span data-stu-id="f7532-153">System.String</span></span>

## <span data-ttu-id="f7532-154">筆記</span><span class="sxs-lookup"><span data-stu-id="f7532-154">NOTES</span></span>

## <span data-ttu-id="f7532-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7532-155">RELATED LINKS</span></span>

[<span data-ttu-id="f7532-156">AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f7532-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="f7532-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f7532-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="f7532-158">匯入-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f7532-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="f7532-159">新-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f7532-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="f7532-160">移除-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f7532-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="f7532-161">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f7532-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


