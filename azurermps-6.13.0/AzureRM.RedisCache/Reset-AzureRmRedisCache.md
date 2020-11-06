---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/reset-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
ms.openlocfilehash: 8aad14bde950a5e98d8d9331428a62e957cb0afe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455076"
---
# <span data-ttu-id="5c353-101">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="5c353-101">Reset-AzureRmRedisCache</span></span>

## <span data-ttu-id="5c353-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5c353-102">SYNOPSIS</span></span>
<span data-ttu-id="5c353-103">重新開機快取的節點。</span><span class="sxs-lookup"><span data-stu-id="5c353-103">Restarts nodes of a cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c353-104">句法</span><span class="sxs-lookup"><span data-stu-id="5c353-104">SYNTAX</span></span>

```
Reset-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c353-105">說明</span><span class="sxs-lookup"><span data-stu-id="5c353-105">DESCRIPTION</span></span>
<span data-ttu-id="5c353-106">**Reset AzureRmRedisCache** Cmdlet 會重新開機 Azure Redis Cache 實例的節點。</span><span class="sxs-lookup"><span data-stu-id="5c353-106">The **Reset-AzureRmRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="5c353-107">示例</span><span class="sxs-lookup"><span data-stu-id="5c353-107">EXAMPLES</span></span>

### <span data-ttu-id="5c353-108">範例1：重新開機兩個節點</span><span class="sxs-lookup"><span data-stu-id="5c353-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="5c353-109">這個命令會重新開機名為 RedisCache06 的快取節點。</span><span class="sxs-lookup"><span data-stu-id="5c353-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="5c353-110">參數</span><span class="sxs-lookup"><span data-stu-id="5c353-110">PARAMETERS</span></span>

### <span data-ttu-id="5c353-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c353-111">-DefaultProfile</span></span>
<span data-ttu-id="5c353-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5c353-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c353-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5c353-113">-Force</span></span>
<span data-ttu-id="5c353-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="5c353-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5c353-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="5c353-115">-Name</span></span>
<span data-ttu-id="5c353-116">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c353-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="5c353-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c353-117">-PassThru</span></span>
<span data-ttu-id="5c353-118">指示這個 Cmdlet 會傳回一個布林值，指出該作業是否會成功。</span><span class="sxs-lookup"><span data-stu-id="5c353-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="5c353-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="5c353-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5c353-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="5c353-120">-RebootType</span></span>
<span data-ttu-id="5c353-121">指定要重新開機的一個或哪些節點。</span><span class="sxs-lookup"><span data-stu-id="5c353-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="5c353-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5c353-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5c353-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="5c353-123">PrimaryNode</span></span> 
- <span data-ttu-id="5c353-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="5c353-124">SecondaryNode</span></span> 
- <span data-ttu-id="5c353-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="5c353-125">AllNodes</span></span>

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

### <span data-ttu-id="5c353-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c353-126">-ResourceGroupName</span></span>
<span data-ttu-id="5c353-127">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5c353-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="5c353-128">-ShardId</span><span class="sxs-lookup"><span data-stu-id="5c353-128">-ShardId</span></span>
<span data-ttu-id="5c353-129">指定此 Cmdlet 針對啟用群集的 premium 快取重新開機的 shard 識別碼。</span><span class="sxs-lookup"><span data-stu-id="5c353-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

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

### <span data-ttu-id="5c353-130">-確認</span><span class="sxs-lookup"><span data-stu-id="5c353-130">-Confirm</span></span>
<span data-ttu-id="5c353-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5c353-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c353-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c353-132">-WhatIf</span></span>
<span data-ttu-id="5c353-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5c353-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c353-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5c353-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c353-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c353-135">CommonParameters</span></span>
<span data-ttu-id="5c353-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5c353-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c353-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5c353-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c353-138">輸入</span><span class="sxs-lookup"><span data-stu-id="5c353-138">INPUTS</span></span>

### <span data-ttu-id="5c353-139">System.object</span><span class="sxs-lookup"><span data-stu-id="5c353-139">System.String</span></span>

### <span data-ttu-id="5c353-140">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="5c353-140">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="5c353-141">輸出</span><span class="sxs-lookup"><span data-stu-id="5c353-141">OUTPUTS</span></span>

### <span data-ttu-id="5c353-142">System.object</span><span class="sxs-lookup"><span data-stu-id="5c353-142">System.Boolean</span></span>

## <span data-ttu-id="5c353-143">筆記</span><span class="sxs-lookup"><span data-stu-id="5c353-143">NOTES</span></span>
* <span data-ttu-id="5c353-144">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="5c353-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="5c353-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="5c353-145">RELATED LINKS</span></span>

[<span data-ttu-id="5c353-146">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="5c353-146">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="5c353-147">匯入-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="5c353-147">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="5c353-148">新-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="5c353-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="5c353-149">移除-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="5c353-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="5c353-150">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="5c353-150">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


