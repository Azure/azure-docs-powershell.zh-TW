---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
ms.openlocfilehash: 0edfec1d98423f444b2291d43e6f2a3489e20b29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453304"
---
# <span data-ttu-id="74d52-101">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="74d52-101">Export-AzureRmRedisCache</span></span>

## <span data-ttu-id="74d52-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74d52-102">SYNOPSIS</span></span>
<span data-ttu-id="74d52-103">從 Azure Redis Cache 將資料匯出至容器。</span><span class="sxs-lookup"><span data-stu-id="74d52-103">Exports data from Azure Redis Cache to a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74d52-104">句法</span><span class="sxs-lookup"><span data-stu-id="74d52-104">SYNTAX</span></span>

```
Export-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74d52-105">說明</span><span class="sxs-lookup"><span data-stu-id="74d52-105">DESCRIPTION</span></span>
<span data-ttu-id="74d52-106">**Export AzureRmRedisCache** Cmdlet 會從 Azure Redis Cache 將資料匯出至容器。</span><span class="sxs-lookup"><span data-stu-id="74d52-106">The **Export-AzureRmRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="74d52-107">示例</span><span class="sxs-lookup"><span data-stu-id="74d52-107">EXAMPLES</span></span>

### <span data-ttu-id="74d52-108">範例1：匯出資料</span><span class="sxs-lookup"><span data-stu-id="74d52-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="74d52-109">這個命令會將來自 Azure Redis Cache 實例的資料匯出到 SAS URL 所指定的容器中。</span><span class="sxs-lookup"><span data-stu-id="74d52-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="74d52-110">參數</span><span class="sxs-lookup"><span data-stu-id="74d52-110">PARAMETERS</span></span>

### <span data-ttu-id="74d52-111">-容器</span><span class="sxs-lookup"><span data-stu-id="74d52-111">-Container</span></span>
<span data-ttu-id="74d52-112">指定此 Cmdlet 匯出資料之容器的服務 SAS URL。</span><span class="sxs-lookup"><span data-stu-id="74d52-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="74d52-113">您可以使用下列 PowerShell 命令產生服務 SAS URL：</span><span class="sxs-lookup"><span data-stu-id="74d52-113">You can generate a Service SAS URL using the following PowerShell commands:</span></span>

<span data-ttu-id="74d52-114">$storageAccountCoNtext = New-AzureStorageContext-StorageAccountName "storageName"-StorageAccountKey "key"</span><span class="sxs-lookup"><span data-stu-id="74d52-114">$storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key"</span></span>

<span data-ttu-id="74d52-115">$sasKeyForContainer = New-AzureStorageContainerSASToken 名稱 "容器"-許可權 "rwdl"-StartTime ( [System.object]：：現在) 。AddMinutes (-15) -ExpiryTime ( [System. DateTime]：：現在) 。AddHours (5) -內容 $storageAccountCoNtext-FullUri</span><span class="sxs-lookup"><span data-stu-id="74d52-115">$sasKeyForContainer = New-AzureStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri</span></span> 

<span data-ttu-id="74d52-116">Export-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName"-Prefix "blobprefix"-容器 ($sasKeyForContainer) </span><span class="sxs-lookup"><span data-stu-id="74d52-116">Export-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="74d52-117">-Format</span><span class="sxs-lookup"><span data-stu-id="74d52-117">-Format</span></span>
<span data-ttu-id="74d52-118">指定 blob 的格式。</span><span class="sxs-lookup"><span data-stu-id="74d52-118">Specifies a format for the blob.</span></span>
<span data-ttu-id="74d52-119">目前的 rdb 是唯一支援的格式。</span><span class="sxs-lookup"><span data-stu-id="74d52-119">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="74d52-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="74d52-120">-Name</span></span>
<span data-ttu-id="74d52-121">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="74d52-121">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="74d52-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74d52-122">-PassThru</span></span>
<span data-ttu-id="74d52-123">指示這個 Cmdlet 會傳回一個布林值，指出該作業是否會成功。</span><span class="sxs-lookup"><span data-stu-id="74d52-123">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="74d52-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="74d52-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="74d52-125">-Prefix</span><span class="sxs-lookup"><span data-stu-id="74d52-125">-Prefix</span></span>
<span data-ttu-id="74d52-126">指定要用於 blob 名稱的前置詞。</span><span class="sxs-lookup"><span data-stu-id="74d52-126">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="74d52-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74d52-127">-ResourceGroupName</span></span>
<span data-ttu-id="74d52-128">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="74d52-128">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="74d52-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74d52-129">-DefaultProfile</span></span>
<span data-ttu-id="74d52-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="74d52-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74d52-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74d52-131">CommonParameters</span></span>
<span data-ttu-id="74d52-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74d52-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74d52-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="74d52-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74d52-134">輸入</span><span class="sxs-lookup"><span data-stu-id="74d52-134">INPUTS</span></span>

### <span data-ttu-id="74d52-135">所有</span><span class="sxs-lookup"><span data-stu-id="74d52-135">None</span></span>
<span data-ttu-id="74d52-136">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74d52-136">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="74d52-137">輸出</span><span class="sxs-lookup"><span data-stu-id="74d52-137">OUTPUTS</span></span>

### <span data-ttu-id="74d52-138">所有</span><span class="sxs-lookup"><span data-stu-id="74d52-138">None</span></span>

## <span data-ttu-id="74d52-139">筆記</span><span class="sxs-lookup"><span data-stu-id="74d52-139">NOTES</span></span>
* <span data-ttu-id="74d52-140">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="74d52-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="74d52-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="74d52-141">RELATED LINKS</span></span>

[<span data-ttu-id="74d52-142">匯入-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="74d52-142">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="74d52-143">新-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="74d52-143">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="74d52-144">移除-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="74d52-144">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="74d52-145">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="74d52-145">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="74d52-146">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="74d52-146">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


