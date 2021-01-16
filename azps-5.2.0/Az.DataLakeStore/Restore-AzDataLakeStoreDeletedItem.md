---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 9dcc45f8f082ce59a6082ad71c2084c5df10064c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98279238"
---
# <span data-ttu-id="5c8d2-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="5c8d2-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="5c8d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5c8d2-102">SYNOPSIS</span></span>
<span data-ttu-id="5c8d2-103">在 Azure Data Lake 中還原已刪除的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="5c8d2-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="5c8d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="5c8d2-104">SYNTAX</span></span>

### <span data-ttu-id="5c8d2-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="5c8d2-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5c8d2-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5c8d2-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c8d2-107">說明</span><span class="sxs-lookup"><span data-stu-id="5c8d2-107">DESCRIPTION</span></span>
<span data-ttu-id="5c8d2-108">**Restore-AzDataLakeStoreDeletedItem** Cmdlet 會在 Data Lake store 中還原已刪除的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="5c8d2-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="5c8d2-109">需要由 AzDataLakeStoreDeletedItem 傳回的 [垃圾桶] 中的已刪除專案路徑。</span><span class="sxs-lookup"><span data-stu-id="5c8d2-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>
<span data-ttu-id="5c8d2-110">注意： [未完成的檔案] 是最佳的操作。</span><span class="sxs-lookup"><span data-stu-id="5c8d2-110">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="5c8d2-111">在刪除檔案後，就不會保證檔案可以還原。</span><span class="sxs-lookup"><span data-stu-id="5c8d2-111">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="5c8d2-112">此 API 的使用是透過 whitelisting 啟用。</span><span class="sxs-lookup"><span data-stu-id="5c8d2-112">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="5c8d2-113">如果您的 ADL 帳戶未列入白名單，則使用這個 api 將會拋出未實現的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="5c8d2-113">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="5c8d2-114">如需進一步的資訊和協助，請聯絡 Microsoft 支援。</span><span class="sxs-lookup"><span data-stu-id="5c8d2-114">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="5c8d2-115">示例</span><span class="sxs-lookup"><span data-stu-id="5c8d2-115">EXAMPLES</span></span>

### <span data-ttu-id="5c8d2-116">範例1：使用-force 選項從 Data Lake Store 還原檔案</span><span class="sxs-lookup"><span data-stu-id="5c8d2-116">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
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

## <span data-ttu-id="5c8d2-117">參數</span><span class="sxs-lookup"><span data-stu-id="5c8d2-117">PARAMETERS</span></span>

### <span data-ttu-id="5c8d2-118">-帳戶</span><span class="sxs-lookup"><span data-stu-id="5c8d2-118">-Account</span></span>
<span data-ttu-id="5c8d2-119">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c8d2-119">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5c8d2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c8d2-120">-DefaultProfile</span></span>
<span data-ttu-id="5c8d2-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c8d2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c8d2-122">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="5c8d2-122">-DeletedItem</span></span>
<span data-ttu-id="5c8d2-123">已刪除的專案物件。</span><span class="sxs-lookup"><span data-stu-id="5c8d2-123">The deleted item object.</span></span>

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

### <span data-ttu-id="5c8d2-124">-目的地</span><span class="sxs-lookup"><span data-stu-id="5c8d2-124">-Destination</span></span>
<span data-ttu-id="5c8d2-125">要還原已刪除檔案或資料夾之位置的目的地路徑。</span><span class="sxs-lookup"><span data-stu-id="5c8d2-125">The destination path to where the deleted file or folder should be restored.</span></span> 

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

### <span data-ttu-id="5c8d2-126">-Force</span><span class="sxs-lookup"><span data-stu-id="5c8d2-126">-Force</span></span>
<span data-ttu-id="5c8d2-127">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="5c8d2-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5c8d2-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c8d2-128">-PassThru</span></span>
<span data-ttu-id="5c8d2-129">成功時傳回布林值 true。</span><span class="sxs-lookup"><span data-stu-id="5c8d2-129">Return boolean true on success.</span></span>

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

### <span data-ttu-id="5c8d2-130">-Path</span><span class="sxs-lookup"><span data-stu-id="5c8d2-130">-Path</span></span>
<span data-ttu-id="5c8d2-131">[垃圾桶] 中已刪除檔案或資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="5c8d2-131">The path of the deleted file or folder in trash.</span></span>

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

### <span data-ttu-id="5c8d2-132">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="5c8d2-132">-RestoreAction</span></span>
<span data-ttu-id="5c8d2-133">要採取的動作與目的名稱衝突-「複製」或「覆寫」</span><span class="sxs-lookup"><span data-stu-id="5c8d2-133">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

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

### <span data-ttu-id="5c8d2-134">-類型</span><span class="sxs-lookup"><span data-stu-id="5c8d2-134">-Type</span></span>
<span data-ttu-id="5c8d2-135">要復原的專案類型-"file" 或 "folder"</span><span class="sxs-lookup"><span data-stu-id="5c8d2-135">The type of entry being restored - "file" or "folder"</span></span>

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

### <span data-ttu-id="5c8d2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c8d2-136">CommonParameters</span></span>
<span data-ttu-id="5c8d2-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5c8d2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c8d2-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5c8d2-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c8d2-139">輸入</span><span class="sxs-lookup"><span data-stu-id="5c8d2-139">INPUTS</span></span>

### <span data-ttu-id="5c8d2-140">System.object</span><span class="sxs-lookup"><span data-stu-id="5c8d2-140">System.String</span></span>

## <span data-ttu-id="5c8d2-141">輸出</span><span class="sxs-lookup"><span data-stu-id="5c8d2-141">OUTPUTS</span></span>

### <span data-ttu-id="5c8d2-142">所有</span><span class="sxs-lookup"><span data-stu-id="5c8d2-142">None</span></span>

## <span data-ttu-id="5c8d2-143">筆記</span><span class="sxs-lookup"><span data-stu-id="5c8d2-143">NOTES</span></span>

## <span data-ttu-id="5c8d2-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c8d2-144">RELATED LINKS</span></span>

[<span data-ttu-id="5c8d2-145">AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="5c8d2-145">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)