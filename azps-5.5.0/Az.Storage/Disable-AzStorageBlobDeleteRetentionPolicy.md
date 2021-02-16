---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: f3891d30322a7c6577c14d43f7796a3242b53ecf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133455"
---
# <span data-ttu-id="64134-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="64134-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="64134-102">摘要</span><span class="sxs-lookup"><span data-stu-id="64134-102">SYNOPSIS</span></span>
<span data-ttu-id="64134-103">停用 Azure Storage Blob 服務的 [刪除保留原則]。</span><span class="sxs-lookup"><span data-stu-id="64134-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="64134-104">句法</span><span class="sxs-lookup"><span data-stu-id="64134-104">SYNTAX</span></span>

### <span data-ttu-id="64134-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="64134-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64134-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="64134-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64134-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="64134-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64134-108">說明</span><span class="sxs-lookup"><span data-stu-id="64134-108">DESCRIPTION</span></span>
<span data-ttu-id="64134-109">**Disable AzStorageBlobDeleteRetentionPolicy** Cmdlet 會停用 Azure Storage Blob 服務的刪除保留原則。</span><span class="sxs-lookup"><span data-stu-id="64134-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="64134-110">示例</span><span class="sxs-lookup"><span data-stu-id="64134-110">EXAMPLES</span></span>

### <span data-ttu-id="64134-111">範例1：停用 [刪除 Blob 服務的保留原則]</span><span class="sxs-lookup"><span data-stu-id="64134-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="64134-112">這個命令會停用 [刪除 Blob 服務的保留原則]。</span><span class="sxs-lookup"><span data-stu-id="64134-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="64134-113">參數</span><span class="sxs-lookup"><span data-stu-id="64134-113">PARAMETERS</span></span>

### <span data-ttu-id="64134-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64134-114">-DefaultProfile</span></span>
<span data-ttu-id="64134-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="64134-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64134-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64134-116">-PassThru</span></span>
<span data-ttu-id="64134-117">顯示 ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="64134-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="64134-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64134-118">-ResourceGroupName</span></span>
<span data-ttu-id="64134-119">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="64134-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="64134-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64134-120">-ResourceId</span></span>
<span data-ttu-id="64134-121">輸入儲存空間帳戶資源識別碼，或 [Blob 服務屬性] 資源 Id。</span><span class="sxs-lookup"><span data-stu-id="64134-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="64134-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="64134-122">-StorageAccount</span></span>
<span data-ttu-id="64134-123">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="64134-123">Storage account object</span></span>

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

### <span data-ttu-id="64134-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="64134-124">-StorageAccountName</span></span>
<span data-ttu-id="64134-125">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="64134-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="64134-126">-確認</span><span class="sxs-lookup"><span data-stu-id="64134-126">-Confirm</span></span>
<span data-ttu-id="64134-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="64134-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64134-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64134-128">-WhatIf</span></span>
<span data-ttu-id="64134-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="64134-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64134-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="64134-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64134-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64134-131">CommonParameters</span></span>
<span data-ttu-id="64134-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="64134-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64134-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="64134-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64134-134">輸入</span><span class="sxs-lookup"><span data-stu-id="64134-134">INPUTS</span></span>

### <span data-ttu-id="64134-135">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="64134-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="64134-136">System.object</span><span class="sxs-lookup"><span data-stu-id="64134-136">System.String</span></span>

## <span data-ttu-id="64134-137">輸出</span><span class="sxs-lookup"><span data-stu-id="64134-137">OUTPUTS</span></span>

### <span data-ttu-id="64134-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="64134-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="64134-139">筆記</span><span class="sxs-lookup"><span data-stu-id="64134-139">NOTES</span></span>

## <span data-ttu-id="64134-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="64134-140">RELATED LINKS</span></span>
