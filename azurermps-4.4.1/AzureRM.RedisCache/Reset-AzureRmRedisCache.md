---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A73D4DDD-387A-4468-AC6E-F15BF473527E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Reset-AzureRmRedisCache.md
ms.openlocfilehash: 2b352c649d01e2fceb42f99a6c4dad20859a2adc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623862"
---
# <span data-ttu-id="7eb94-101">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7eb94-101">Reset-AzureRmRedisCache</span></span>

## <span data-ttu-id="7eb94-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7eb94-102">SYNOPSIS</span></span>
<span data-ttu-id="7eb94-103">重新開機快取的節點。</span><span class="sxs-lookup"><span data-stu-id="7eb94-103">Restarts nodes of a cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eb94-104">句法</span><span class="sxs-lookup"><span data-stu-id="7eb94-104">SYNTAX</span></span>

```
Reset-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -RebootType <String> [-ShardId <Int32>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7eb94-105">說明</span><span class="sxs-lookup"><span data-stu-id="7eb94-105">DESCRIPTION</span></span>
<span data-ttu-id="7eb94-106">**Reset AzureRmRedisCache** Cmdlet 會重新開機 Azure Redis Cache 實例的節點。</span><span class="sxs-lookup"><span data-stu-id="7eb94-106">The **Reset-AzureRmRedisCache** cmdlet restarts nodes of an Azure Redis Cache instance.</span></span>

## <span data-ttu-id="7eb94-107">示例</span><span class="sxs-lookup"><span data-stu-id="7eb94-107">EXAMPLES</span></span>

### <span data-ttu-id="7eb94-108">範例1：重新開機兩個節點</span><span class="sxs-lookup"><span data-stu-id="7eb94-108">Example 1: Restart both nodes</span></span>
```
PS C:\>Reset-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -RebootType "AllNodes" -Force
```

<span data-ttu-id="7eb94-109">這個命令會重新開機名為 RedisCache06 的快取節點。</span><span class="sxs-lookup"><span data-stu-id="7eb94-109">This command restarts both nodes for the cache named RedisCache06.</span></span>

## <span data-ttu-id="7eb94-110">參數</span><span class="sxs-lookup"><span data-stu-id="7eb94-110">PARAMETERS</span></span>

### <span data-ttu-id="7eb94-111">-Force</span><span class="sxs-lookup"><span data-stu-id="7eb94-111">-Force</span></span>
<span data-ttu-id="7eb94-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="7eb94-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7eb94-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="7eb94-113">-Name</span></span>
<span data-ttu-id="7eb94-114">指定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="7eb94-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="7eb94-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7eb94-115">-PassThru</span></span>
<span data-ttu-id="7eb94-116">指示這個 Cmdlet 會傳回一個布林值，指出該作業是否會成功。</span><span class="sxs-lookup"><span data-stu-id="7eb94-116">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="7eb94-117">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="7eb94-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7eb94-118">-RebootType</span><span class="sxs-lookup"><span data-stu-id="7eb94-118">-RebootType</span></span>
<span data-ttu-id="7eb94-119">指定要重新開機的一個或哪些節點。</span><span class="sxs-lookup"><span data-stu-id="7eb94-119">Specifies which node or nodes to restart.</span></span>
<span data-ttu-id="7eb94-120">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="7eb94-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7eb94-121">PrimaryNode</span><span class="sxs-lookup"><span data-stu-id="7eb94-121">PrimaryNode</span></span> 
- <span data-ttu-id="7eb94-122">SecondaryNode</span><span class="sxs-lookup"><span data-stu-id="7eb94-122">SecondaryNode</span></span> 
- <span data-ttu-id="7eb94-123">AllNodes</span><span class="sxs-lookup"><span data-stu-id="7eb94-123">AllNodes</span></span>

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

### <span data-ttu-id="7eb94-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eb94-124">-ResourceGroupName</span></span>
<span data-ttu-id="7eb94-125">指定包含快取的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7eb94-125">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="7eb94-126">-ShardId</span><span class="sxs-lookup"><span data-stu-id="7eb94-126">-ShardId</span></span>
<span data-ttu-id="7eb94-127">指定此 Cmdlet 針對啟用群集的 premium 快取重新開機的 shard 識別碼。</span><span class="sxs-lookup"><span data-stu-id="7eb94-127">Specifies the ID of the shard that this cmdlet restarts for a premium cache with clustering enabled.</span></span>

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

### <span data-ttu-id="7eb94-128">-確認</span><span class="sxs-lookup"><span data-stu-id="7eb94-128">-Confirm</span></span>
<span data-ttu-id="7eb94-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7eb94-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eb94-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eb94-130">-WhatIf</span></span>
<span data-ttu-id="7eb94-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7eb94-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eb94-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7eb94-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eb94-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eb94-133">-DefaultProfile</span></span>
<span data-ttu-id="7eb94-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7eb94-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7eb94-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eb94-135">CommonParameters</span></span>
<span data-ttu-id="7eb94-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7eb94-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eb94-137">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7eb94-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eb94-138">輸入</span><span class="sxs-lookup"><span data-stu-id="7eb94-138">INPUTS</span></span>

### <span data-ttu-id="7eb94-139">所有</span><span class="sxs-lookup"><span data-stu-id="7eb94-139">None</span></span>
<span data-ttu-id="7eb94-140">您可以透過屬性名稱（而不是依值），將輸入管到這個 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7eb94-140">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="7eb94-141">輸出</span><span class="sxs-lookup"><span data-stu-id="7eb94-141">OUTPUTS</span></span>

### <span data-ttu-id="7eb94-142">所有</span><span class="sxs-lookup"><span data-stu-id="7eb94-142">None</span></span>

## <span data-ttu-id="7eb94-143">筆記</span><span class="sxs-lookup"><span data-stu-id="7eb94-143">NOTES</span></span>
* <span data-ttu-id="7eb94-144">關鍵字： azure、azurerm、arm、資源、管理、manager、redis、cache、web、webapp、網站</span><span class="sxs-lookup"><span data-stu-id="7eb94-144">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="7eb94-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="7eb94-145">RELATED LINKS</span></span>

[<span data-ttu-id="7eb94-146">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7eb94-146">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="7eb94-147">匯入-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7eb94-147">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="7eb94-148">新-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7eb94-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="7eb94-149">移除-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7eb94-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="7eb94-150">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7eb94-150">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


