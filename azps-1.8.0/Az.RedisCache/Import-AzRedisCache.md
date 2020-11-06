---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/import-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
ms.openlocfilehash: 018518f359c1142f9e20536f795b9080a942beaa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620999"
---
# <span data-ttu-id="03517-101">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="03517-101">Import-AzRedisCache</span></span>

## <span data-ttu-id="03517-102">摘要</span><span class="sxs-lookup"><span data-stu-id="03517-102">SYNOPSIS</span></span>
<span data-ttu-id="03517-103">從 blob 匯入資料到 Azure Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="03517-103">Imports data from blobs to Azure Redis Cache.</span></span>

## <span data-ttu-id="03517-104">句法</span><span class="sxs-lookup"><span data-stu-id="03517-104">SYNTAX</span></span>

```
Import-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03517-105">說明</span><span class="sxs-lookup"><span data-stu-id="03517-105">DESCRIPTION</span></span>
<span data-ttu-id="03517-106">匯 **入-AzRedisCache** Cmdlet 會將資料從 blob 匯入到 Azure Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="03517-106">The **Import-AzRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="03517-107">示例</span><span class="sxs-lookup"><span data-stu-id="03517-107">EXAMPLES</span></span>

### <span data-ttu-id="03517-108">範例1：匯入資料</span><span class="sxs-lookup"><span data-stu-id="03517-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="03517-109">這個命令會將 SAS URL 所指定的 blob 中的資料匯入 Azure Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="03517-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="03517-110">參數</span><span class="sxs-lookup"><span data-stu-id="03517-110">PARAMETERS</span></span>

### <span data-ttu-id="03517-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03517-111">-DefaultProfile</span></span>
<span data-ttu-id="03517-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="03517-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03517-113">-檔案</span><span class="sxs-lookup"><span data-stu-id="03517-113">-Files</span></span>
<span data-ttu-id="03517-114">指定其內容此 Cmdlet 匯入到快取的 blob 的 SAS Url。</span><span class="sxs-lookup"><span data-stu-id="03517-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="03517-115">您可以使用下列 PowerShell 命令產生 SAS Url： $storageAccountCoNtext = New-AzStorageContext-StorageAccountName "storageName"-StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken 容器 "容器"-blob "blobName"-許可權 "rwdl"-StartTime ( [System. DateTime]：： Now) 。AddMinutes (-15) -ExpiryTime ( [System. DateTime]：：現在) 。AddHours (5) -CoNtext $storageAccountCoNtext-FullUri Import-AzRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName"- ($sasKeyForBlob) </span><span class="sxs-lookup"><span data-stu-id="03517-115">You can generate the SAS URLs using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

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

### <span data-ttu-id="03517-116">-Force</span><span class="sxs-lookup"><span data-stu-id="03517-116">-Force</span></span>
<span data-ttu-id="03517-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="03517-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="03517-118">-Format</span><span class="sxs-lookup"><span data-stu-id="03517-118">-Format</span></span>
<span data-ttu-id="03517-119">指定 blob 的格式。</span><span class="sxs-lookup"><span data-stu-id="03517-119">Specifies the format of the blob.</span></span>
<span data-ttu-id="03517-120">目前的 rdb 是唯一支援的格式。</span><span class="sxs-lookup"><span data-stu-id="03517-120">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="03517-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="03517-121">-Name</span></span>
<span data-ttu-id="03517-122">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="03517-122">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="03517-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03517-123">-PassThru</span></span>
<span data-ttu-id="03517-124">指示這個 Cmdlet 會傳回一個布林值，指出該作業是否會成功。</span><span class="sxs-lookup"><span data-stu-id="03517-124">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="03517-125">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="03517-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="03517-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03517-126">-ResourceGroupName</span></span>
<span data-ttu-id="03517-127">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="03517-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="03517-128">-確認</span><span class="sxs-lookup"><span data-stu-id="03517-128">-Confirm</span></span>
<span data-ttu-id="03517-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="03517-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03517-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03517-130">-WhatIf</span></span>
<span data-ttu-id="03517-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="03517-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03517-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03517-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03517-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03517-133">CommonParameters</span></span>
<span data-ttu-id="03517-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="03517-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03517-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="03517-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03517-136">輸入</span><span class="sxs-lookup"><span data-stu-id="03517-136">INPUTS</span></span>

### <span data-ttu-id="03517-137">System.object</span><span class="sxs-lookup"><span data-stu-id="03517-137">System.String</span></span>

### <span data-ttu-id="03517-138">System.object []</span><span class="sxs-lookup"><span data-stu-id="03517-138">System.String[]</span></span>

## <span data-ttu-id="03517-139">輸出</span><span class="sxs-lookup"><span data-stu-id="03517-139">OUTPUTS</span></span>

### <span data-ttu-id="03517-140">System.object</span><span class="sxs-lookup"><span data-stu-id="03517-140">System.Boolean</span></span>

## <span data-ttu-id="03517-141">筆記</span><span class="sxs-lookup"><span data-stu-id="03517-141">NOTES</span></span>
* <span data-ttu-id="03517-142">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="03517-142">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="03517-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="03517-143">RELATED LINKS</span></span>

[<span data-ttu-id="03517-144">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="03517-144">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="03517-145">新-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="03517-145">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="03517-146">移除-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="03517-146">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="03517-147">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="03517-147">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="03517-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="03517-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


