---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: a5b5b1c761bb6e3c23a5dd5f0525d2d6627b3ab2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280156"
---
# <span data-ttu-id="9dde3-101">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="9dde3-101">Enable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="9dde3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9dde3-102">SYNOPSIS</span></span>
<span data-ttu-id="9dde3-103">在儲存空間帳戶上啟用 Blob 還原原則。</span><span class="sxs-lookup"><span data-stu-id="9dde3-103">Enables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="9dde3-104">句法</span><span class="sxs-lookup"><span data-stu-id="9dde3-104">SYNTAX</span></span>

### <span data-ttu-id="9dde3-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="9dde3-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RestoreDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9dde3-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="9dde3-106">AccountObject</span></span>
```
Enable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dde3-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="9dde3-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceId] <String> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dde3-108">說明</span><span class="sxs-lookup"><span data-stu-id="9dde3-108">DESCRIPTION</span></span>
<span data-ttu-id="9dde3-109">**Enable-AzStorageBlobRestorePolicy** Cmdlet 會針對 Azure Storage Blob 服務啟用 Blob 還原原則。</span><span class="sxs-lookup"><span data-stu-id="9dde3-109">The **Enable-AzStorageBlobRestorePolicy** cmdlet enables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="9dde3-110">示例</span><span class="sxs-lookup"><span data-stu-id="9dde3-110">EXAMPLES</span></span>

### <span data-ttu-id="9dde3-111">範例1：針對儲存空間帳戶上的 Azure Storage Blob 服務啟用 Blob 還原原則</span><span class="sxs-lookup"><span data-stu-id="9dde3-111">Example 1: Enables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
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

<span data-ttu-id="9dde3-112">這個命令首先啟用 Blob softdelete 和 changefeed，然後啟用 [Blob] 還原原則，最後請檢查 [Blob 服務屬性] 中的設定。</span><span class="sxs-lookup"><span data-stu-id="9dde3-112">This command first enable Blob softdelete and changefeed, then enables Blob Restore Policy, finally check the setting in Blob service properties.</span></span>
<span data-ttu-id="9dde3-113">[Blob 服務 RestorePolicy] 必須小於 DeleteRetentionPolicy 天。</span><span class="sxs-lookup"><span data-stu-id="9dde3-113">The Blob service RestorePolicy.Days must be smaller than DeleteRetentionPolicy.Days.</span></span>
<span data-ttu-id="9dde3-114">在啟用 blob 還原原則之前，必須先啟用 blob softdelete 和 ChangeFeed。</span><span class="sxs-lookup"><span data-stu-id="9dde3-114">Blob softdelete and ChangeFeed must be enabled before enable blob Restore Policy.</span></span>
<span data-ttu-id="9dde3-115">如果 softdelete 和 Changefeed 剛剛啟用，可能需要等候一段時間，讓伺服器處理該設定，然後再啟用 Blob 還原原則。</span><span class="sxs-lookup"><span data-stu-id="9dde3-115">If softdelete and Changefeed are just enabled, might need wait for some time for server to handle the setting, before enable Blob restore policy.</span></span>

## <span data-ttu-id="9dde3-116">參數</span><span class="sxs-lookup"><span data-stu-id="9dde3-116">PARAMETERS</span></span>

### <span data-ttu-id="9dde3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dde3-117">-DefaultProfile</span></span>
<span data-ttu-id="9dde3-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9dde3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dde3-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9dde3-119">-PassThru</span></span>
<span data-ttu-id="9dde3-120">顯示 ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="9dde3-120">Display ServiceProperties</span></span>

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

### <span data-ttu-id="9dde3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dde3-121">-ResourceGroupName</span></span>
<span data-ttu-id="9dde3-122">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="9dde3-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="9dde3-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9dde3-123">-ResourceId</span></span>
<span data-ttu-id="9dde3-124">輸入儲存空間帳戶資源識別碼，或 [Blob 服務屬性] 資源 Id。</span><span class="sxs-lookup"><span data-stu-id="9dde3-124">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="9dde3-125">-RestoreDays</span><span class="sxs-lookup"><span data-stu-id="9dde3-125">-RestoreDays</span></span>
<span data-ttu-id="9dde3-126">設定可還原 blob 的天數。</span><span class="sxs-lookup"><span data-stu-id="9dde3-126">Sets the number of days for the blob can be restored..</span></span>

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

### <span data-ttu-id="9dde3-127">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9dde3-127">-StorageAccount</span></span>
<span data-ttu-id="9dde3-128">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="9dde3-128">Storage account object</span></span>

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

### <span data-ttu-id="9dde3-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9dde3-129">-StorageAccountName</span></span>
<span data-ttu-id="9dde3-130">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9dde3-130">Storage Account Name.</span></span>

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

### <span data-ttu-id="9dde3-131">-確認</span><span class="sxs-lookup"><span data-stu-id="9dde3-131">-Confirm</span></span>
<span data-ttu-id="9dde3-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9dde3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dde3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dde3-133">-WhatIf</span></span>
<span data-ttu-id="9dde3-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9dde3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9dde3-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9dde3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dde3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dde3-136">CommonParameters</span></span>
<span data-ttu-id="9dde3-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9dde3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dde3-138">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9dde3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dde3-139">輸入</span><span class="sxs-lookup"><span data-stu-id="9dde3-139">INPUTS</span></span>

### <span data-ttu-id="9dde3-140">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="9dde3-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="9dde3-141">System.object</span><span class="sxs-lookup"><span data-stu-id="9dde3-141">System.String</span></span>

## <span data-ttu-id="9dde3-142">輸出</span><span class="sxs-lookup"><span data-stu-id="9dde3-142">OUTPUTS</span></span>

### <span data-ttu-id="9dde3-143">PSRestorePolicy 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="9dde3-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="9dde3-144">筆記</span><span class="sxs-lookup"><span data-stu-id="9dde3-144">NOTES</span></span>

## <span data-ttu-id="9dde3-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="9dde3-145">RELATED LINKS</span></span>
