---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
ms.openlocfilehash: b309875fd330df5695283c187e454556669b6652
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94128639"
---
# <span data-ttu-id="52cd3-101">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="52cd3-101">Remove-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="52cd3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="52cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="52cd3-103">在 Azure Redis Cache 上停用診斷。</span><span class="sxs-lookup"><span data-stu-id="52cd3-103">Disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="52cd3-104">句法</span><span class="sxs-lookup"><span data-stu-id="52cd3-104">SYNTAX</span></span>

```
Remove-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52cd3-105">說明</span><span class="sxs-lookup"><span data-stu-id="52cd3-105">DESCRIPTION</span></span>
<span data-ttu-id="52cd3-106">**AzRedisCacheDiagnostic** Cmdlet 會在 Azure Redis Cache 上停用診斷。</span><span class="sxs-lookup"><span data-stu-id="52cd3-106">The **Remove-AzRedisCacheDiagnostic** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="52cd3-107">示例</span><span class="sxs-lookup"><span data-stu-id="52cd3-107">EXAMPLES</span></span>

### <span data-ttu-id="52cd3-108">範例1：停用診斷</span><span class="sxs-lookup"><span data-stu-id="52cd3-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="52cd3-109">這個命令會停用指定 Azure Redis Cache 的診斷。</span><span class="sxs-lookup"><span data-stu-id="52cd3-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="52cd3-110">這會針對訂閱的同一區域中的所有 Azure Redis 緩存停用診斷功能。</span><span class="sxs-lookup"><span data-stu-id="52cd3-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="52cd3-111">參數</span><span class="sxs-lookup"><span data-stu-id="52cd3-111">PARAMETERS</span></span>

### <span data-ttu-id="52cd3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52cd3-112">-DefaultProfile</span></span>
<span data-ttu-id="52cd3-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="52cd3-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52cd3-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="52cd3-114">-Name</span></span>
<span data-ttu-id="52cd3-115">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="52cd3-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="52cd3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52cd3-116">-ResourceGroupName</span></span>
<span data-ttu-id="52cd3-117">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="52cd3-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="52cd3-118">-確認</span><span class="sxs-lookup"><span data-stu-id="52cd3-118">-Confirm</span></span>
<span data-ttu-id="52cd3-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="52cd3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52cd3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52cd3-120">-WhatIf</span></span>
<span data-ttu-id="52cd3-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="52cd3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52cd3-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52cd3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52cd3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52cd3-123">CommonParameters</span></span>
<span data-ttu-id="52cd3-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="52cd3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52cd3-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="52cd3-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52cd3-126">輸入</span><span class="sxs-lookup"><span data-stu-id="52cd3-126">INPUTS</span></span>

### <span data-ttu-id="52cd3-127">System.object</span><span class="sxs-lookup"><span data-stu-id="52cd3-127">System.String</span></span>

## <span data-ttu-id="52cd3-128">輸出</span><span class="sxs-lookup"><span data-stu-id="52cd3-128">OUTPUTS</span></span>

### <span data-ttu-id="52cd3-129">System.void</span><span class="sxs-lookup"><span data-stu-id="52cd3-129">System.Void</span></span>

## <span data-ttu-id="52cd3-130">筆記</span><span class="sxs-lookup"><span data-stu-id="52cd3-130">NOTES</span></span>
* <span data-ttu-id="52cd3-131">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="52cd3-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="52cd3-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="52cd3-132">RELATED LINKS</span></span>

[<span data-ttu-id="52cd3-133">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="52cd3-133">Set-AzRedisCacheDiagnostic</span></span>](./Set-AzRedisCacheDiagnostic.md)


