---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/powershell/module/az.rediscache/remove-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
ms.openlocfilehash: d32fe3286a8c6e4b723137f8b20921c79caa45be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910386"
---
# <span data-ttu-id="a2c29-101">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="a2c29-101">Remove-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="a2c29-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a2c29-102">SYNOPSIS</span></span>
<span data-ttu-id="a2c29-103">停用 Azure Redis Cache 上的診斷。</span><span class="sxs-lookup"><span data-stu-id="a2c29-103">Disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="a2c29-104">語法</span><span class="sxs-lookup"><span data-stu-id="a2c29-104">SYNTAX</span></span>

```
Remove-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2c29-105">描述</span><span class="sxs-lookup"><span data-stu-id="a2c29-105">DESCRIPTION</span></span>
<span data-ttu-id="a2c29-106">**Remove-AzRedisCacheDiagnostic** Cmdlet 會停用 Azure Redis Cache 上的診斷。</span><span class="sxs-lookup"><span data-stu-id="a2c29-106">The **Remove-AzRedisCacheDiagnostic** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="a2c29-107">例子</span><span class="sxs-lookup"><span data-stu-id="a2c29-107">EXAMPLES</span></span>

### <span data-ttu-id="a2c29-108">範例 1：停用診斷</span><span class="sxs-lookup"><span data-stu-id="a2c29-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="a2c29-109">此命令會停用指定 Azure Redis Cache 上的診斷。</span><span class="sxs-lookup"><span data-stu-id="a2c29-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="a2c29-110">這會停用訂閱同一地區內所有 Azure Redis Caches 的診斷。</span><span class="sxs-lookup"><span data-stu-id="a2c29-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="a2c29-111">參數</span><span class="sxs-lookup"><span data-stu-id="a2c29-111">PARAMETERS</span></span>

### <span data-ttu-id="a2c29-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2c29-112">-DefaultProfile</span></span>
<span data-ttu-id="a2c29-113">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2c29-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2c29-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="a2c29-114">-Name</span></span>
<span data-ttu-id="a2c29-115">指定緩存的名稱。</span><span class="sxs-lookup"><span data-stu-id="a2c29-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="a2c29-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2c29-116">-ResourceGroupName</span></span>
<span data-ttu-id="a2c29-117">指定包含該緩存的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a2c29-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="a2c29-118">-確認</span><span class="sxs-lookup"><span data-stu-id="a2c29-118">-Confirm</span></span>
<span data-ttu-id="a2c29-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a2c29-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2c29-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2c29-120">-WhatIf</span></span>
<span data-ttu-id="a2c29-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a2c29-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2c29-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a2c29-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2c29-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2c29-123">CommonParameters</span></span>
<span data-ttu-id="a2c29-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a2c29-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2c29-125">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a2c29-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2c29-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a2c29-126">INPUTS</span></span>

### <span data-ttu-id="a2c29-127">System.String</span><span class="sxs-lookup"><span data-stu-id="a2c29-127">System.String</span></span>

## <span data-ttu-id="a2c29-128">輸出</span><span class="sxs-lookup"><span data-stu-id="a2c29-128">OUTPUTS</span></span>

### <span data-ttu-id="a2c29-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="a2c29-129">System.Void</span></span>

## <span data-ttu-id="a2c29-130">筆記</span><span class="sxs-lookup"><span data-stu-id="a2c29-130">NOTES</span></span>
* <span data-ttu-id="a2c29-131">關鍵字：azure、azurerm、arm、resource、management、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="a2c29-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="a2c29-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2c29-132">RELATED LINKS</span></span>

[<span data-ttu-id="a2c29-133">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="a2c29-133">Set-AzRedisCacheDiagnostic</span></span>](./Set-AzRedisCacheDiagnostic.md)


