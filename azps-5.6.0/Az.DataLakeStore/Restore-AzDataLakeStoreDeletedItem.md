---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: ba8a97e96a07e63cd3b1f63c85a71291c59fdab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902978"
---
# <span data-ttu-id="a7e40-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="a7e40-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="a7e40-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a7e40-102">SYNOPSIS</span></span>
<span data-ttu-id="a7e40-103">還原 Azure Data Lake 中已刪除的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="a7e40-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="a7e40-104">語法</span><span class="sxs-lookup"><span data-stu-id="a7e40-104">SYNTAX</span></span>

### <span data-ttu-id="a7e40-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="a7e40-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7e40-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a7e40-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a7e40-107">描述</span><span class="sxs-lookup"><span data-stu-id="a7e40-107">DESCRIPTION</span></span>
<span data-ttu-id="a7e40-108">**Restore-AzDataLakeStoreDeletedItem** Cmdlet 會還原 Data Lake Store 中已刪除的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="a7e40-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="a7e40-109">需要 Get-AzDataLakeStoreDeletedItem 所回收垃圾桶中已刪除專案的路徑。</span><span class="sxs-lookup"><span data-stu-id="a7e40-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>
<span data-ttu-id="a7e40-110">注意：取消下載檔案是最佳方法。</span><span class="sxs-lookup"><span data-stu-id="a7e40-110">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="a7e40-111">不保證檔案一旦刪除後即可以還原。</span><span class="sxs-lookup"><span data-stu-id="a7e40-111">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="a7e40-112">此 API 的使用會透過白名單啟用。</span><span class="sxs-lookup"><span data-stu-id="a7e40-112">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="a7e40-113">如果您的 ADL 帳戶未列入白名單，則使用此 api 會放棄未執行例外。</span><span class="sxs-lookup"><span data-stu-id="a7e40-113">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="a7e40-114">如需詳細資訊和協助，請聯絡 Microsoft 支援服務。</span><span class="sxs-lookup"><span data-stu-id="a7e40-114">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="a7e40-115">例子</span><span class="sxs-lookup"><span data-stu-id="a7e40-115">EXAMPLES</span></span>

### <span data-ttu-id="a7e40-116">範例 1：使用 -force 選項從 Data Lake Store 還原檔案</span><span class="sxs-lookup"><span data-stu-id="a7e40-116">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
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

## <span data-ttu-id="a7e40-117">參數</span><span class="sxs-lookup"><span data-stu-id="a7e40-117">PARAMETERS</span></span>

### <span data-ttu-id="a7e40-118">-帳戶</span><span class="sxs-lookup"><span data-stu-id="a7e40-118">-Account</span></span>
<span data-ttu-id="a7e40-119">指定 Data Lake Store 帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="a7e40-119">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a7e40-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7e40-120">-DefaultProfile</span></span>
<span data-ttu-id="a7e40-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a7e40-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7e40-122">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="a7e40-122">-DeletedItem</span></span>
<span data-ttu-id="a7e40-123">刪除的專案物件。</span><span class="sxs-lookup"><span data-stu-id="a7e40-123">The deleted item object.</span></span>

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

### <span data-ttu-id="a7e40-124">-目的地</span><span class="sxs-lookup"><span data-stu-id="a7e40-124">-Destination</span></span>
<span data-ttu-id="a7e40-125">刪除的檔案或資料夾應還原的目標路徑。</span><span class="sxs-lookup"><span data-stu-id="a7e40-125">The destination path to where the deleted file or folder should be restored.</span></span> 

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

### <span data-ttu-id="a7e40-126">-強制</span><span class="sxs-lookup"><span data-stu-id="a7e40-126">-Force</span></span>
<span data-ttu-id="a7e40-127">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="a7e40-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a7e40-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a7e40-128">-PassThru</span></span>
<span data-ttu-id="a7e40-129">成功時，再返回布林值。</span><span class="sxs-lookup"><span data-stu-id="a7e40-129">Return boolean true on success.</span></span>

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

### <span data-ttu-id="a7e40-130">-路徑</span><span class="sxs-lookup"><span data-stu-id="a7e40-130">-Path</span></span>
<span data-ttu-id="a7e40-131">已刪除的檔案或資料夾在垃圾桶中的路徑。</span><span class="sxs-lookup"><span data-stu-id="a7e40-131">The path of the deleted file or folder in trash.</span></span>

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

### <span data-ttu-id="a7e40-132">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="a7e40-132">-RestoreAction</span></span>
<span data-ttu-id="a7e40-133">針對目的地名稱衝突採取的動作 - 「複製」或「覆寫」</span><span class="sxs-lookup"><span data-stu-id="a7e40-133">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

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

### <span data-ttu-id="a7e40-134">-類型</span><span class="sxs-lookup"><span data-stu-id="a7e40-134">-Type</span></span>
<span data-ttu-id="a7e40-135">要還原的專案類型 - 「檔案」或「資料夾」</span><span class="sxs-lookup"><span data-stu-id="a7e40-135">The type of entry being restored - "file" or "folder"</span></span>

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

### <span data-ttu-id="a7e40-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7e40-136">CommonParameters</span></span>
<span data-ttu-id="a7e40-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a7e40-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7e40-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a7e40-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7e40-139">輸入</span><span class="sxs-lookup"><span data-stu-id="a7e40-139">INPUTS</span></span>

### <span data-ttu-id="a7e40-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a7e40-140">System.String</span></span>

## <span data-ttu-id="a7e40-141">輸出</span><span class="sxs-lookup"><span data-stu-id="a7e40-141">OUTPUTS</span></span>

### <span data-ttu-id="a7e40-142">沒有</span><span class="sxs-lookup"><span data-stu-id="a7e40-142">None</span></span>

## <span data-ttu-id="a7e40-143">筆記</span><span class="sxs-lookup"><span data-stu-id="a7e40-143">NOTES</span></span>

## <span data-ttu-id="a7e40-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="a7e40-144">RELATED LINKS</span></span>

[<span data-ttu-id="a7e40-145">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="a7e40-145">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)