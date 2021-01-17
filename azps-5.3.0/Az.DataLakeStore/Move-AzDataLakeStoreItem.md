---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: e8e90b6cca2808bbf2caee69ebef5582ed0f8c5b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434813"
---
# <span data-ttu-id="e6eb9-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6eb9-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="e6eb9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e6eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="e6eb9-103">移動或重新命名 Data Lake Store 中的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="e6eb9-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e6eb9-104">句法</span><span class="sxs-lookup"><span data-stu-id="e6eb9-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6eb9-105">說明</span><span class="sxs-lookup"><span data-stu-id="e6eb9-105">DESCRIPTION</span></span>
<span data-ttu-id="e6eb9-106">**AzDataLakeStoreItem** Cmdlet 會移動或重新命名 Data Lake store 中的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="e6eb9-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e6eb9-107">示例</span><span class="sxs-lookup"><span data-stu-id="e6eb9-107">EXAMPLES</span></span>

### <span data-ttu-id="e6eb9-108">範例1：移動及重新命名專案</span><span class="sxs-lookup"><span data-stu-id="e6eb9-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="e6eb9-109">這個命令會將 File.txt 的專案重新命名為 RenamedFile.txt，然後將它移到不同的資料夾。</span><span class="sxs-lookup"><span data-stu-id="e6eb9-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="e6eb9-110">參數</span><span class="sxs-lookup"><span data-stu-id="e6eb9-110">PARAMETERS</span></span>

### <span data-ttu-id="e6eb9-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="e6eb9-111">-Account</span></span>
<span data-ttu-id="e6eb9-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e6eb9-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="e6eb9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6eb9-113">-DefaultProfile</span></span>
<span data-ttu-id="e6eb9-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e6eb9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6eb9-115">-目的地</span><span class="sxs-lookup"><span data-stu-id="e6eb9-115">-Destination</span></span>
<span data-ttu-id="e6eb9-116">指定要將專案移到哪個資料 Lake Store 路徑，從根目錄 (/) 開始。</span><span class="sxs-lookup"><span data-stu-id="e6eb9-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6eb9-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e6eb9-117">-Force</span></span>
<span data-ttu-id="e6eb9-118">表示此操作可以覆寫目標檔案（如果該檔案已經存在的話）。</span><span class="sxs-lookup"><span data-stu-id="e6eb9-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="e6eb9-119">-Path</span><span class="sxs-lookup"><span data-stu-id="e6eb9-119">-Path</span></span>
<span data-ttu-id="e6eb9-120">指定要移動或重新命名之專案的 Data Lake Store 路徑（從根目錄 (/) 開始）。</span><span class="sxs-lookup"><span data-stu-id="e6eb9-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="e6eb9-121">-確認</span><span class="sxs-lookup"><span data-stu-id="e6eb9-121">-Confirm</span></span>
<span data-ttu-id="e6eb9-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e6eb9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6eb9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6eb9-123">-WhatIf</span></span>
<span data-ttu-id="e6eb9-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e6eb9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6eb9-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e6eb9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6eb9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6eb9-126">CommonParameters</span></span>
<span data-ttu-id="e6eb9-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e6eb9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6eb9-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e6eb9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6eb9-129">輸入</span><span class="sxs-lookup"><span data-stu-id="e6eb9-129">INPUTS</span></span>

### <span data-ttu-id="e6eb9-130">System.object</span><span class="sxs-lookup"><span data-stu-id="e6eb9-130">System.String</span></span>

### <span data-ttu-id="e6eb9-131">DataLakeStorePathInstance 中的 DataLakeStore。</span><span class="sxs-lookup"><span data-stu-id="e6eb9-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="e6eb9-132">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="e6eb9-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e6eb9-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e6eb9-133">OUTPUTS</span></span>

### <span data-ttu-id="e6eb9-134">System.object</span><span class="sxs-lookup"><span data-stu-id="e6eb9-134">System.String</span></span>

## <span data-ttu-id="e6eb9-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e6eb9-135">NOTES</span></span>

## <span data-ttu-id="e6eb9-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e6eb9-136">RELATED LINKS</span></span>

[<span data-ttu-id="e6eb9-137">AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6eb9-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="e6eb9-138">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6eb9-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="e6eb9-139">匯入-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6eb9-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="e6eb9-140">新-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6eb9-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="e6eb9-141">移除-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6eb9-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="e6eb9-142">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6eb9-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


