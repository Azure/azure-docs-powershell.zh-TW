---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/enable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: 9a4afaa1a67d9f1f9bffa0fdf6c7b40c7cf72b13
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907266"
---
# <span data-ttu-id="2f071-101">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2f071-101">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="2f071-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2f071-102">SYNOPSIS</span></span>
<span data-ttu-id="2f071-103">啟用 Azure 儲存體 Blob 服務的刪除保留原則。</span><span class="sxs-lookup"><span data-stu-id="2f071-103">Enable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="2f071-104">語法</span><span class="sxs-lookup"><span data-stu-id="2f071-104">SYNTAX</span></span>

### <span data-ttu-id="2f071-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="2f071-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RetentionDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f071-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="2f071-106">AccountObject</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f071-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="2f071-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f071-108">描述</span><span class="sxs-lookup"><span data-stu-id="2f071-108">DESCRIPTION</span></span>
<span data-ttu-id="2f071-109">**Enable-AzStorageBlobDeleteRetentionPolidlet** 啟用 Azure 儲存體 Blob 服務的刪除保留原則。</span><span class="sxs-lookup"><span data-stu-id="2f071-109">The **Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="2f071-110">例子</span><span class="sxs-lookup"><span data-stu-id="2f071-110">EXAMPLES</span></span>

### <span data-ttu-id="2f071-111">範例 1：啟用 Blob 服務的刪除保留原則</span><span class="sxs-lookup"><span data-stu-id="2f071-111">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru -RetentionDays 4

Enabled Days
------- ----
   True    4
```

<span data-ttu-id="2f071-112">此命令會啟用 Blob 服務的刪除保留原則，並且將已刪除的 Blob 保留天數設為 4。</span><span class="sxs-lookup"><span data-stu-id="2f071-112">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 4.</span></span>

## <span data-ttu-id="2f071-113">參數</span><span class="sxs-lookup"><span data-stu-id="2f071-113">PARAMETERS</span></span>

### <span data-ttu-id="2f071-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f071-114">-DefaultProfile</span></span>
<span data-ttu-id="2f071-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f071-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f071-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f071-116">-PassThru</span></span>
<span data-ttu-id="2f071-117">顯示 ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="2f071-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="2f071-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f071-118">-ResourceGroupName</span></span>
<span data-ttu-id="2f071-119">資源組名。</span><span class="sxs-lookup"><span data-stu-id="2f071-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="2f071-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f071-120">-ResourceId</span></span>
<span data-ttu-id="2f071-121">輸入儲存帳戶資源識別碼或 Blob 服務屬性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f071-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="2f071-122">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="2f071-122">-RetentionDays</span></span>
<span data-ttu-id="2f071-123">設定 DeleteRetentionPolicy 的保留天數。</span><span class="sxs-lookup"><span data-stu-id="2f071-123">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="2f071-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2f071-124">-StorageAccount</span></span>
<span data-ttu-id="2f071-125">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="2f071-125">Storage account object</span></span>

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

### <span data-ttu-id="2f071-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2f071-126">-StorageAccountName</span></span>
<span data-ttu-id="2f071-127">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2f071-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="2f071-128">-確認</span><span class="sxs-lookup"><span data-stu-id="2f071-128">-Confirm</span></span>
<span data-ttu-id="2f071-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2f071-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f071-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f071-130">-WhatIf</span></span>
<span data-ttu-id="2f071-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2f071-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f071-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f071-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f071-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f071-133">CommonParameters</span></span>
<span data-ttu-id="2f071-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2f071-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f071-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="2f071-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f071-136">輸入</span><span class="sxs-lookup"><span data-stu-id="2f071-136">INPUTS</span></span>

### <span data-ttu-id="2f071-137">Microsoft.Azure.Commands.management.storage.models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2f071-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="2f071-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2f071-138">System.String</span></span>

## <span data-ttu-id="2f071-139">輸出</span><span class="sxs-lookup"><span data-stu-id="2f071-139">OUTPUTS</span></span>

### <span data-ttu-id="2f071-140">Microsoft.Azure.Commands.management.storage.models.PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="2f071-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="2f071-141">筆記</span><span class="sxs-lookup"><span data-stu-id="2f071-141">NOTES</span></span>

## <span data-ttu-id="2f071-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f071-142">RELATED LINKS</span></span>
