---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/reset-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
ms.openlocfilehash: df306f6bf97d47d87a78d0cefecff6c4d89020aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448587"
---
# <span data-ttu-id="bde2d-101">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="bde2d-101">Reset-AzureRmRedisCache</span></span>

## <span data-ttu-id="bde2d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bde2d-102">SYNOPSIS</span></span>
<span data-ttu-id="bde2d-103">重新開機快取的節點。</span><span class="sxs-lookup"><span data-stu-id="bde2d-103">Restarts nodes of a cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bde2d-104">句法</span><span class="sxs-lookup"><span data-stu-id="bde2d-104">SYNTAX</span></span>

```
Reset-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bde2d-105">說明</span><span class="sxs-lookup"><span data-stu-id="bde2d-105">DESCRIPTION</span></span>
<span data-ttu-id="bde2d-106">**Reset AzureRmRedisCache** Cmdlet 會重新開機 Azure Redis Cache 實例的節點。</span><span class="sxs-lookup"><span data-stu-id="bde2d-106">The **Reset-AzureRmRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="bde2d-107">示例</span><span class="sxs-lookup"><span data-stu-id="bde2d-107">EXAMPLES</span></span>

### <span data-ttu-id="bde2d-108">範例1：重新開機兩個節點</span><span class="sxs-lookup"><span data-stu-id="bde2d-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="bde2d-109">這個命令會重新開機名為 RedisCache06 的快取節點。</span><span class="sxs-lookup"><span data-stu-id="bde2d-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="bde2d-110">參數</span><span class="sxs-lookup"><span data-stu-id="bde2d-110">PARAMETERS</span></span>

### <span data-ttu-id="bde2d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bde2d-111">-DefaultProfile</span></span>
<span data-ttu-id="bde2d-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bde2d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bde2d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="bde2d-113">-Force</span></span>
<span data-ttu-id="bde2d-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="bde2d-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bde2d-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="bde2d-115">-Name</span></span>
<span data-ttu-id="bde2d-116">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="bde2d-116">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="bde2d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bde2d-117">-PassThru</span></span>
<span data-ttu-id="bde2d-118">指示這個 Cmdlet 會傳回一個布林值，指出該作業是否會成功。</span><span class="sxs-lookup"><span data-stu-id="bde2d-118">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="bde2d-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="bde2d-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bde2d-120">-RebootType</span><span class="sxs-lookup"><span data-stu-id="bde2d-120">-RebootType</span></span>
<span data-ttu-id="bde2d-121">指定要重新開機的一個或哪些節點。</span><span class="sxs-lookup"><span data-stu-id="bde2d-121">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="bde2d-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="bde2d-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bde2d-123">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="bde2d-123">PrimaryNode</span></span> 
- <span data-ttu-id="bde2d-124">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="bde2d-124">SecondaryNode</span></span> 
- <span data-ttu-id="bde2d-125">AllNodes</span><span class="sxs-lookup"><span data-stu-id="bde2d-125">AllNodes</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryNode, SecondaryNode, AllNodes

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bde2d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bde2d-126">-ResourceGroupName</span></span>
<span data-ttu-id="bde2d-127">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bde2d-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="bde2d-128">-ShardId</span><span class="sxs-lookup"><span data-stu-id="bde2d-128">-ShardId</span></span>
<span data-ttu-id="bde2d-129">指定此 Cmdlet 針對啟用群集的 premium 快取重新開機的 shard 識別碼。</span><span class="sxs-lookup"><span data-stu-id="bde2d-129">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bde2d-130">-確認</span><span class="sxs-lookup"><span data-stu-id="bde2d-130">-Confirm</span></span>
<span data-ttu-id="bde2d-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bde2d-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bde2d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bde2d-132">-WhatIf</span></span>
<span data-ttu-id="bde2d-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bde2d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bde2d-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bde2d-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bde2d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bde2d-135">CommonParameters</span></span>
<span data-ttu-id="bde2d-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bde2d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bde2d-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bde2d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bde2d-138">輸入</span><span class="sxs-lookup"><span data-stu-id="bde2d-138">INPUTS</span></span>

### <span data-ttu-id="bde2d-139">所有</span><span class="sxs-lookup"><span data-stu-id="bde2d-139">None</span></span>
<span data-ttu-id="bde2d-140">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bde2d-140">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="bde2d-141">輸出</span><span class="sxs-lookup"><span data-stu-id="bde2d-141">OUTPUTS</span></span>

### <span data-ttu-id="bde2d-142">所有</span><span class="sxs-lookup"><span data-stu-id="bde2d-142">None</span></span>

## <span data-ttu-id="bde2d-143">筆記</span><span class="sxs-lookup"><span data-stu-id="bde2d-143">NOTES</span></span>
* <span data-ttu-id="bde2d-144">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="bde2d-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="bde2d-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="bde2d-145">RELATED LINKS</span></span>

[<span data-ttu-id="bde2d-146">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="bde2d-146">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="bde2d-147">匯入-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="bde2d-147">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="bde2d-148">新-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="bde2d-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="bde2d-149">移除-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="bde2d-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="bde2d-150">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="bde2d-150">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


