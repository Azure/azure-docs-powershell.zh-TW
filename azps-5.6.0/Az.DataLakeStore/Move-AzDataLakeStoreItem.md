---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/move-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Move-AzDataLakeStoreItem.md
ms.openlocfilehash: 7b50d78835c6e87676c1168b10ff3d119aeca20f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911710"
---
# <span data-ttu-id="387a8-101">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="387a8-101">Move-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="387a8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="387a8-102">SYNOPSIS</span></span>
<span data-ttu-id="387a8-103">在 Data Lake Store 中移動或重新命名檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="387a8-103">Moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="387a8-104">語法</span><span class="sxs-lookup"><span data-stu-id="387a8-104">SYNTAX</span></span>

```
Move-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="387a8-105">描述</span><span class="sxs-lookup"><span data-stu-id="387a8-105">DESCRIPTION</span></span>
<span data-ttu-id="387a8-106">**Move-AzDataLakeStoreItem** Cmdlet 會移動或重新命名 Data Lake Store 中的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="387a8-106">The **Move-AzDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="387a8-107">例子</span><span class="sxs-lookup"><span data-stu-id="387a8-107">EXAMPLES</span></span>

### <span data-ttu-id="387a8-108">範例 1：移動和重新命名專案</span><span class="sxs-lookup"><span data-stu-id="387a8-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="387a8-109">此命令會重新命名要File.txtRenamedFile.txt，並將其移至不同的資料夾。</span><span class="sxs-lookup"><span data-stu-id="387a8-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="387a8-110">參數</span><span class="sxs-lookup"><span data-stu-id="387a8-110">PARAMETERS</span></span>

### <span data-ttu-id="387a8-111">-帳戶</span><span class="sxs-lookup"><span data-stu-id="387a8-111">-Account</span></span>
<span data-ttu-id="387a8-112">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="387a8-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="387a8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="387a8-113">-DefaultProfile</span></span>
<span data-ttu-id="387a8-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="387a8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="387a8-115">-目的地</span><span class="sxs-lookup"><span data-stu-id="387a8-115">-Destination</span></span>
<span data-ttu-id="387a8-116">指定要移動專案的 Data Lake Store 路徑，從根目錄或 / (開始) 。</span><span class="sxs-lookup"><span data-stu-id="387a8-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="387a8-117">-強制</span><span class="sxs-lookup"><span data-stu-id="387a8-117">-Force</span></span>
<span data-ttu-id="387a8-118">表示此作業可以覆寫目標檔案 ，如果已存在。</span><span class="sxs-lookup"><span data-stu-id="387a8-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="387a8-119">-路徑</span><span class="sxs-lookup"><span data-stu-id="387a8-119">-Path</span></span>
<span data-ttu-id="387a8-120">指定要移動或重新命名之專案的 Data Lake Store 路徑，從根目錄開始 (/) 。</span><span class="sxs-lookup"><span data-stu-id="387a8-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="387a8-121">-確認</span><span class="sxs-lookup"><span data-stu-id="387a8-121">-Confirm</span></span>
<span data-ttu-id="387a8-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="387a8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="387a8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="387a8-123">-WhatIf</span></span>
<span data-ttu-id="387a8-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="387a8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="387a8-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="387a8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="387a8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="387a8-126">CommonParameters</span></span>
<span data-ttu-id="387a8-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="387a8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="387a8-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="387a8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="387a8-129">輸入</span><span class="sxs-lookup"><span data-stu-id="387a8-129">INPUTS</span></span>

### <span data-ttu-id="387a8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="387a8-130">System.String</span></span>

### <span data-ttu-id="387a8-131">Microsoft.Azure.Commands.DataLakeStore.models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="387a8-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="387a8-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="387a8-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="387a8-133">輸出</span><span class="sxs-lookup"><span data-stu-id="387a8-133">OUTPUTS</span></span>

### <span data-ttu-id="387a8-134">System.String</span><span class="sxs-lookup"><span data-stu-id="387a8-134">System.String</span></span>

## <span data-ttu-id="387a8-135">筆記</span><span class="sxs-lookup"><span data-stu-id="387a8-135">NOTES</span></span>

## <span data-ttu-id="387a8-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="387a8-136">RELATED LINKS</span></span>

[<span data-ttu-id="387a8-137">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="387a8-137">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="387a8-138">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="387a8-138">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="387a8-139">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="387a8-139">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="387a8-140">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="387a8-140">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="387a8-141">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="387a8-141">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="387a8-142">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="387a8-142">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


