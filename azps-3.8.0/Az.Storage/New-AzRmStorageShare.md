---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 040e4e8584c29f77e6b847eea886851c41e606e9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959089"
---
# <span data-ttu-id="2c22d-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="2c22d-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="2c22d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2c22d-102">SYNOPSIS</span></span>
<span data-ttu-id="2c22d-103">建立儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="2c22d-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="2c22d-104">句法</span><span class="sxs-lookup"><span data-stu-id="2c22d-104">SYNTAX</span></span>

### <span data-ttu-id="2c22d-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="2c22d-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c22d-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="2c22d-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c22d-107">說明</span><span class="sxs-lookup"><span data-stu-id="2c22d-107">DESCRIPTION</span></span>
<span data-ttu-id="2c22d-108">**新的-AzRmStorageShare** Cmdlet 會建立儲存檔案共用。</span><span class="sxs-lookup"><span data-stu-id="2c22d-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="2c22d-109">示例</span><span class="sxs-lookup"><span data-stu-id="2c22d-109">EXAMPLES</span></span>

### <span data-ttu-id="2c22d-110">範例1：使用儲存空間帳戶名稱和共用名稱稱（含中繼資料和共用配額）來建立儲存檔案共用（100 GiB）。</span><span class="sxs-lookup"><span data-stu-id="2c22d-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup
```

<span data-ttu-id="2c22d-111">這個命令會建立含中繼資料的儲存空間共用，並以 100 GiB 的方式共用配額。</span><span class="sxs-lookup"><span data-stu-id="2c22d-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="2c22d-112">範例2：使用儲存空間帳戶物件建立儲存檔案共用</span><span class="sxs-lookup"><span data-stu-id="2c22d-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | New-AzRmStorageShare -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup
```

<span data-ttu-id="2c22d-113">這個命令會建立包含儲存空間帳戶物件和共用名稱稱的儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="2c22d-113">This command creates a Storage file share with Storage account object and share name.</span></span>

## <span data-ttu-id="2c22d-114">參數</span><span class="sxs-lookup"><span data-stu-id="2c22d-114">PARAMETERS</span></span>

### <span data-ttu-id="2c22d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c22d-115">-DefaultProfile</span></span>
<span data-ttu-id="2c22d-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c22d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c22d-117">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="2c22d-117">-Metadata</span></span>
<span data-ttu-id="2c22d-118">共用中繼資料</span><span class="sxs-lookup"><span data-stu-id="2c22d-118">Share Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c22d-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="2c22d-119">-Name</span></span>
<span data-ttu-id="2c22d-120">Azure 檔案共用名稱稱</span><span class="sxs-lookup"><span data-stu-id="2c22d-120">Azure File share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c22d-121">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="2c22d-121">-QuotaGiB</span></span>
<span data-ttu-id="2c22d-122">在 Gibibyte 中共用配額。</span><span class="sxs-lookup"><span data-stu-id="2c22d-122">Share Quota in Gibibyte.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Quota

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c22d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c22d-123">-ResourceGroupName</span></span>
<span data-ttu-id="2c22d-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="2c22d-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="2c22d-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c22d-125">-StorageAccount</span></span>
<span data-ttu-id="2c22d-126">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="2c22d-126">Storage account object</span></span>

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

### <span data-ttu-id="2c22d-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2c22d-127">-StorageAccountName</span></span>
<span data-ttu-id="2c22d-128">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="2c22d-128">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c22d-129">-確認</span><span class="sxs-lookup"><span data-stu-id="2c22d-129">-Confirm</span></span>
<span data-ttu-id="2c22d-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2c22d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c22d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c22d-131">-WhatIf</span></span>
<span data-ttu-id="2c22d-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2c22d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c22d-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2c22d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c22d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c22d-134">CommonParameters</span></span>
<span data-ttu-id="2c22d-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2c22d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c22d-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2c22d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c22d-137">輸入</span><span class="sxs-lookup"><span data-stu-id="2c22d-137">INPUTS</span></span>

### <span data-ttu-id="2c22d-138">System.object</span><span class="sxs-lookup"><span data-stu-id="2c22d-138">System.String</span></span>

### <span data-ttu-id="2c22d-139">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="2c22d-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="2c22d-140">輸出</span><span class="sxs-lookup"><span data-stu-id="2c22d-140">OUTPUTS</span></span>

### <span data-ttu-id="2c22d-141">PSShare 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="2c22d-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="2c22d-142">筆記</span><span class="sxs-lookup"><span data-stu-id="2c22d-142">NOTES</span></span>

## <span data-ttu-id="2c22d-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c22d-143">RELATED LINKS</span></span>
