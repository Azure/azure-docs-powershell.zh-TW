---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/import-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
ms.openlocfilehash: 278afd493d66fdc817bd61b0a11e15b1c6b54391
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452771"
---
# <span data-ttu-id="31f08-101">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="31f08-101">Import-AzureRmRedisCache</span></span>

## <span data-ttu-id="31f08-102">摘要</span><span class="sxs-lookup"><span data-stu-id="31f08-102">SYNOPSIS</span></span>
<span data-ttu-id="31f08-103">從 blob 匯入資料到 Azure Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="31f08-103">Imports data from blobs to Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31f08-104">句法</span><span class="sxs-lookup"><span data-stu-id="31f08-104">SYNTAX</span></span>

```
Import-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31f08-105">說明</span><span class="sxs-lookup"><span data-stu-id="31f08-105">DESCRIPTION</span></span>
<span data-ttu-id="31f08-106">匯 **入-AzureRmRedisCache** Cmdlet 會將資料從 blob 匯入到 Azure Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="31f08-106">The **Import-AzureRmRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="31f08-107">示例</span><span class="sxs-lookup"><span data-stu-id="31f08-107">EXAMPLES</span></span>

### <span data-ttu-id="31f08-108">範例1：匯入資料</span><span class="sxs-lookup"><span data-stu-id="31f08-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="31f08-109">這個命令會將 SAS URL 所指定的 blob 中的資料匯入 Azure Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="31f08-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="31f08-110">參數</span><span class="sxs-lookup"><span data-stu-id="31f08-110">PARAMETERS</span></span>

### <span data-ttu-id="31f08-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31f08-111">-DefaultProfile</span></span>
<span data-ttu-id="31f08-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="31f08-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f08-113">-檔案</span><span class="sxs-lookup"><span data-stu-id="31f08-113">-Files</span></span>
<span data-ttu-id="31f08-114">指定其內容此 Cmdlet 匯入到快取的 blob 的 SAS Url。</span><span class="sxs-lookup"><span data-stu-id="31f08-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="31f08-115">您可以使用下列 PowerShell 命令產生 SAS Url： $storageAccountCoNtext = New-AzureStorageContext-StorageAccountName "storageName"-StorageAccountKey "key" $sasKeyForBlob = New-AzureStorageBlobSASToken 容器 "容器"-blob "blobName"-許可權 "rwdl"-StartTime ( [System. DateTime]：： Now) 。AddMinutes (-15) -ExpiryTime ( [System. DateTime]：：現在) 。AddHours (5) -CoNtext $storageAccountCoNtext-FullUri Import-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName"- ($sasKeyForBlob) </span><span class="sxs-lookup"><span data-stu-id="31f08-115">You can generate the SAS URLs using the following PowerShell commands: $storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzureStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Import-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

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

### <span data-ttu-id="31f08-116">-Force</span><span class="sxs-lookup"><span data-stu-id="31f08-116">-Force</span></span>
<span data-ttu-id="31f08-117">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="31f08-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="31f08-118">-Format</span><span class="sxs-lookup"><span data-stu-id="31f08-118">-Format</span></span>
<span data-ttu-id="31f08-119">指定 blob 的格式。</span><span class="sxs-lookup"><span data-stu-id="31f08-119">Specifies the format of the blob.</span></span>
<span data-ttu-id="31f08-120">目前的 rdb 是唯一支援的格式。</span><span class="sxs-lookup"><span data-stu-id="31f08-120">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="31f08-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="31f08-121">-Name</span></span>
<span data-ttu-id="31f08-122">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="31f08-122">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="31f08-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31f08-123">-PassThru</span></span>
<span data-ttu-id="31f08-124">指示這個 Cmdlet 會傳回一個布林值，指出該作業是否會成功。</span><span class="sxs-lookup"><span data-stu-id="31f08-124">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="31f08-125">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="31f08-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="31f08-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31f08-126">-ResourceGroupName</span></span>
<span data-ttu-id="31f08-127">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="31f08-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="31f08-128">-確認</span><span class="sxs-lookup"><span data-stu-id="31f08-128">-Confirm</span></span>
<span data-ttu-id="31f08-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="31f08-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31f08-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31f08-130">-WhatIf</span></span>
<span data-ttu-id="31f08-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="31f08-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31f08-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="31f08-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31f08-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f08-133">CommonParameters</span></span>
<span data-ttu-id="31f08-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="31f08-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f08-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="31f08-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f08-136">輸入</span><span class="sxs-lookup"><span data-stu-id="31f08-136">INPUTS</span></span>

### <span data-ttu-id="31f08-137">System.object</span><span class="sxs-lookup"><span data-stu-id="31f08-137">System.String</span></span>

### <span data-ttu-id="31f08-138">System.object []</span><span class="sxs-lookup"><span data-stu-id="31f08-138">System.String[]</span></span>

## <span data-ttu-id="31f08-139">輸出</span><span class="sxs-lookup"><span data-stu-id="31f08-139">OUTPUTS</span></span>

### <span data-ttu-id="31f08-140">System.object</span><span class="sxs-lookup"><span data-stu-id="31f08-140">System.Boolean</span></span>

## <span data-ttu-id="31f08-141">筆記</span><span class="sxs-lookup"><span data-stu-id="31f08-141">NOTES</span></span>
* <span data-ttu-id="31f08-142">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="31f08-142">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="31f08-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="31f08-143">RELATED LINKS</span></span>

[<span data-ttu-id="31f08-144">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="31f08-144">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="31f08-145">新-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="31f08-145">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="31f08-146">移除-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="31f08-146">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="31f08-147">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="31f08-147">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="31f08-148">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="31f08-148">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)

