---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/powershell/module/az.rediscache/reset-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
ms.openlocfilehash: 797ea800962e00dfd94e1be14e39293fc303ef38
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914685"
---
# <span data-ttu-id="b5510-101">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b5510-101">Reset-AzRedisCache</span></span>

## <span data-ttu-id="b5510-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b5510-102">SYNOPSIS</span></span>
<span data-ttu-id="b5510-103">重新開機緩存的節點。</span><span class="sxs-lookup"><span data-stu-id="b5510-103">Restarts nodes of a cache.</span></span>

## <span data-ttu-id="b5510-104">語法</span><span class="sxs-lookup"><span data-stu-id="b5510-104">SYNTAX</span></span>

```
Reset-AzRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5510-105">描述</span><span class="sxs-lookup"><span data-stu-id="b5510-105">DESCRIPTION</span></span>
<span data-ttu-id="b5510-106">**Reset-AzRedisCache** Cmdlet 會重新開機 Azure Redis Cache 實例的節點。</span><span class="sxs-lookup"><span data-stu-id="b5510-106">The **Reset-AzRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="b5510-107">例子</span><span class="sxs-lookup"><span data-stu-id="b5510-107">EXAMPLES</span></span>

### <span data-ttu-id="b5510-108">範例 1：重新開機兩個節點</span><span class="sxs-lookup"><span data-stu-id="b5510-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="b5510-109">此命令會重新開機名為 RedisCache06 的緩存的兩個節點。</span><span class="sxs-lookup"><span data-stu-id="b5510-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="b5510-110">參數</span><span class="sxs-lookup"><span data-stu-id="b5510-110">PARAMETERS</span></span>

### <span data-ttu-id="b5510-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5510-111">-DefaultProfile</span></span>
<span data-ttu-id="b5510-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b5510-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5510-113">-強制</span><span class="sxs-lookup"><span data-stu-id="b5510-113">-Force</span></span>
<span data-ttu-id="b5510-114">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b5510-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b5510-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="b5510-115">-Name</span></span>
<span data-ttu-id="b5510-116">指定緩存的名稱。</span><span class="sxs-lookup"><span data-stu-id="b5510-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="b5510-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5510-117">-PassThru</span></span>
<span data-ttu-id="b5510-118">表示此 Cmdlet 會返回布林值，指出作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="b5510-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="b5510-119">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b5510-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b5510-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="b5510-120">-RebootType</span></span>
<span data-ttu-id="b5510-121">指定要重新開機的節點或節點。</span><span class="sxs-lookup"><span data-stu-id="b5510-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="b5510-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b5510-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b5510-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="b5510-123">PrimaryNode</span></span> 
- <span data-ttu-id="b5510-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="b5510-124">SecondaryNode</span></span> 
- <span data-ttu-id="b5510-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="b5510-125">AllNodes</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryNode, SecondaryNode, AllNodes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5510-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5510-126">-ResourceGroupName</span></span>
<span data-ttu-id="b5510-127">指定包含該緩存的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b5510-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="b5510-128">-S有型</span><span class="sxs-lookup"><span data-stu-id="b5510-128">-ShardId</span></span>
<span data-ttu-id="b5510-129">指定此 Cmdlet 會針對已啟用集區之進位緩存重新開機的 s一板識別碼。</span><span class="sxs-lookup"><span data-stu-id="b5510-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5510-130">-確認</span><span class="sxs-lookup"><span data-stu-id="b5510-130">-Confirm</span></span>
<span data-ttu-id="b5510-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b5510-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5510-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5510-132">-WhatIf</span></span>
<span data-ttu-id="b5510-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b5510-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5510-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b5510-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5510-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5510-135">CommonParameters</span></span>
<span data-ttu-id="b5510-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b5510-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5510-137">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b5510-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5510-138">輸入</span><span class="sxs-lookup"><span data-stu-id="b5510-138">INPUTS</span></span>

### <span data-ttu-id="b5510-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b5510-139">System.String</span></span>

### <span data-ttu-id="b5510-140">System.Nullable'1[[System.Int32， System.Private.CoreLib， Version=4.0.0.0， Culture=neutral， PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b5510-140">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b5510-141">輸出</span><span class="sxs-lookup"><span data-stu-id="b5510-141">OUTPUTS</span></span>

### <span data-ttu-id="b5510-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b5510-142">System.Boolean</span></span>

## <span data-ttu-id="b5510-143">筆記</span><span class="sxs-lookup"><span data-stu-id="b5510-143">NOTES</span></span>
* <span data-ttu-id="b5510-144">關鍵字：azure、azurerm、arm、resource、management、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="b5510-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="b5510-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5510-145">RELATED LINKS</span></span>

[<span data-ttu-id="b5510-146">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b5510-146">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="b5510-147">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b5510-147">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="b5510-148">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b5510-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="b5510-149">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b5510-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="b5510-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b5510-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


