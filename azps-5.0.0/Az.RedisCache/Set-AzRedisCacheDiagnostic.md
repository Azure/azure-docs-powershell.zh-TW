---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
ms.openlocfilehash: 60c552b0878907c7b2c4a56d8068968c3ace862a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94287376"
---
# <span data-ttu-id="440ab-101">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="440ab-101">Set-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="440ab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="440ab-102">SYNOPSIS</span></span>
<span data-ttu-id="440ab-103">啟用 Azure Redis Cache 的診斷。</span><span class="sxs-lookup"><span data-stu-id="440ab-103">Enables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="440ab-104">句法</span><span class="sxs-lookup"><span data-stu-id="440ab-104">SYNTAX</span></span>

```
Set-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="440ab-105">說明</span><span class="sxs-lookup"><span data-stu-id="440ab-105">DESCRIPTION</span></span>
<span data-ttu-id="440ab-106">**AzRedisCacheDiagnostic** Cmdlet 可為 Azure Redis Cache 啟用診斷。</span><span class="sxs-lookup"><span data-stu-id="440ab-106">The **Set-AzRedisCacheDiagnostic** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="440ab-107">示例</span><span class="sxs-lookup"><span data-stu-id="440ab-107">EXAMPLES</span></span>

### <span data-ttu-id="440ab-108">範例1：啟用診斷</span><span class="sxs-lookup"><span data-stu-id="440ab-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="440ab-109">這個命令會啟用 Azure Redis 快取的診斷。</span><span class="sxs-lookup"><span data-stu-id="440ab-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="440ab-110">此命令將針對訂閱的同一區域中的所有 Azure Redis 緩存啟用診斷或更新儲存空間帳戶。</span><span class="sxs-lookup"><span data-stu-id="440ab-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="440ab-111">參數</span><span class="sxs-lookup"><span data-stu-id="440ab-111">PARAMETERS</span></span>

### <span data-ttu-id="440ab-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="440ab-112">-DefaultProfile</span></span>
<span data-ttu-id="440ab-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="440ab-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="440ab-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="440ab-114">-Name</span></span>
<span data-ttu-id="440ab-115">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="440ab-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="440ab-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="440ab-116">-ResourceGroupName</span></span>
<span data-ttu-id="440ab-117">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="440ab-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="440ab-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="440ab-118">-StorageAccountId</span></span>
<span data-ttu-id="440ab-119">指定用來儲存診斷資料之儲存空間帳戶的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="440ab-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="440ab-120">-確認</span><span class="sxs-lookup"><span data-stu-id="440ab-120">-Confirm</span></span>
<span data-ttu-id="440ab-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="440ab-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="440ab-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="440ab-122">-WhatIf</span></span>
<span data-ttu-id="440ab-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="440ab-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="440ab-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="440ab-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="440ab-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="440ab-125">CommonParameters</span></span>
<span data-ttu-id="440ab-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="440ab-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="440ab-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="440ab-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="440ab-128">輸入</span><span class="sxs-lookup"><span data-stu-id="440ab-128">INPUTS</span></span>

### <span data-ttu-id="440ab-129">System.object</span><span class="sxs-lookup"><span data-stu-id="440ab-129">System.String</span></span>

## <span data-ttu-id="440ab-130">輸出</span><span class="sxs-lookup"><span data-stu-id="440ab-130">OUTPUTS</span></span>

### <span data-ttu-id="440ab-131">System.void</span><span class="sxs-lookup"><span data-stu-id="440ab-131">System.Void</span></span>

## <span data-ttu-id="440ab-132">筆記</span><span class="sxs-lookup"><span data-stu-id="440ab-132">NOTES</span></span>
* <span data-ttu-id="440ab-133">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="440ab-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="440ab-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="440ab-134">RELATED LINKS</span></span>

[<span data-ttu-id="440ab-135">移除-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="440ab-135">Remove-AzRedisCacheDiagnostic</span></span>](./Remove-AzRedisCacheDiagnostic.md)


