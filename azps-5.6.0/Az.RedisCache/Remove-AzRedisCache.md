---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/powershell/module/az.rediscache/remove-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
ms.openlocfilehash: 2ae4c2d5de8eeba370c981ceb5a94baa1ba91cf2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903954"
---
# <span data-ttu-id="49a81-101">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="49a81-101">Remove-AzRedisCache</span></span>

## <span data-ttu-id="49a81-102">簡介</span><span class="sxs-lookup"><span data-stu-id="49a81-102">SYNOPSIS</span></span>
<span data-ttu-id="49a81-103">移除 Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="49a81-103">Removes a Redis Cache.</span></span>

## <span data-ttu-id="49a81-104">語法</span><span class="sxs-lookup"><span data-stu-id="49a81-104">SYNTAX</span></span>

```
Remove-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49a81-105">描述</span><span class="sxs-lookup"><span data-stu-id="49a81-105">DESCRIPTION</span></span>
<span data-ttu-id="49a81-106">**Remove-AzRedisCache** Cmdlet 會移除 Azure Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="49a81-106">The **Remove-AzRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="49a81-107">例子</span><span class="sxs-lookup"><span data-stu-id="49a81-107">EXAMPLES</span></span>

### <span data-ttu-id="49a81-108">範例 1：移除 Redis Cache 並返回結果</span><span class="sxs-lookup"><span data-stu-id="49a81-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="49a81-109">此命令會移除 Redis Cache，並顯示作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="49a81-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="49a81-110">範例 2：移除 Redis Cache 且不顯示結果</span><span class="sxs-lookup"><span data-stu-id="49a81-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="49a81-111">此命令會移除 Redis Cache。</span><span class="sxs-lookup"><span data-stu-id="49a81-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="49a81-112">由於 *未指定 PassThru* 參數，因此不會顯示作業的結果。</span><span class="sxs-lookup"><span data-stu-id="49a81-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="49a81-113">參數</span><span class="sxs-lookup"><span data-stu-id="49a81-113">PARAMETERS</span></span>

### <span data-ttu-id="49a81-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a81-114">-DefaultProfile</span></span>
<span data-ttu-id="49a81-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="49a81-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49a81-116">-強制</span><span class="sxs-lookup"><span data-stu-id="49a81-116">-Force</span></span>
<span data-ttu-id="49a81-117">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="49a81-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="49a81-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="49a81-118">-Name</span></span>
<span data-ttu-id="49a81-119">指定要移除的 Redis Cache 名稱。</span><span class="sxs-lookup"><span data-stu-id="49a81-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="49a81-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="49a81-120">-PassThru</span></span>
<span data-ttu-id="49a81-121">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="49a81-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="49a81-122">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="49a81-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="49a81-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49a81-123">-ResourceGroupName</span></span>
<span data-ttu-id="49a81-124">指定包含要移除之 Redis Cache 的資源組名。</span><span class="sxs-lookup"><span data-stu-id="49a81-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="49a81-125">-確認</span><span class="sxs-lookup"><span data-stu-id="49a81-125">-Confirm</span></span>
<span data-ttu-id="49a81-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="49a81-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49a81-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49a81-127">-WhatIf</span></span>
<span data-ttu-id="49a81-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="49a81-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49a81-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49a81-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49a81-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a81-130">CommonParameters</span></span>
<span data-ttu-id="49a81-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="49a81-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a81-132">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="49a81-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a81-133">輸入</span><span class="sxs-lookup"><span data-stu-id="49a81-133">INPUTS</span></span>

### <span data-ttu-id="49a81-134">System.String</span><span class="sxs-lookup"><span data-stu-id="49a81-134">System.String</span></span>

## <span data-ttu-id="49a81-135">輸出</span><span class="sxs-lookup"><span data-stu-id="49a81-135">OUTPUTS</span></span>

### <span data-ttu-id="49a81-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="49a81-136">System.Boolean</span></span>

## <span data-ttu-id="49a81-137">筆記</span><span class="sxs-lookup"><span data-stu-id="49a81-137">NOTES</span></span>

## <span data-ttu-id="49a81-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="49a81-138">RELATED LINKS</span></span>

[<span data-ttu-id="49a81-139">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="49a81-139">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="49a81-140">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="49a81-140">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="49a81-141">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="49a81-141">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


