---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/export-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
ms.openlocfilehash: fb44ca997fd3b7599c25c5ba986ed0ca0771b3e6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140609"
---
# <span data-ttu-id="d589a-101">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d589a-101">Export-AzRedisCache</span></span>

## <span data-ttu-id="d589a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d589a-102">SYNOPSIS</span></span>
<span data-ttu-id="d589a-103">從 Azure Redis Cache 將資料匯出至容器。</span><span class="sxs-lookup"><span data-stu-id="d589a-103">Exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="d589a-104">句法</span><span class="sxs-lookup"><span data-stu-id="d589a-104">SYNTAX</span></span>

```
Export-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d589a-105">說明</span><span class="sxs-lookup"><span data-stu-id="d589a-105">DESCRIPTION</span></span>
<span data-ttu-id="d589a-106">**Export AzRedisCache** Cmdlet 會從 Azure Redis Cache 將資料匯出至容器。</span><span class="sxs-lookup"><span data-stu-id="d589a-106">The **Export-AzRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="d589a-107">示例</span><span class="sxs-lookup"><span data-stu-id="d589a-107">EXAMPLES</span></span>

### <span data-ttu-id="d589a-108">範例1：匯出資料</span><span class="sxs-lookup"><span data-stu-id="d589a-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="d589a-109">這個命令會將來自 Azure Redis Cache 實例的資料匯出到 SAS URL 所指定的容器中。</span><span class="sxs-lookup"><span data-stu-id="d589a-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="d589a-110">參數</span><span class="sxs-lookup"><span data-stu-id="d589a-110">PARAMETERS</span></span>

### <span data-ttu-id="d589a-111">-容器</span><span class="sxs-lookup"><span data-stu-id="d589a-111">-Container</span></span>
<span data-ttu-id="d589a-112">指定此 Cmdlet 匯出資料之容器的服務 SAS URL。</span><span class="sxs-lookup"><span data-stu-id="d589a-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="d589a-113">您可以使用下列 PowerShell 命令產生服務 SAS URL： $storageAccountCoNtext = New-AzStorageContext-StorageAccountName "storageName"-StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken 名稱 "容器"-許可權 "rwdl"-StartTime ( [System. DateTime]：：現在) 。AddMinutes (-15) -ExpiryTime ( [System. DateTime]：：現在) 。AddHours (5) -內容 $storageAccountCoNtext-FullUri Export-AzRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName"-Prefix "blobprefix"-容器 ($sasKeyForContainer) </span><span class="sxs-lookup"><span data-stu-id="d589a-113">You can generate a Service SAS URL using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d589a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d589a-114">-DefaultProfile</span></span>
<span data-ttu-id="d589a-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d589a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d589a-116">-Format</span><span class="sxs-lookup"><span data-stu-id="d589a-116">-Format</span></span>
<span data-ttu-id="d589a-117">指定 blob 的格式。</span><span class="sxs-lookup"><span data-stu-id="d589a-117">Specifies a format for the blob.</span></span>
<span data-ttu-id="d589a-118">目前的 rdb 是唯一支援的格式。</span><span class="sxs-lookup"><span data-stu-id="d589a-118">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="d589a-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="d589a-119">-Name</span></span>
<span data-ttu-id="d589a-120">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="d589a-120">Specifies the name of a cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d589a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d589a-121">-PassThru</span></span>
<span data-ttu-id="d589a-122">指示這個 Cmdlet 會傳回一個布林值，指出該作業是否會成功。</span><span class="sxs-lookup"><span data-stu-id="d589a-122">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="d589a-123">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="d589a-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d589a-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="d589a-124">-Prefix</span></span>
<span data-ttu-id="d589a-125">指定要用於 blob 名稱的前置詞。</span><span class="sxs-lookup"><span data-stu-id="d589a-125">Specifies a prefix to use for blob names.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d589a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d589a-126">-ResourceGroupName</span></span>
<span data-ttu-id="d589a-127">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d589a-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="d589a-128">-確認</span><span class="sxs-lookup"><span data-stu-id="d589a-128">-Confirm</span></span>
<span data-ttu-id="d589a-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d589a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d589a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d589a-130">-WhatIf</span></span>
<span data-ttu-id="d589a-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d589a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d589a-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d589a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d589a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d589a-133">CommonParameters</span></span>
<span data-ttu-id="d589a-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d589a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d589a-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d589a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d589a-136">輸入</span><span class="sxs-lookup"><span data-stu-id="d589a-136">INPUTS</span></span>

### <span data-ttu-id="d589a-137">System.object</span><span class="sxs-lookup"><span data-stu-id="d589a-137">System.String</span></span>

## <span data-ttu-id="d589a-138">輸出</span><span class="sxs-lookup"><span data-stu-id="d589a-138">OUTPUTS</span></span>

### <span data-ttu-id="d589a-139">System.object</span><span class="sxs-lookup"><span data-stu-id="d589a-139">System.Boolean</span></span>

## <span data-ttu-id="d589a-140">筆記</span><span class="sxs-lookup"><span data-stu-id="d589a-140">NOTES</span></span>
* <span data-ttu-id="d589a-141">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="d589a-141">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="d589a-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="d589a-142">RELATED LINKS</span></span>

[<span data-ttu-id="d589a-143">匯入-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d589a-143">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="d589a-144">新-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d589a-144">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="d589a-145">移除-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d589a-145">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="d589a-146">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d589a-146">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="d589a-147">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="d589a-147">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


