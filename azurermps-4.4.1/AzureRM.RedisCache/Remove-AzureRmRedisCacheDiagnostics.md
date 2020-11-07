---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: 9eb2d3a0dfa960ecd3b3b66ce44a01de64d7f5bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623647"
---
# <span data-ttu-id="f97cc-101">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="f97cc-101">Remove-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="f97cc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f97cc-102">SYNOPSIS</span></span>
<span data-ttu-id="f97cc-103">在 Azure Redis Cache 上停用診斷。</span><span class="sxs-lookup"><span data-stu-id="f97cc-103">Disables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f97cc-104">句法</span><span class="sxs-lookup"><span data-stu-id="f97cc-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCacheDiagnostics -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f97cc-105">說明</span><span class="sxs-lookup"><span data-stu-id="f97cc-105">DESCRIPTION</span></span>
<span data-ttu-id="f97cc-106">**AzureRmRedisCacheDiagnostics** Cmdlet 會在 Azure Redis Cache 上停用診斷。</span><span class="sxs-lookup"><span data-stu-id="f97cc-106">The **Remove-AzureRmRedisCacheDiagnostics** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="f97cc-107">示例</span><span class="sxs-lookup"><span data-stu-id="f97cc-107">EXAMPLES</span></span>

### <span data-ttu-id="f97cc-108">範例1：停用診斷</span><span class="sxs-lookup"><span data-stu-id="f97cc-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="f97cc-109">這個命令會停用指定 Azure Redis Cache 的診斷。</span><span class="sxs-lookup"><span data-stu-id="f97cc-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>

<span data-ttu-id="f97cc-110">這會針對訂閱的同一區域中的所有 Azure Redis 緩存停用診斷功能。</span><span class="sxs-lookup"><span data-stu-id="f97cc-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="f97cc-111">參數</span><span class="sxs-lookup"><span data-stu-id="f97cc-111">PARAMETERS</span></span>

### <span data-ttu-id="f97cc-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="f97cc-112">-Name</span></span>
<span data-ttu-id="f97cc-113">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="f97cc-113">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="f97cc-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f97cc-114">-ResourceGroupName</span></span>
<span data-ttu-id="f97cc-115">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f97cc-115">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="f97cc-116">-確認</span><span class="sxs-lookup"><span data-stu-id="f97cc-116">-Confirm</span></span>
<span data-ttu-id="f97cc-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f97cc-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f97cc-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f97cc-118">-WhatIf</span></span>
<span data-ttu-id="f97cc-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f97cc-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f97cc-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f97cc-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f97cc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f97cc-121">-DefaultProfile</span></span>
<span data-ttu-id="f97cc-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f97cc-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f97cc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f97cc-123">CommonParameters</span></span>
<span data-ttu-id="f97cc-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f97cc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f97cc-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f97cc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f97cc-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f97cc-126">INPUTS</span></span>

### <span data-ttu-id="f97cc-127">所有</span><span class="sxs-lookup"><span data-stu-id="f97cc-127">None</span></span>

## <span data-ttu-id="f97cc-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f97cc-128">OUTPUTS</span></span>

### <span data-ttu-id="f97cc-129">失去</span><span class="sxs-lookup"><span data-stu-id="f97cc-129">Void</span></span>

## <span data-ttu-id="f97cc-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f97cc-130">NOTES</span></span>
* <span data-ttu-id="f97cc-131">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="f97cc-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="f97cc-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f97cc-132">RELATED LINKS</span></span>

[<span data-ttu-id="f97cc-133">Set-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="f97cc-133">Set-AzureRmRedisCacheDiagnostics</span></span>](./Set-AzureRmRedisCacheDiagnostics.md)


