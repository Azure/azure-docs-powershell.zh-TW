---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/powershell/module/az.rediscache/set-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
ms.openlocfilehash: ee6e2848325222d86271bfd70705ec7aa855cbb6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914677"
---
# <span data-ttu-id="ac7ce-101">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ac7ce-101">Set-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="ac7ce-102">簡介</span><span class="sxs-lookup"><span data-stu-id="ac7ce-102">SYNOPSIS</span></span>
<span data-ttu-id="ac7ce-103">在 Azure Redis Cache 上啟用診斷。</span><span class="sxs-lookup"><span data-stu-id="ac7ce-103">Enables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="ac7ce-104">語法</span><span class="sxs-lookup"><span data-stu-id="ac7ce-104">SYNTAX</span></span>

```
Set-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac7ce-105">描述</span><span class="sxs-lookup"><span data-stu-id="ac7ce-105">DESCRIPTION</span></span>
<span data-ttu-id="ac7ce-106">**Set-AzRedisCacheDiagnostic** Cmdlet 可針對 Azure Redis Cache 啟用診斷。</span><span class="sxs-lookup"><span data-stu-id="ac7ce-106">The **Set-AzRedisCacheDiagnostic** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="ac7ce-107">例子</span><span class="sxs-lookup"><span data-stu-id="ac7ce-107">EXAMPLES</span></span>

### <span data-ttu-id="ac7ce-108">範例 1：啟用診斷</span><span class="sxs-lookup"><span data-stu-id="ac7ce-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="ac7ce-109">此命令會啟用 Azure Redis 緩存的診斷。</span><span class="sxs-lookup"><span data-stu-id="ac7ce-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="ac7ce-110">此命令將針對訂閱的相同區域的所有 Azure Redis 快用啟用診斷或更新儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="ac7ce-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="ac7ce-111">參數</span><span class="sxs-lookup"><span data-stu-id="ac7ce-111">PARAMETERS</span></span>

### <span data-ttu-id="ac7ce-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac7ce-112">-DefaultProfile</span></span>
<span data-ttu-id="ac7ce-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="ac7ce-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac7ce-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="ac7ce-114">-Name</span></span>
<span data-ttu-id="ac7ce-115">指定緩存的名稱。</span><span class="sxs-lookup"><span data-stu-id="ac7ce-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="ac7ce-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac7ce-116">-ResourceGroupName</span></span>
<span data-ttu-id="ac7ce-117">指定包含該緩存的資源組名。</span><span class="sxs-lookup"><span data-stu-id="ac7ce-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="ac7ce-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ac7ce-118">-StorageAccountId</span></span>
<span data-ttu-id="ac7ce-119">指定用來儲存診斷資料之儲存空間帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ac7ce-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="ac7ce-120">-確認</span><span class="sxs-lookup"><span data-stu-id="ac7ce-120">-Confirm</span></span>
<span data-ttu-id="ac7ce-121">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="ac7ce-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac7ce-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac7ce-122">-WhatIf</span></span>
<span data-ttu-id="ac7ce-123">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ac7ce-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac7ce-124">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ac7ce-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac7ce-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac7ce-125">CommonParameters</span></span>
<span data-ttu-id="ac7ce-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="ac7ce-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac7ce-127">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="ac7ce-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac7ce-128">輸入</span><span class="sxs-lookup"><span data-stu-id="ac7ce-128">INPUTS</span></span>

### <span data-ttu-id="ac7ce-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ac7ce-129">System.String</span></span>

## <span data-ttu-id="ac7ce-130">輸出</span><span class="sxs-lookup"><span data-stu-id="ac7ce-130">OUTPUTS</span></span>

### <span data-ttu-id="ac7ce-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="ac7ce-131">System.Void</span></span>

## <span data-ttu-id="ac7ce-132">筆記</span><span class="sxs-lookup"><span data-stu-id="ac7ce-132">NOTES</span></span>
* <span data-ttu-id="ac7ce-133">關鍵字：azure、azurerm、arm、resource、management、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="ac7ce-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="ac7ce-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="ac7ce-134">RELATED LINKS</span></span>

[<span data-ttu-id="ac7ce-135">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="ac7ce-135">Remove-AzRedisCacheDiagnostic</span></span>](./Remove-AzRedisCacheDiagnostic.md)


