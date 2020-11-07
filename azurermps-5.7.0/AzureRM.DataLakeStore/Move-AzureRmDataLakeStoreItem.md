---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/move-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 5e6fb437833db3f4278335f67693d084c2d6d95b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624096"
---
# <span data-ttu-id="60a5c-101">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="60a5c-101">Move-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="60a5c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="60a5c-102">SYNOPSIS</span></span>
<span data-ttu-id="60a5c-103">移動或重新命名 Data Lake Store 中的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="60a5c-103">Moves or renames a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60a5c-104">句法</span><span class="sxs-lookup"><span data-stu-id="60a5c-104">SYNTAX</span></span>

```
Move-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60a5c-105">說明</span><span class="sxs-lookup"><span data-stu-id="60a5c-105">DESCRIPTION</span></span>
<span data-ttu-id="60a5c-106">**AzureRmDataLakeStoreItem** Cmdlet 會移動或重新命名 Data Lake store 中的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="60a5c-106">The **Move-AzureRmDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="60a5c-107">示例</span><span class="sxs-lookup"><span data-stu-id="60a5c-107">EXAMPLES</span></span>

### <span data-ttu-id="60a5c-108">範例1：移動及重新命名專案</span><span class="sxs-lookup"><span data-stu-id="60a5c-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="60a5c-109">這個命令會將 File.txt 的專案重新命名為 RenamedFile.txt，然後將它移到不同的資料夾。</span><span class="sxs-lookup"><span data-stu-id="60a5c-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="60a5c-110">參數</span><span class="sxs-lookup"><span data-stu-id="60a5c-110">PARAMETERS</span></span>

### <span data-ttu-id="60a5c-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="60a5c-111">-Account</span></span>
<span data-ttu-id="60a5c-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="60a5c-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="60a5c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a5c-113">-DefaultProfile</span></span>
<span data-ttu-id="60a5c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="60a5c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60a5c-115">-目的地</span><span class="sxs-lookup"><span data-stu-id="60a5c-115">-Destination</span></span>
<span data-ttu-id="60a5c-116">指定要將專案移到哪個資料 Lake Store 路徑，從根目錄 (/) 開始。</span><span class="sxs-lookup"><span data-stu-id="60a5c-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60a5c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="60a5c-117">-Force</span></span>
<span data-ttu-id="60a5c-118">表示此操作可以覆寫目標檔案（如果該檔案已經存在的話）。</span><span class="sxs-lookup"><span data-stu-id="60a5c-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="60a5c-119">-Path</span><span class="sxs-lookup"><span data-stu-id="60a5c-119">-Path</span></span>
<span data-ttu-id="60a5c-120">指定要移動或重新命名之專案的 Data Lake Store 路徑（從根目錄 (/) 開始）。</span><span class="sxs-lookup"><span data-stu-id="60a5c-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="60a5c-121">-確認</span><span class="sxs-lookup"><span data-stu-id="60a5c-121">-Confirm</span></span>
<span data-ttu-id="60a5c-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="60a5c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60a5c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60a5c-123">-WhatIf</span></span>
<span data-ttu-id="60a5c-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="60a5c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60a5c-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="60a5c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60a5c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a5c-126">CommonParameters</span></span>
<span data-ttu-id="60a5c-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="60a5c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a5c-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="60a5c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a5c-129">輸入</span><span class="sxs-lookup"><span data-stu-id="60a5c-129">INPUTS</span></span>

### <span data-ttu-id="60a5c-130">所有</span><span class="sxs-lookup"><span data-stu-id="60a5c-130">None</span></span>
<span data-ttu-id="60a5c-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="60a5c-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="60a5c-132">輸出</span><span class="sxs-lookup"><span data-stu-id="60a5c-132">OUTPUTS</span></span>

### <span data-ttu-id="60a5c-133">字串</span><span class="sxs-lookup"><span data-stu-id="60a5c-133">string</span></span>
<span data-ttu-id="60a5c-134">已移動檔案或資料夾的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="60a5c-134">The full path to the moved file or folder.</span></span>

## <span data-ttu-id="60a5c-135">筆記</span><span class="sxs-lookup"><span data-stu-id="60a5c-135">NOTES</span></span>

## <span data-ttu-id="60a5c-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="60a5c-136">RELATED LINKS</span></span>

[<span data-ttu-id="60a5c-137">AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="60a5c-137">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="60a5c-138">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="60a5c-138">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="60a5c-139">匯入-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="60a5c-139">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="60a5c-140">新-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="60a5c-140">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="60a5c-141">移除-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="60a5c-141">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="60a5c-142">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="60a5c-142">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


