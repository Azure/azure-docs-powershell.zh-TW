---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/powershell/module/az.rediscache/import-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
ms.openlocfilehash: 34ea5ccc662514b3a2807924c932fb2e11b5b214
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914690"
---
# <span data-ttu-id="efdd9-101">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="efdd9-101">Import-AzRedisCache</span></span>

## <span data-ttu-id="efdd9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="efdd9-102">SYNOPSIS</span></span>
<span data-ttu-id="efdd9-103">將資料從 Blob 導入到 Azure Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="efdd9-103">Imports data from blobs to Azure Redis Cache.</span></span>

## <span data-ttu-id="efdd9-104">語法</span><span class="sxs-lookup"><span data-stu-id="efdd9-104">SYNTAX</span></span>

```
Import-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efdd9-105">描述</span><span class="sxs-lookup"><span data-stu-id="efdd9-105">DESCRIPTION</span></span>
<span data-ttu-id="efdd9-106">**Import-AzRedisCache** Cmdlet 將資料從 Blob 導入 Azure Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="efdd9-106">The **Import-AzRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="efdd9-107">例子</span><span class="sxs-lookup"><span data-stu-id="efdd9-107">EXAMPLES</span></span>

### <span data-ttu-id="efdd9-108">範例 1：匯出資料</span><span class="sxs-lookup"><span data-stu-id="efdd9-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="efdd9-109">此命令會從 SAS URL 指定的 Blob 將資料導入 Azure Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="efdd9-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="efdd9-110">參數</span><span class="sxs-lookup"><span data-stu-id="efdd9-110">PARAMETERS</span></span>

### <span data-ttu-id="efdd9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efdd9-111">-DefaultProfile</span></span>
<span data-ttu-id="efdd9-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="efdd9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="efdd9-113">-檔案</span><span class="sxs-lookup"><span data-stu-id="efdd9-113">-Files</span></span>
<span data-ttu-id="efdd9-114">指定此 Cmdlet 內容會導入至緩存的 Blob 的 SAS URL。</span><span class="sxs-lookup"><span data-stu-id="efdd9-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="efdd9-115">您可以使用下列 PowerShell 命令產生 SAS URL：$storageAccountCoNtext = New-AzStorageContext -StorageAccountName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]：：now) 。AddMinutes (-15) -ExpiryTime ([System.DateTime]：：now) 。AddHours (5) -CoNtext $storageAccountCoNtext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -files ($sasKeyForBlob) -Force</span><span class="sxs-lookup"><span data-stu-id="efdd9-115">You can generate the SAS URLs using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efdd9-116">-強制</span><span class="sxs-lookup"><span data-stu-id="efdd9-116">-Force</span></span>
<span data-ttu-id="efdd9-117">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="efdd9-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="efdd9-118">-格式</span><span class="sxs-lookup"><span data-stu-id="efdd9-118">-Format</span></span>
<span data-ttu-id="efdd9-119">指定 Blob 的格式。</span><span class="sxs-lookup"><span data-stu-id="efdd9-119">Specifies the format of the blob.</span></span>
<span data-ttu-id="efdd9-120">目前唯一支援的格式是 rdb。</span><span class="sxs-lookup"><span data-stu-id="efdd9-120">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="efdd9-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="efdd9-121">-Name</span></span>
<span data-ttu-id="efdd9-122">指定緩存的名稱。</span><span class="sxs-lookup"><span data-stu-id="efdd9-122">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="efdd9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="efdd9-123">-PassThru</span></span>
<span data-ttu-id="efdd9-124">表示此 Cmdlet 會返回布林值，指出作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="efdd9-124">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="efdd9-125">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="efdd9-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="efdd9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efdd9-126">-ResourceGroupName</span></span>
<span data-ttu-id="efdd9-127">指定包含該緩存的資源組名。</span><span class="sxs-lookup"><span data-stu-id="efdd9-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="efdd9-128">-確認</span><span class="sxs-lookup"><span data-stu-id="efdd9-128">-Confirm</span></span>
<span data-ttu-id="efdd9-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="efdd9-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efdd9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efdd9-130">-WhatIf</span></span>
<span data-ttu-id="efdd9-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="efdd9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="efdd9-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="efdd9-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efdd9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efdd9-133">CommonParameters</span></span>
<span data-ttu-id="efdd9-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="efdd9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efdd9-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="efdd9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efdd9-136">輸入</span><span class="sxs-lookup"><span data-stu-id="efdd9-136">INPUTS</span></span>

### <span data-ttu-id="efdd9-137">System.String</span><span class="sxs-lookup"><span data-stu-id="efdd9-137">System.String</span></span>

### <span data-ttu-id="efdd9-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="efdd9-138">System.String[]</span></span>

## <span data-ttu-id="efdd9-139">輸出</span><span class="sxs-lookup"><span data-stu-id="efdd9-139">OUTPUTS</span></span>

### <span data-ttu-id="efdd9-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="efdd9-140">System.Boolean</span></span>

## <span data-ttu-id="efdd9-141">筆記</span><span class="sxs-lookup"><span data-stu-id="efdd9-141">NOTES</span></span>
* <span data-ttu-id="efdd9-142">關鍵字：azure、azurerm、arm、resource、management、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="efdd9-142">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="efdd9-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="efdd9-143">RELATED LINKS</span></span>

[<span data-ttu-id="efdd9-144">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="efdd9-144">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="efdd9-145">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="efdd9-145">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="efdd9-146">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="efdd9-146">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="efdd9-147">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="efdd9-147">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="efdd9-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="efdd9-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


