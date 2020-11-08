---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/reset-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Reset-AzRedisCache.md
ms.openlocfilehash: c2373bb4ef093a35abc12b14f55f4c977fc54d64
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127401"
---
# <span data-ttu-id="3e5d7-101">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3e5d7-101">Reset-AzRedisCache</span></span>

## <span data-ttu-id="3e5d7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3e5d7-102">SYNOPSIS</span></span>
<span data-ttu-id="3e5d7-103">重新開機快取的節點。</span><span class="sxs-lookup"><span data-stu-id="3e5d7-103">Restarts nodes of a cache.</span></span>

## <span data-ttu-id="3e5d7-104">句法</span><span class="sxs-lookup"><span data-stu-id="3e5d7-104">SYNTAX</span></span>

```
Reset-AzRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e5d7-105">說明</span><span class="sxs-lookup"><span data-stu-id="3e5d7-105">DESCRIPTION</span></span>
<span data-ttu-id="3e5d7-106">**Reset AzRedisCache** Cmdlet 會重新開機 Azure Redis Cache 實例的節點。</span><span class="sxs-lookup"><span data-stu-id="3e5d7-106">The **Reset-AzRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="3e5d7-107">示例</span><span class="sxs-lookup"><span data-stu-id="3e5d7-107">EXAMPLES</span></span>

### <span data-ttu-id="3e5d7-108">範例1：重新開機兩個節點</span><span class="sxs-lookup"><span data-stu-id="3e5d7-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="3e5d7-109">這個命令會重新開機名為 RedisCache06 的快取節點。</span><span class="sxs-lookup"><span data-stu-id="3e5d7-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="3e5d7-110">參數</span><span class="sxs-lookup"><span data-stu-id="3e5d7-110">PARAMETERS</span></span>

### <span data-ttu-id="3e5d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e5d7-111">-DefaultProfile</span></span>
<span data-ttu-id="3e5d7-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e5d7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e5d7-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3e5d7-113">-Force</span></span>
<span data-ttu-id="3e5d7-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="3e5d7-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3e5d7-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="3e5d7-115">-Name</span></span>
<span data-ttu-id="3e5d7-116">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e5d7-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="3e5d7-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e5d7-117">-PassThru</span></span>
<span data-ttu-id="3e5d7-118">指示這個 Cmdlet 會傳回一個布林值，指出該作業是否會成功。</span><span class="sxs-lookup"><span data-stu-id="3e5d7-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="3e5d7-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="3e5d7-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3e5d7-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="3e5d7-120">-RebootType</span></span>
<span data-ttu-id="3e5d7-121">指定要重新開機的一個或哪些節點。</span><span class="sxs-lookup"><span data-stu-id="3e5d7-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="3e5d7-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3e5d7-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3e5d7-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="3e5d7-123">PrimaryNode</span></span> 
- <span data-ttu-id="3e5d7-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="3e5d7-124">SecondaryNode</span></span> 
- <span data-ttu-id="3e5d7-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="3e5d7-125">AllNodes</span></span>

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

### <span data-ttu-id="3e5d7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e5d7-126">-ResourceGroupName</span></span>
<span data-ttu-id="3e5d7-127">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e5d7-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="3e5d7-128">-ShardId</span><span class="sxs-lookup"><span data-stu-id="3e5d7-128">-ShardId</span></span>
<span data-ttu-id="3e5d7-129">指定此 Cmdlet 針對啟用群集的 premium 快取重新開機的 shard 識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e5d7-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

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

### <span data-ttu-id="3e5d7-130">-確認</span><span class="sxs-lookup"><span data-stu-id="3e5d7-130">-Confirm</span></span>
<span data-ttu-id="3e5d7-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3e5d7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e5d7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e5d7-132">-WhatIf</span></span>
<span data-ttu-id="3e5d7-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3e5d7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e5d7-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3e5d7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e5d7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e5d7-135">CommonParameters</span></span>
<span data-ttu-id="3e5d7-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3e5d7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e5d7-137">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3e5d7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e5d7-138">輸入</span><span class="sxs-lookup"><span data-stu-id="3e5d7-138">INPUTS</span></span>

### <span data-ttu-id="3e5d7-139">System.object</span><span class="sxs-lookup"><span data-stu-id="3e5d7-139">System.String</span></span>

### <span data-ttu-id="3e5d7-140">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3e5d7-140">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3e5d7-141">輸出</span><span class="sxs-lookup"><span data-stu-id="3e5d7-141">OUTPUTS</span></span>

### <span data-ttu-id="3e5d7-142">System.object</span><span class="sxs-lookup"><span data-stu-id="3e5d7-142">System.Boolean</span></span>

## <span data-ttu-id="3e5d7-143">筆記</span><span class="sxs-lookup"><span data-stu-id="3e5d7-143">NOTES</span></span>
* <span data-ttu-id="3e5d7-144">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="3e5d7-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="3e5d7-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e5d7-145">RELATED LINKS</span></span>

[<span data-ttu-id="3e5d7-146">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3e5d7-146">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="3e5d7-147">匯入-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3e5d7-147">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="3e5d7-148">新-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3e5d7-148">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="3e5d7-149">移除-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3e5d7-149">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="3e5d7-150">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="3e5d7-150">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


