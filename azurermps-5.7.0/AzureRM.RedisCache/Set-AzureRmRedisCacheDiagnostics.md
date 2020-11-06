---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscachediagnostics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: bab40aec2cd4a03d013f2c215f1baaaead3dc51e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444387"
---
# <span data-ttu-id="d221b-101">Set-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="d221b-101">Set-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="d221b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d221b-102">SYNOPSIS</span></span>
<span data-ttu-id="d221b-103">啟用 Azure Redis Cache 的診斷。</span><span class="sxs-lookup"><span data-stu-id="d221b-103">Enables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d221b-104">句法</span><span class="sxs-lookup"><span data-stu-id="d221b-104">SYNTAX</span></span>

```
Set-AzureRmRedisCacheDiagnostics [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d221b-105">說明</span><span class="sxs-lookup"><span data-stu-id="d221b-105">DESCRIPTION</span></span>
<span data-ttu-id="d221b-106">**AzureRmRedisCacheDiagnostics** Cmdlet 可為 Azure Redis Cache 啟用診斷。</span><span class="sxs-lookup"><span data-stu-id="d221b-106">The **Set-AzureRmRedisCacheDiagnostics** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="d221b-107">示例</span><span class="sxs-lookup"><span data-stu-id="d221b-107">EXAMPLES</span></span>

### <span data-ttu-id="d221b-108">範例1：啟用診斷</span><span class="sxs-lookup"><span data-stu-id="d221b-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="d221b-109">這個命令會啟用 Azure Redis 快取的診斷。</span><span class="sxs-lookup"><span data-stu-id="d221b-109">This command enables diagnostics for an Azure Redis cache.</span></span>

<span data-ttu-id="d221b-110">此命令將針對訂閱的同一區域中的所有 Azure Redis 緩存啟用診斷或更新儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="d221b-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="d221b-111">參數</span><span class="sxs-lookup"><span data-stu-id="d221b-111">PARAMETERS</span></span>

### <span data-ttu-id="d221b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d221b-112">-DefaultProfile</span></span>
<span data-ttu-id="d221b-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d221b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d221b-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="d221b-114">-Name</span></span>
<span data-ttu-id="d221b-115">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="d221b-115">Specifies the name of the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d221b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d221b-116">-ResourceGroupName</span></span>
<span data-ttu-id="d221b-117">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d221b-117">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d221b-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d221b-118">-StorageAccountId</span></span>
<span data-ttu-id="d221b-119">指定用來儲存診斷資料之儲存空間帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d221b-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d221b-120">-確認</span><span class="sxs-lookup"><span data-stu-id="d221b-120">-Confirm</span></span>
<span data-ttu-id="d221b-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d221b-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d221b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d221b-122">-WhatIf</span></span>
<span data-ttu-id="d221b-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d221b-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d221b-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d221b-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d221b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d221b-125">CommonParameters</span></span>
<span data-ttu-id="d221b-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d221b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d221b-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d221b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d221b-128">輸入</span><span class="sxs-lookup"><span data-stu-id="d221b-128">INPUTS</span></span>

### <span data-ttu-id="d221b-129">所有</span><span class="sxs-lookup"><span data-stu-id="d221b-129">None</span></span>

## <span data-ttu-id="d221b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="d221b-130">OUTPUTS</span></span>

### <span data-ttu-id="d221b-131">失去</span><span class="sxs-lookup"><span data-stu-id="d221b-131">Void</span></span>

## <span data-ttu-id="d221b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="d221b-132">NOTES</span></span>
* <span data-ttu-id="d221b-133">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="d221b-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="d221b-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="d221b-134">RELATED LINKS</span></span>

[<span data-ttu-id="d221b-135">移除-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="d221b-135">Remove-AzureRmRedisCacheDiagnostics</span></span>](./Remove-AzureRmRedisCacheDiagnostics.md)


