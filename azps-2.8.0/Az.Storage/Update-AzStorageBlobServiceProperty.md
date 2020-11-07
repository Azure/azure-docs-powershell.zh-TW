---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 195bc966bb47bf921eb0150272cfb9af6d73c63a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792919"
---
# <span data-ttu-id="9d2c2-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="9d2c2-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="9d2c2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9d2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="9d2c2-103">修改 Azure 儲存區 Blob 服務的服務屬性。</span><span class="sxs-lookup"><span data-stu-id="9d2c2-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="9d2c2-104">句法</span><span class="sxs-lookup"><span data-stu-id="9d2c2-104">SYNTAX</span></span>

### <span data-ttu-id="9d2c2-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="9d2c2-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d2c2-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="9d2c2-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d2c2-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="9d2c2-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d2c2-108">說明</span><span class="sxs-lookup"><span data-stu-id="9d2c2-108">DESCRIPTION</span></span>
<span data-ttu-id="9d2c2-109">**AzStorageBlobServiceProperty** Cmdlet 會修改 Azure Storage Blob 服務的服務屬性。</span><span class="sxs-lookup"><span data-stu-id="9d2c2-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="9d2c2-110">示例</span><span class="sxs-lookup"><span data-stu-id="9d2c2-110">EXAMPLES</span></span>

### <span data-ttu-id="9d2c2-111">範例1：將 Blob 服務 DefaultServiceVersion 設定為2018-03-28</span><span class="sxs-lookup"><span data-stu-id="9d2c2-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days
------------------ ----------------- --------------------- ----------------------------- --------------------------
myresourcegroup    mystorageaccount  2018-03-28            False
```

<span data-ttu-id="9d2c2-112">這個命令會將 Blob 服務的 DefaultServiceVersion 設定為2018-03-28。</span><span class="sxs-lookup"><span data-stu-id="9d2c2-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

## <span data-ttu-id="9d2c2-113">參數</span><span class="sxs-lookup"><span data-stu-id="9d2c2-113">PARAMETERS</span></span>

### <span data-ttu-id="9d2c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d2c2-114">-DefaultProfile</span></span>
<span data-ttu-id="9d2c2-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9d2c2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d2c2-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="9d2c2-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="9d2c2-117">要設定的預設服務版本</span><span class="sxs-lookup"><span data-stu-id="9d2c2-117">Default Service Version to Set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d2c2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d2c2-118">-ResourceGroupName</span></span>
<span data-ttu-id="9d2c2-119">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="9d2c2-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="9d2c2-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d2c2-120">-ResourceId</span></span>
<span data-ttu-id="9d2c2-121">輸入儲存空間帳戶資源識別碼，或 [Blob 服務屬性] 資源 Id。</span><span class="sxs-lookup"><span data-stu-id="9d2c2-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="9d2c2-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9d2c2-122">-StorageAccount</span></span>
<span data-ttu-id="9d2c2-123">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="9d2c2-123">Storage account object</span></span>

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

### <span data-ttu-id="9d2c2-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9d2c2-124">-StorageAccountName</span></span>
<span data-ttu-id="9d2c2-125">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="9d2c2-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="9d2c2-126">-確認</span><span class="sxs-lookup"><span data-stu-id="9d2c2-126">-Confirm</span></span>
<span data-ttu-id="9d2c2-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9d2c2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d2c2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d2c2-128">-WhatIf</span></span>
<span data-ttu-id="9d2c2-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9d2c2-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d2c2-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9d2c2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d2c2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d2c2-131">CommonParameters</span></span>
<span data-ttu-id="9d2c2-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9d2c2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d2c2-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9d2c2-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d2c2-134">輸入</span><span class="sxs-lookup"><span data-stu-id="9d2c2-134">INPUTS</span></span>

### <span data-ttu-id="9d2c2-135">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="9d2c2-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="9d2c2-136">System.object</span><span class="sxs-lookup"><span data-stu-id="9d2c2-136">System.String</span></span>

## <span data-ttu-id="9d2c2-137">輸出</span><span class="sxs-lookup"><span data-stu-id="9d2c2-137">OUTPUTS</span></span>

### <span data-ttu-id="9d2c2-138">PSBlobServiceProperties 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="9d2c2-138">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="9d2c2-139">筆記</span><span class="sxs-lookup"><span data-stu-id="9d2c2-139">NOTES</span></span>

## <span data-ttu-id="9d2c2-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="9d2c2-140">RELATED LINKS</span></span>
