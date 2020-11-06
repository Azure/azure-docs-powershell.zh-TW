---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: d674376325c103f6e3e8e0368f0db6c64422c97b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622500"
---
# <span data-ttu-id="e1f78-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="e1f78-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="e1f78-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e1f78-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f78-103">在 Azure Data Lake 中還原已刪除的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="e1f78-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="e1f78-104">句法</span><span class="sxs-lookup"><span data-stu-id="e1f78-104">SYNTAX</span></span>

### <span data-ttu-id="e1f78-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="e1f78-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1f78-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="e1f78-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e1f78-107">說明</span><span class="sxs-lookup"><span data-stu-id="e1f78-107">DESCRIPTION</span></span>
<span data-ttu-id="e1f78-108">**Restore-AzDataLakeStoreDeletedItem** Cmdlet 會在 Data Lake store 中還原已刪除的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="e1f78-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="e1f78-109">在 [垃圾桶 retunred] 中需要 AzDataLakeStoreDeletedItem 的已刪除專案路徑。</span><span class="sxs-lookup"><span data-stu-id="e1f78-109">Requires the path of deleted item in trash retunred by Get-AzDataLakeStoreDeletedItem.</span></span>

## <span data-ttu-id="e1f78-110">示例</span><span class="sxs-lookup"><span data-stu-id="e1f78-110">EXAMPLES</span></span>

### <span data-ttu-id="e1f78-111">範例1：使用-force 選項從 Data Lake Store 還原檔案</span><span class="sxs-lookup"><span data-stu-id="e1f78-111">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
```
PS > Restore-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -Destination adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 -Type "file" -Force
PS >

### Example 2: Restore a file from Data Lake Store using user confirmation

PS > restore-azdatalakestoredeleteditem -account ml1ptrashtest -path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -destination adl://ml1ptrashtest.azuredatalake.com/test4/file_1115 -type file

Restore user data ?
From - 927e8fb1-a287-4353-b50e-3b4a39ae4088
To   - adl://ml1ptrashtest.azuredatalake.com/test4/file_1115
Type - file
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
PS >
```

## <span data-ttu-id="e1f78-112">參數</span><span class="sxs-lookup"><span data-stu-id="e1f78-112">PARAMETERS</span></span>

### <span data-ttu-id="e1f78-113">-帳戶</span><span class="sxs-lookup"><span data-stu-id="e1f78-113">-Account</span></span>
<span data-ttu-id="e1f78-114">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="e1f78-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="e1f78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f78-115">-DefaultProfile</span></span>
<span data-ttu-id="e1f78-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e1f78-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1f78-117">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="e1f78-117">-DeletedItem</span></span>
<span data-ttu-id="e1f78-118">已刪除的專案物件。</span><span class="sxs-lookup"><span data-stu-id="e1f78-118">The deleted item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f78-119">-目的地</span><span class="sxs-lookup"><span data-stu-id="e1f78-119">-Destination</span></span>
<span data-ttu-id="e1f78-120">要還原已刪除檔案或資料夾之位置的目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="e1f78-120">The destination path to where the deleted file or folder should be restored.</span></span> 

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f78-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e1f78-121">-Force</span></span>
<span data-ttu-id="e1f78-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e1f78-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f78-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1f78-123">-PassThru</span></span>
<span data-ttu-id="e1f78-124">成功時傳回布林值 true。</span><span class="sxs-lookup"><span data-stu-id="e1f78-124">Return boolean true on success.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1f78-125">-Path</span><span class="sxs-lookup"><span data-stu-id="e1f78-125">-Path</span></span>
<span data-ttu-id="e1f78-126">[垃圾桶] 中已刪除檔案或資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="e1f78-126">The path of the deleted file or folder in trash.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f78-127">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="e1f78-127">-RestoreAction</span></span>
<span data-ttu-id="e1f78-128">要採取的動作與目的名稱衝突-「複製」或「覆寫」</span><span class="sxs-lookup"><span data-stu-id="e1f78-128">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f78-129">-類型</span><span class="sxs-lookup"><span data-stu-id="e1f78-129">-Type</span></span>
<span data-ttu-id="e1f78-130">要復原的專案類型-"file" 或 "folder"</span><span class="sxs-lookup"><span data-stu-id="e1f78-130">The type of entry being restored - "file" or "folder"</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f78-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f78-131">CommonParameters</span></span>
<span data-ttu-id="e1f78-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e1f78-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f78-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e1f78-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f78-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e1f78-134">INPUTS</span></span>

### <span data-ttu-id="e1f78-135">System.object</span><span class="sxs-lookup"><span data-stu-id="e1f78-135">System.String</span></span>

## <span data-ttu-id="e1f78-136">輸出</span><span class="sxs-lookup"><span data-stu-id="e1f78-136">OUTPUTS</span></span>

### <span data-ttu-id="e1f78-137">所有</span><span class="sxs-lookup"><span data-stu-id="e1f78-137">None</span></span>

## <span data-ttu-id="e1f78-138">筆記</span><span class="sxs-lookup"><span data-stu-id="e1f78-138">NOTES</span></span>

## <span data-ttu-id="e1f78-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="e1f78-139">RELATED LINKS</span></span>

[<span data-ttu-id="e1f78-140">AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="e1f78-140">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)