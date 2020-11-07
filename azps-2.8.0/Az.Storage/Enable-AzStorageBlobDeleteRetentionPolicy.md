---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: fdac081aa6edc5ac43c98800ad2d857cb8f62b09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792625"
---
# <span data-ttu-id="165cd-101">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="165cd-101">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="165cd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="165cd-102">SYNOPSIS</span></span>
<span data-ttu-id="165cd-103">針對 Azure Storage Blob 服務啟用刪除保留原則。</span><span class="sxs-lookup"><span data-stu-id="165cd-103">Enable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="165cd-104">句法</span><span class="sxs-lookup"><span data-stu-id="165cd-104">SYNTAX</span></span>

### <span data-ttu-id="165cd-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="165cd-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RetentionDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="165cd-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="165cd-106">AccountObject</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="165cd-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="165cd-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="165cd-108">說明</span><span class="sxs-lookup"><span data-stu-id="165cd-108">DESCRIPTION</span></span>
<span data-ttu-id="165cd-109">**Enable-AzStorageBlobDeleteRetentionPolicy** Cmdlet 會啟用 Azure Storage Blob 服務的刪除保留原則。</span><span class="sxs-lookup"><span data-stu-id="165cd-109">The **Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="165cd-110">示例</span><span class="sxs-lookup"><span data-stu-id="165cd-110">EXAMPLES</span></span>

### <span data-ttu-id="165cd-111">範例1：啟用 [刪除 Blob 服務的保留原則]</span><span class="sxs-lookup"><span data-stu-id="165cd-111">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru -RetentionDays 4

Enabled Days
------- ----
   True    4
```

<span data-ttu-id="165cd-112">這個命令會啟用 Blob 服務的 [刪除保留原則]，並將 [刪除的 blob 保留天數] 設定為4。</span><span class="sxs-lookup"><span data-stu-id="165cd-112">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 4.</span></span>

## <span data-ttu-id="165cd-113">參數</span><span class="sxs-lookup"><span data-stu-id="165cd-113">PARAMETERS</span></span>

### <span data-ttu-id="165cd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="165cd-114">-DefaultProfile</span></span>
<span data-ttu-id="165cd-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="165cd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="165cd-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="165cd-116">-PassThru</span></span>
<span data-ttu-id="165cd-117">顯示 ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="165cd-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="165cd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="165cd-118">-ResourceGroupName</span></span>
<span data-ttu-id="165cd-119">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="165cd-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="165cd-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="165cd-120">-ResourceId</span></span>
<span data-ttu-id="165cd-121">輸入儲存空間帳戶資源識別碼，或 [Blob 服務屬性] 資源 Id。</span><span class="sxs-lookup"><span data-stu-id="165cd-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="165cd-122">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="165cd-122">-RetentionDays</span></span>
<span data-ttu-id="165cd-123">設定 DeleteRetentionPolicy 的保留天數。</span><span class="sxs-lookup"><span data-stu-id="165cd-123">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="165cd-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="165cd-124">-StorageAccount</span></span>
<span data-ttu-id="165cd-125">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="165cd-125">Storage account object</span></span>

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

### <span data-ttu-id="165cd-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="165cd-126">-StorageAccountName</span></span>
<span data-ttu-id="165cd-127">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="165cd-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="165cd-128">-確認</span><span class="sxs-lookup"><span data-stu-id="165cd-128">-Confirm</span></span>
<span data-ttu-id="165cd-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="165cd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="165cd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="165cd-130">-WhatIf</span></span>
<span data-ttu-id="165cd-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="165cd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="165cd-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="165cd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="165cd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="165cd-133">CommonParameters</span></span>
<span data-ttu-id="165cd-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="165cd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="165cd-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="165cd-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="165cd-136">輸入</span><span class="sxs-lookup"><span data-stu-id="165cd-136">INPUTS</span></span>

### <span data-ttu-id="165cd-137">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="165cd-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="165cd-138">System.object</span><span class="sxs-lookup"><span data-stu-id="165cd-138">System.String</span></span>

## <span data-ttu-id="165cd-139">輸出</span><span class="sxs-lookup"><span data-stu-id="165cd-139">OUTPUTS</span></span>

### <span data-ttu-id="165cd-140">PSBlobServiceProperties 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="165cd-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="165cd-141">筆記</span><span class="sxs-lookup"><span data-stu-id="165cd-141">NOTES</span></span>

## <span data-ttu-id="165cd-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="165cd-142">RELATED LINKS</span></span>
