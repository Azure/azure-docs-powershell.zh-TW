---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 01871c63d9a734cba88da30032f8b1da21198160
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793030"
---
# <span data-ttu-id="f4fc8-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="f4fc8-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="f4fc8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="f4fc8-103">建立儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="f4fc8-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="f4fc8-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4fc8-104">SYNTAX</span></span>

### <span data-ttu-id="f4fc8-105">AccountName (預設) </span><span class="sxs-lookup"><span data-stu-id="f4fc8-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4fc8-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f4fc8-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4fc8-107">說明</span><span class="sxs-lookup"><span data-stu-id="f4fc8-107">DESCRIPTION</span></span>
<span data-ttu-id="f4fc8-108">**新的-AzRmStorageShare** Cmdlet 會建立儲存檔案共用。</span><span class="sxs-lookup"><span data-stu-id="f4fc8-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="f4fc8-109">示例</span><span class="sxs-lookup"><span data-stu-id="f4fc8-109">EXAMPLES</span></span>

### <span data-ttu-id="f4fc8-110">範例1：使用儲存空間帳戶名稱和共用名稱稱（含中繼資料和共用配額）來建立儲存檔案共用（100 GiB）。</span><span class="sxs-lookup"><span data-stu-id="f4fc8-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   
```

<span data-ttu-id="f4fc8-111">這個命令會建立含中繼資料的儲存空間共用，並以 100 GiB 的方式共用配額。</span><span class="sxs-lookup"><span data-stu-id="f4fc8-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="f4fc8-112">範例2：使用儲存空間帳戶物件建立儲存檔案共用</span><span class="sxs-lookup"><span data-stu-id="f4fc8-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | New-AzRmStorageShare -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   
```

<span data-ttu-id="f4fc8-113">這個命令會建立包含儲存空間帳戶物件和共用名稱稱的儲存空間共用。</span><span class="sxs-lookup"><span data-stu-id="f4fc8-113">This command creates a Storage file share with Storage account object and share name.</span></span>

## <span data-ttu-id="f4fc8-114">參數</span><span class="sxs-lookup"><span data-stu-id="f4fc8-114">PARAMETERS</span></span>

### <span data-ttu-id="f4fc8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4fc8-115">-DefaultProfile</span></span>
<span data-ttu-id="f4fc8-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4fc8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4fc8-117">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="f4fc8-117">-Metadata</span></span>
<span data-ttu-id="f4fc8-118">共用中繼資料</span><span class="sxs-lookup"><span data-stu-id="f4fc8-118">Share Metadata</span></span>

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

### <span data-ttu-id="f4fc8-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f4fc8-119">-Name</span></span>
<span data-ttu-id="f4fc8-120">Azure 檔案共用名稱稱</span><span class="sxs-lookup"><span data-stu-id="f4fc8-120">Azure File share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fc8-121">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="f4fc8-121">-QuotaGiB</span></span>
<span data-ttu-id="f4fc8-122">在 Gibibyte 中共用配額。</span><span class="sxs-lookup"><span data-stu-id="f4fc8-122">Share Quota in Gibibyte.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4fc8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4fc8-123">-ResourceGroupName</span></span>
<span data-ttu-id="f4fc8-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f4fc8-124">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fc8-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f4fc8-125">-StorageAccount</span></span>
<span data-ttu-id="f4fc8-126">儲存空間帳戶物件</span><span class="sxs-lookup"><span data-stu-id="f4fc8-126">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fc8-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f4fc8-127">-StorageAccountName</span></span>
<span data-ttu-id="f4fc8-128">儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f4fc8-128">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4fc8-129">-確認</span><span class="sxs-lookup"><span data-stu-id="f4fc8-129">-Confirm</span></span>
<span data-ttu-id="f4fc8-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f4fc8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4fc8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4fc8-131">-WhatIf</span></span>
<span data-ttu-id="f4fc8-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f4fc8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4fc8-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f4fc8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4fc8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4fc8-134">CommonParameters</span></span>
<span data-ttu-id="f4fc8-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4fc8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4fc8-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f4fc8-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4fc8-137">輸入</span><span class="sxs-lookup"><span data-stu-id="f4fc8-137">INPUTS</span></span>

### <span data-ttu-id="f4fc8-138">System.object</span><span class="sxs-lookup"><span data-stu-id="f4fc8-138">System.String</span></span>

### <span data-ttu-id="f4fc8-139">PSStorageAccount 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="f4fc8-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="f4fc8-140">輸出</span><span class="sxs-lookup"><span data-stu-id="f4fc8-140">OUTPUTS</span></span>

### <span data-ttu-id="f4fc8-141">PSShare 中的 [管理]。</span><span class="sxs-lookup"><span data-stu-id="f4fc8-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="f4fc8-142">筆記</span><span class="sxs-lookup"><span data-stu-id="f4fc8-142">NOTES</span></span>

## <span data-ttu-id="f4fc8-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4fc8-143">RELATED LINKS</span></span>
