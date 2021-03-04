---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: aa2fe76f221ce412c0e47f7a43b1dba551131f45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912878"
---
# <span data-ttu-id="93c37-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="93c37-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="93c37-102">簡介</span><span class="sxs-lookup"><span data-stu-id="93c37-102">SYNOPSIS</span></span>
<span data-ttu-id="93c37-103">新增內容至 Data Lake Store 中的專案。</span><span class="sxs-lookup"><span data-stu-id="93c37-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="93c37-104">語法</span><span class="sxs-lookup"><span data-stu-id="93c37-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93c37-105">描述</span><span class="sxs-lookup"><span data-stu-id="93c37-105">DESCRIPTION</span></span>
<span data-ttu-id="93c37-106">**Add-AzDataLakeStoreItemContent** Cmdlet 會將內容新增到 Azure Data Lake Store 中的專案。</span><span class="sxs-lookup"><span data-stu-id="93c37-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="93c37-107">例子</span><span class="sxs-lookup"><span data-stu-id="93c37-107">EXAMPLES</span></span>

### <span data-ttu-id="93c37-108">範例 1：新增內容至檔案</span><span class="sxs-lookup"><span data-stu-id="93c37-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="93c37-109">此命令會將內容新增到檔案myFile.txt。</span><span class="sxs-lookup"><span data-stu-id="93c37-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="93c37-110">參數</span><span class="sxs-lookup"><span data-stu-id="93c37-110">PARAMETERS</span></span>

### <span data-ttu-id="93c37-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="93c37-111">-Account</span></span>
<span data-ttu-id="93c37-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="93c37-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="93c37-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93c37-113">-DefaultProfile</span></span>
<span data-ttu-id="93c37-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="93c37-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93c37-115">-編碼</span><span class="sxs-lookup"><span data-stu-id="93c37-115">-Encoding</span></span>
<span data-ttu-id="93c37-116">指定要建立專案的編碼。</span><span class="sxs-lookup"><span data-stu-id="93c37-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="93c37-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="93c37-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="93c37-118">未知</span><span class="sxs-lookup"><span data-stu-id="93c37-118">Unknown</span></span>
- <span data-ttu-id="93c37-119">字串</span><span class="sxs-lookup"><span data-stu-id="93c37-119">String</span></span>
- <span data-ttu-id="93c37-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="93c37-120">Unicode</span></span>
- <span data-ttu-id="93c37-121">位元組</span><span class="sxs-lookup"><span data-stu-id="93c37-121">Byte</span></span>
- <span data-ttu-id="93c37-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="93c37-122">BigEndianUnicode</span></span>
- <span data-ttu-id="93c37-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="93c37-123">UTF8</span></span>
- <span data-ttu-id="93c37-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="93c37-124">UTF7</span></span>
- <span data-ttu-id="93c37-125">Ascii</span><span class="sxs-lookup"><span data-stu-id="93c37-125">Ascii</span></span>
- <span data-ttu-id="93c37-126">預設</span><span class="sxs-lookup"><span data-stu-id="93c37-126">Default</span></span>
- <span data-ttu-id="93c37-127">Oem</span><span class="sxs-lookup"><span data-stu-id="93c37-127">Oem</span></span>
- <span data-ttu-id="93c37-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="93c37-128">BigEndianUTF32</span></span>

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

### <span data-ttu-id="93c37-129">-路徑</span><span class="sxs-lookup"><span data-stu-id="93c37-129">-Path</span></span>
<span data-ttu-id="93c37-130">指定要修改之專案的 Data Lake Store 路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="93c37-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="93c37-131">-值</span><span class="sxs-lookup"><span data-stu-id="93c37-131">-Value</span></span>
<span data-ttu-id="93c37-132">指定要新加入專案的內容。</span><span class="sxs-lookup"><span data-stu-id="93c37-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="93c37-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93c37-133">CommonParameters</span></span>
<span data-ttu-id="93c37-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="93c37-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93c37-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="93c37-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93c37-136">輸入</span><span class="sxs-lookup"><span data-stu-id="93c37-136">INPUTS</span></span>

### <span data-ttu-id="93c37-137">System.String</span><span class="sxs-lookup"><span data-stu-id="93c37-137">System.String</span></span>

### <span data-ttu-id="93c37-138">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="93c37-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="93c37-139">System.Object</span><span class="sxs-lookup"><span data-stu-id="93c37-139">System.Object</span></span>

### <span data-ttu-id="93c37-140">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="93c37-140">System.Text.Encoding</span></span>

## <span data-ttu-id="93c37-141">輸出</span><span class="sxs-lookup"><span data-stu-id="93c37-141">OUTPUTS</span></span>

### <span data-ttu-id="93c37-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="93c37-142">System.Boolean</span></span>

## <span data-ttu-id="93c37-143">筆記</span><span class="sxs-lookup"><span data-stu-id="93c37-143">NOTES</span></span>

## <span data-ttu-id="93c37-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="93c37-144">RELATED LINKS</span></span>

[<span data-ttu-id="93c37-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="93c37-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


