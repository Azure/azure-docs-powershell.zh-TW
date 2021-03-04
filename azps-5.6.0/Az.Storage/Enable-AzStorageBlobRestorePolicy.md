---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/enable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: cd3a8b12b6dbd6aec6dbc157aa3ff4d4ce398002
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907258"
---
# <span data-ttu-id="ffc3e-101">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="ffc3e-101">Enable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="ffc3e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ffc3e-102">SYNOPSIS</span></span>
<span data-ttu-id="ffc3e-103">在儲存空間帳戶上啟用 Blob 還原策略。</span><span class="sxs-lookup"><span data-stu-id="ffc3e-103">Enables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="ffc3e-104">語法</span><span class="sxs-lookup"><span data-stu-id="ffc3e-104">SYNTAX</span></span>

### <span data-ttu-id="ffc3e-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="ffc3e-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RestoreDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ffc3e-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ffc3e-106">AccountObject</span></span>
```
Enable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffc3e-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="ffc3e-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceId] <String> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffc3e-108">描述</span><span class="sxs-lookup"><span data-stu-id="ffc3e-108">DESCRIPTION</span></span>
<span data-ttu-id="ffc3e-109">**Enable-AzStorageBlobRestorePolicy** Cmdlet 可啟用 Azure 儲存體 Blob 服務的 Blob 還原策略。</span><span class="sxs-lookup"><span data-stu-id="ffc3e-109">The **Enable-AzStorageBlobRestorePolicy** cmdlet enables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="ffc3e-110">例子</span><span class="sxs-lookup"><span data-stu-id="ffc3e-110">EXAMPLES</span></span>

### <span data-ttu-id="ffc3e-111">範例 1：針對儲存帳戶上的 Azure 儲存體 Blob 服務啟用 Blob 還原策略</span><span class="sxs-lookup"><span data-stu-id="ffc3e-111">Example 1: Enables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" $accountName -RetentionDays 5

PS C:\> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -EnableChangeFeed $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegoup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : True
DeleteRetentionPolicy.Days    : 5
RestorePolicy.Enabled         : False
RestorePolicy.Days            : 
RestorePolicy.MinRestoreTime  : 
ChangeFeed                    : True
IsVersioningEnabled           : True

PS C:\> Enable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -RestoreDays 4

PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegoup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : True
DeleteRetentionPolicy.Days    : 5
RestorePolicy.Enabled         : True
RestorePolicy.Days            : 4
RestorePolicy.MinRestoreTime  : 8/28/2020 6:00:59 AM
ChangeFeed                    : True
IsVersioningEnabled           : True
```

<span data-ttu-id="ffc3e-112">此命令會先啟用 Blob Softdelete 和 changefeed，然後啟用 Blob 還原策略，最後檢查 Blob 服務屬性中的設定。</span><span class="sxs-lookup"><span data-stu-id="ffc3e-112">This command first enable Blob softdelete and changefeed, then enables Blob Restore Policy, finally check the setting in Blob service properties.</span></span>
<span data-ttu-id="ffc3e-113">Blob 服務 RestorePolicy.Days 必須小於 DeleteRetentionPolicy.Days。</span><span class="sxs-lookup"><span data-stu-id="ffc3e-113">The Blob service RestorePolicy.Days must be smaller than DeleteRetentionPolicy.Days.</span></span>
<span data-ttu-id="ffc3e-114">啟用 Blob 還原策略之前，必須先啟用 Blob softdelete 和 ChangeFeed。</span><span class="sxs-lookup"><span data-stu-id="ffc3e-114">Blob softdelete and ChangeFeed must be enabled before enable blob Restore Policy.</span></span>
<span data-ttu-id="ffc3e-115">如果只啟用 softdelete 和 Changefeed，可能需要等候一段時間，伺服器才能處理設定，才能啟用 Blob 還原策略。</span><span class="sxs-lookup"><span data-stu-id="ffc3e-115">If softdelete and Changefeed are just enabled, might need wait for some time for server to handle the setting, before enable Blob restore policy.</span></span>

## <span data-ttu-id="ffc3e-116">參數</span><span class="sxs-lookup"><span data-stu-id="ffc3e-116">PARAMETERS</span></span>

### <span data-ttu-id="ffc3e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffc3e-117">-DefaultProfile</span></span>
<span data-ttu-id="ffc3e-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ffc3e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffc3e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ffc3e-119">-PassThru</span></span>
<span data-ttu-id="ffc3e-120">顯示 ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="ffc3e-120">Display ServiceProperties</span></span>

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

### <span data-ttu-id="ffc3e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffc3e-121">-ResourceGroupName</span></span>
<span data-ttu-id="ffc3e-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="ffc3e-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc3e-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ffc3e-123">-ResourceId</span></span>
<span data-ttu-id="ffc3e-124">輸入儲存帳戶資源識別碼或 Blob 服務屬性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ffc3e-124">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc3e-125">-RestoreDays</span><span class="sxs-lookup"><span data-stu-id="ffc3e-125">-RestoreDays</span></span>
<span data-ttu-id="ffc3e-126">設定 Blob 可還原的天數。</span><span class="sxs-lookup"><span data-stu-id="ffc3e-126">Sets the number of days for the blob can be restored..</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc3e-127">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ffc3e-127">-StorageAccount</span></span>
<span data-ttu-id="ffc3e-128">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="ffc3e-128">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffc3e-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ffc3e-129">-StorageAccountName</span></span>
<span data-ttu-id="ffc3e-130">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ffc3e-130">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc3e-131">-確認</span><span class="sxs-lookup"><span data-stu-id="ffc3e-131">-Confirm</span></span>
<span data-ttu-id="ffc3e-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ffc3e-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc3e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffc3e-133">-WhatIf</span></span>
<span data-ttu-id="ffc3e-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ffc3e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffc3e-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ffc3e-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffc3e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffc3e-136">CommonParameters</span></span>
<span data-ttu-id="ffc3e-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ffc3e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffc3e-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ffc3e-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffc3e-139">輸入</span><span class="sxs-lookup"><span data-stu-id="ffc3e-139">INPUTS</span></span>

### <span data-ttu-id="ffc3e-140">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ffc3e-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="ffc3e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ffc3e-141">System.String</span></span>

## <span data-ttu-id="ffc3e-142">輸出</span><span class="sxs-lookup"><span data-stu-id="ffc3e-142">OUTPUTS</span></span>

### <span data-ttu-id="ffc3e-143">Microsoft.Azure.Commands.management.storage.models.PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="ffc3e-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="ffc3e-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ffc3e-144">NOTES</span></span>

## <span data-ttu-id="ffc3e-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="ffc3e-145">RELATED LINKS</span></span>
